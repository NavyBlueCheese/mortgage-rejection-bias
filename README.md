# Disproportionate Impact of Negative Credit Signals on Mortgage Rejection

This is a group project (Group 2) looking at whether negative credit history hits Black women applicants harder when it comes to mortgage rejections — like, does having a bankruptcy or late payments on your record push up your rejection odds more if you're a Black woman compared to everyone else?

## What we did

We used HMDA mortgage loan data and ran logit regressions to test this. The main thing we're looking at is the interaction between being a Black female applicant and various negative credit/mortgage signals (late payments, bankruptcy records, no prior mortgage history, etc.).

The models compare a baseline logit with a version that includes interaction terms so we can see if those negative signals "hit harder" for Black women specifically. We also computed average marginal effects and predicted probabilities to make the results more interpretable.

## Variables

- `reject` — whether the application was rejected (our outcome)
- `black_female` — indicator for Black female applicants
- `mortlat1` / `mortlat2` — one or multiple late mortgage payments
- `mortno` — no prior mortgage history
- `pubrec` — public bankruptcy record
- `chist` / `gdlin` — credit history and guideline flags
- `emp` — employment stability (years employed)

## Tools used

R, with `haven`, `dplyr`, `ggplot2`, `stargazer`, `margins`, and `AER`.

## Key takeaway

Black women face higher rejection rates on average, and some negative credit signals appear to increase their rejection probability more than for other applicants — though results vary by signal type.
