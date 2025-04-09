## "Daily Exercise Regimen Effect on Sleep Quality"

*   `participant_id`: Unique identifier for each participant (Integer).
*   `sex`: Participant's self-reported sex category used for stratification (Factor: "Male", "Female", "Other/NB"). Stratification Variable 1.
*   `chronotype`: Participant's chronotype category used for stratification (Factor: "Morning", "Intermediate", "Evening"). Stratification Variable 2.
*   `block_id`: Identifier for the randomisation block, representing a unique combination of `sex` and `chronotype` (Factor).
*   `treatment_group`: Randomly assigned experimental condition (Numeric: 0 = Control [no change], 1 = Exercise [daily jogging]). This is the **Treatment Assignment** variable.
*   `tst_baseline`: **Primary Outcome (Baseline)** - Average Total Sleep Time during the baseline week (Numeric, minutes). Contains NAs if baseline data is incomplete.
*   `latency_baseline`: **Secondary Outcome (Baseline)** - Average Sleep Latency during the baseline week (Numeric, minutes). Contains NAs if baseline data is incomplete.
*   `waso_baseline`: **Secondary Outcome (Baseline)** - Average Wake After Sleep Onset during the baseline week (Numeric, minutes). Contains NAs if baseline data is incomplete.
*   `efficiency_baseline`: **Secondary Outcome (Baseline)** - Average Sleep Efficiency during the baseline week (Numeric, percentage 0-100). Contains NAs if baseline data is incomplete.
*   `awakenings_baseline`: **Secondary Outcome (Baseline)** - Average number of awakenings during the baseline week (Numeric, count). Contains NAs if baseline data is incomplete.
*   `tst_post`: **Primary Outcome (Post-Intervention)** - Average Total Sleep Time during the 14-day intervention period (Numeric, minutes). Contains NAs if intervention data is incomplete.
*   `latency_post`: **Secondary Outcome (Post-Intervention)** - Average Sleep Latency during the intervention period (Numeric, minutes). Contains NAs if intervention data is incomplete.
*   `waso_post`: **Secondary Outcome (Post-Intervention)** - Average Wake After Sleep Onset during the intervention period (Numeric, minutes). Contains NAs if intervention data is incomplete.
*   `efficiency_post`: **Secondary Outcome (Post-Intervention)** - Average Sleep Efficiency during the intervention period (Numeric, percentage 0-100). Contains NAs if intervention data is incomplete.
*   `awakenings_post`: **Secondary Outcome (Post-Intervention)** - Average number of awakenings during the intervention period (Numeric, count). Contains NAs if intervention data is incomplete.
*   `sleep_env_quality`: Covariate - Participant's self-reported sleep environment quality (Numeric, continuous scale, higher=better). Matches `SEQ` in PAP model.
*   `alcohol_drug_use`: Covariate - Indicator of participant's self-reported alcohol or drug use frequency (Numeric: 0=Low/None, 1=Moderate/High). Matches `ALC` in PAP model.
*   `exercise_compliance_rate`: Compliance Measure - For participants in the treatment group (`treatment_group=1`), the proportion of the 14 days the exercise requirement was met, based on simulated wearable data (Numeric: 0-1). NA for Control group.
*   `is_compliant`: Compliance Measure - Indicator of whether participants in the treatment group met the compliance threshold (>= 12/14 days) (Numeric: 0=No, 1=Yes). NA for Control group.
*   `completed_baseline_week`: Data Quality Indicator - Whether participant provided sufficient valid data during the baseline week (Numeric: 0=No, 1=Yes).
*   `completed_intervention_data`: Data Quality Indicator - Whether participant provided sufficient valid data during the intervention period (Numeric: 0=No, 1=Yes).

**Notes:**

*   The primary analysis involves comparing post-intervention outcomes (e.g., `tst_post`) between `treatment_group` 0 and 1, typically controlling for the corresponding baseline outcome (e.g., `tst_baseline`) and other covariates/blocking factors (`sex`, `chronotype`, `sleep_env_quality`, `alcohol_drug_use`) as shown in the PAP's example regression model.
*   Interaction terms (e.g., `treatment_group * chronotype`) are used to test the secondary hypotheses about moderation.
*   Outcome variables (`_baseline` and `_post`) contain NAs if the respective data collection period was deemed incomplete (`completed_baseline_week=0` or `completed_intervention_data=0`).
*   Compliance variables (`exercise_compliance_rate`, `is_compliant`) are only relevant for the treatment group and can be used for per-protocol analyses (secondary to the main ITT analysis).