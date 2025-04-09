## "Does Gender Identity Matter? Exploring the Role of Gender on LGBTQ+ Attitudes" PAP

**Codebook: Simulated LGBTQ+ Attitudes Data**

This codebook describes the variables in the dataset.

*   `participant_id`: Unique identifier for each participant (Integer).
*   `gender_identity`: Participant's self-reported gender, used for block randomisation (Factor: "Male", "Female").
*   `treatment_group`: Randomly assigned experimental condition determining the video shown (Factor: "Pure Control" [neutral video], "Placebo Control" [heterosexual proposal], "Lesbian PDA" [lesbian proposal], "Gay Male PDA" [gay proposal]). This is the **Intention-to-Treat** variable.
*   `age`: Participant's age in years (Numeric). Covariate.
*   `sexual_orientation`: Participant's self-reported sexual orientation (Factor: "Heterosexual", "LGB+", "Other/Unknown"). Covariate.
*   `religiosity`: Participant's self-reported frequency of religious service attendance or importance of religion (Numeric: Ordinal scale 1-5, higher = more religious). Covariate.
*   `political_ideology`: Participant's self-reported political ideology (Numeric: Ordinal scale 1-7, higher = more conservative). Covariate.
*   `region`: Simulated geographic region of participant (Factor: "Northeast", "South", "Midwest", "West"). Supplemental Covariate.
*   `media_consumption`: Simulated index of media consumption habits (Numeric: 1-5 scale, higher=more). Supplemental Covariate.
*   `lgbtq_social_contacts`: Simulated number of LGBTQ+ identifying friends/close contacts (Integer: 0-5, higher=more). Supplemental Covariate.
*   `watched_video_compliantly`: Indicator if participant likely watched the assigned video without skipping or failing checks (Numeric: 0=No, 1=Yes). Compliance measure.
*   `completed_post_survey`: Indicator if participant completed the outcome survey after the video (Numeric: 0=No, 1=Yes). Measurement completion.
*   `attitude_lgbtq_post`: **Outcome Index 1** - Attitude towards LGBTQ+ people in general, measured post-treatment (Numeric: Scale approx. 1-7, higher = more positive attitudes, contains NAs).
*   `attitude_gay_post`: **Outcome Index 2** - Attitude towards gay men specifically, measured post-treatment (Numeric: Scale approx. 1-7, higher = more positive attitudes, contains NAs).
*   `attitude_lesbian_post`: **Outcome Index 3** - Attitude towards lesbian women specifically, measured post-treatment (Numeric: Scale approx. 1-7, higher = more positive attitudes, contains NAs).

**Notes:**

*   The primary analysis focuses on comparing the `attitude_..._post` outcomes across the `treatment_group` levels, potentially interacting with `gender_identity`.
*   Outcome variables (`attitude_..._post`) will have `NA` values if `completed_post_survey` is 0 or `watched_video_compliantly` is 0.
*   The PAP focuses analysis primarily on `Heterosexual` participants, which may require filtering the dataset based on the `sexual_orientation` variable.
*   This dataset follows a **post-test only** design as described in the PAP sections 4.5 and 6.