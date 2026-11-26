---
title: "Bayesian Inference for Continuous-Time Structural Equation Models"
date: 2026-11-26
tags:
  - Bayesian Statistics
  - CTSEM
  - INLA
  - MCMC
  - R
  - Julia
---

Efficient Bayesian inference for continuous-time structural
equation models (CTSEM) with subject-specific random intercepts.

<!--more-->

## Bayesian Inference using ctsem 4.0.0

### Data Preparation

```r
library(ctsem)

example_data <- ctsem::ctstantestdat

data <- data.frame(
  id = example_data[, "id"],
  time = example_data[, "time"],
  y1 = example_data[, "Y1"],
  y2 = example_data[, "Y2"]
)
```

### Model Specification

```r
model <- ctsem::ctModel(
  type = "ct",
  manifestNames = c("y1", "y2"),
  latentNames = c("x1", "x2", "u1", "u2"),
  LAMBDA = cbind(diag(2), diag(2)),
  DRIFT = rbind(
    c("A11", "A12", 0, 0),
    c("A21", "A22", 0, 0),
    c(0, 0, 0, 0),
    c(0, 0, 0, 0)
  ),
  DIFFUSION = rbind(
    c("g11", 0, 0, 0),
    c("g21", "g22", 0, 0),
    c(0, 0, 0, 0),
    c(0, 0, 0, 0)
  ),
  T0MEANS = rep(0, 4),
  T0VAR = rbind(
    c("stationary", 0, 0, 0),
    c("stationary", "stationary", 0, 0),
    c(0, 0, "u11", 0),
    c(0, 0, "u21", "u22")
  ),
  MANIFESTMEANS = c("nu1", "nu2"),
  MANIFESTVAR = rbind(
    c("sd1", 0),
    c(0, "sd2")
  ),
  silent = TRUE
)

model$pars$indvarying[] <- FALSE
```

### Parameter Initialization

```r
ctsem_raw_names <- c(
  "A11", "A12", "A21", "A22",
  "g11", "g21", "g22",
  "sd1", "sd2", "nu1", "nu2",
  "u11", "u21", "u22"
)

init <- setNames(
  rep(0, length(ctsem_raw_names)),
  ctsem_raw_names
)

init[c("g11", "g22", "u11", "u22", "sd1", "sd2")] <- -1

init[c("nu1", "nu2")] <-
  colMeans(data[c("y1", "y2")], na.rm = TRUE) / 10
```

### Bayesian Inference via NUTS

```r
ctsem::ctJuliaSetup(threads = 4, force = TRUE)

fit_time <- system.time({
  fit_ctsem <- ctsem::ctFit(
    data,
    model,
    backend = "julia",
    cores = 4,
    priors = TRUE,
    optimize = FALSE,
    inits = unname(init),
    sampleControl = list(
      sampler = "nuts",
      warmup = 200,
      iter = 1000,
      seed = 20261123
    )
  )
})
```

### Results

```r
cat(sprintf(
  "Elapsed time: %.2f seconds\n",
  fit_time[["elapsed"]]
))

summary(fit_ctsem)
```
