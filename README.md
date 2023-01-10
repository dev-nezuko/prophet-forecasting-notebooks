# Prophet forecasting study copy

A historical study copy of [facebook/prophet](https://github.com/facebook/prophet), including its Python implementation, documentation notebooks, example datasets, and compatibility shim. Prophet was developed by Facebook's Core Data Science team. This repository does not claim authorship of the forecasting library or its tutorial results.

The bundled upstream README describes the 1.1.4 era and is preserved as [UPSTREAM_README.md](UPSTREAM_README.md). Its badges and release instructions refer to upstream, not to checks run on this repository. The [MIT license](LICENSE) and upstream copyright notices are retained.

## Reading route

| Notebook | What to examine |
| --- | --- |
| [Quick start](notebooks/quick_start.ipynb) | `ds` / `y` inputs, fit, future dates, prediction |
| [Trend changepoints](notebooks/trend_changepoints.ipynb) | Trend flexibility and regularization |
| [Seasonality and regressors](notebooks/seasonality,_holiday_effects,_and_regressors.ipynb) | Calendar effects and extra information |
| [Diagnostics](notebooks/diagnostics.ipynb) | Time-based cross-validation and forecast metrics |
| [Uncertainty intervals](notebooks/uncertainty_intervals.ipynb) | Assumptions behind interval coverage |
| [Handling shocks](notebooks/handling_shocks.ipynb) | Structural breaks in a pedestrian-count example |

Additional notebooks cover outliers, saturation, multiplicative seasonality, non-daily data, and serialization. `examples/` supplies historical demonstration CSVs; those samples are not evidence of a deployed forecasting service.

## Layout and execution

`python/` contains the upstream Python package and tests. `python_shim/` provides the older `fbprophet` import compatibility layer. `docs/` and `notebooks/` are educational material rather than an application API or dashboard.

For static reading, GitHub's notebook renderer needs no local installation. Inspect notebook code before running it: tutorial cells can fetch data or fit models. Notebook outputs already stored here are historical upstream illustrations; they were not regenerated or independently validated during this review.

For deliberate execution, create a separate environment, select and record a compatible Prophet release, and follow the [official quick start](https://facebook.github.io/prophet/docs/quick_start). The preserved upstream README explains source builds. This copy's `setup.py` can download and compile CmdStan; the old Dockerfile uses Python 3.7 Stretch and has not been validated. No automatic install or Docker build was performed.

## What this demonstrates today

This is a reference collection for studying a forecasting library, not an original ML experiment, deployed model, or measured performance claim. Its portfolio value would improve with one separate, reproducible case study: a documented dataset, chronological holdout, seasonal-naive baseline, horizon-specific MAE, and an explanation of failures. That evaluation has not been implemented here, so no invented scores or new benchmark charts are shown.

The review parsed the notebook JSON and Python source and audited locally available Git objects without executing repository code. This establishes structural readability and the recorded audit coverage, not forecasting correctness or reproducibility. Existing upstream plots can be read in the notebooks; another screenshot would duplicate them.
