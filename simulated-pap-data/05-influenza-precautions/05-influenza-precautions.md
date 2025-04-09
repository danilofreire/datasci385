## Impact of Messaging on Influenza Precautions Compliance"

**Codebook: Simulated Influenza Messaging Data**

*   `participant_id`: Unique identifier for each participant (Integer).
*   `age_group`: Participant's age category (Factor: "Younger (18-44)", "Older (45+)"). Blocking factor.
*   `education_level`: Participant's education level category (Factor: "High School or less", "College or Higher"). Blocking factor.
*   `ses_level`: Participant's socioeconomic status category (Factor: "Lower-to-Middle", "Higher"). Blocking factor.
*   `social_interaction_freq`: Participant's social interaction frequency category (Factor: "Low-to-Moderate", "High"). Blocking factor.
*   `block_id`: Identifier for the randomisation block, based on the interaction of the four blocking factors (Integer: 1-16).
*   `treatment_group`: Randomly assigned messaging condition (Factor: "Control" [no message], "Fear-based", "Informational-based"). This is the **Intention-to-Treat** variable.
*   `completed_survey_t0`: Indicator if participant completed the baseline survey (Time 0 - September) (Numeric: 0=No, 1=Yes).
*   `completed_survey_t1`: Indicator if participant completed the first follow-up survey (Time 1 - November) (Numeric: 0=No, 1=Yes).
*   `completed_survey_t2`: Indicator if participant completed the second follow-up survey (Time 2 - February) (Numeric: 0=No, 1=Yes).

**Outcome Variables (Measured at t0, t1, t2):**

*   `mask_wear_t0` / `mask_wear_t1` / `mask_wear_t2`: **Outcome 1** - Self-reported daily mask wearing (Numeric: 0=No, 1=Yes). NA if the respective survey was not completed.
*   `vaccinated_t0` / `vaccinated_t1` / `vaccinated_t2`: **Outcome 2** - Self-reported influenza vaccination status for the current season (Numeric: 0=No, 1=Yes). NA if the respective survey was not completed.
*   `hospitalised_t0` / `hospitalised_t1` / `hospitalised_t2`: **Outcome 3** - Self-reported hospitalisation due to influenza since the previous survey (or baseline) (Numeric: 0=No, 1=Yes). This is a rare event. NA if the respective survey was not completed.
*   `sentiment_t0` / `sentiment_t1` / `sentiment_t2`: **Outcome 4** - Sentiment regarding the seriousness of influenza threat (Numeric: Continuous-like scale, simulated around -1 to 1 based on power analysis parameters, higher values indicate viewing influenza as a *more serious* threat). NA if the respective survey was not completed.

**Notes:**

*   The primary analysis involves comparing changes in outcomes (e.g., t1-t0, t2-t0, or simply t1/t2 levels controlling for t0) across the `treatment_group` levels.
*   Blocking factors (`age_group`, `education_level`, `ses_level`, `social_interaction_freq`) should be included in regression models to account for the design and increase precision.
*   Analyses need to account for missing outcome data due to survey non-completion (`completed_survey_t1=0` or `completed_survey_t2=0`).
*   The `sentiment` variable was simulated as continuous-like based on the PAP's power analysis, which differed from the binary measurement description.