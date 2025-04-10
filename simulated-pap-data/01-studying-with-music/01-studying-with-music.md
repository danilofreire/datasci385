## "Studying with Music: Benefit or Harm on Academic Performance"

*   `participant_id`: Unique identifier for each student participant (Integer).
*   `university`: Simulated university site attended by the participant (Factor: "Uni A", "Uni B", "Uni C", "Uni D").
*   `major_field`: Broad academic field of study (Factor: "STEM", "Humanities"). Stratification variable.
*   `major_specific`: Specific declared major within the broad field (Factor: "Biology", "Chemistry", "Physics", "History", "Creative Writing", "Cultural Studies").
*   `age`: Participant's age in years (Integer: Range 18-25).
*   `gender`: Participant's self-reported gender (Factor: "Female", "Male", "Other/Prefer not to say").
*   `gpa`: Participant's cumulative Grade Point Average (Numeric: Range approx 1.5-4.0). Contains missing values (NA) introduced based on a Missing Not At Random (MNAR) mechanism (lower true GPA was more likely to be missing).
*   `music_habit`: Self-reported frequency of listening to music while studying (Factor: "Low", "Medium", "High"). Used as a blocking variable.
*   `personality_extroversion`: Score on a simulated extroversion scale (Numeric: Standard normal scale, higher score = more extroverted). Simulated Heterogeneous Treatment Effect modifier.
*   `personality_conscientiousness`: Score on a simulated conscientiousness scale (Numeric: Standard normal scale, higher score = more conscientious). Contains missing values (NA).
*   `prior_test_experience`: Self-reported prior experience with standardised tests (Factor: "Low", "High").
*   `block_id`: Identifier for the randomisation block based on `major_field`, baseline GPA category (`gpa_block` derived internally), and `music_habit` (Factor).
*   `treatment`: Assigned study condition (Factor: "Silence", "Lyrical Music"). Randomised within blocks. This is the **Treatment Assignment** variable.
*   `completed_study`: Indicator whether participant completed the 1-hour study session (Numeric: 0 = No/Dropped Out, 1 = Yes). Attrition was simulated to be slightly higher in the "Lyrical Music" group.
*   `reading_score`: **Primary Outcome** - Score on the reading comprehension test (Numeric: Scale approx 0-50). Contains NAs for participants where `completed_study = 0`. Effect of music was programmed to be negative and statistically significant.
*   `math_score`: **Primary Outcome** - Score on the arithmetic math test (Numeric: Scale approx 0-50). Contains NAs for participants where `completed_study = 0`. Effect of music was programmed to be negative but smaller and likely non-significant.
*   `distraction_rating`: **Secondary Outcome** - Self-reported distraction level post-session (Ordered Factor: 1 = "Not distracted at all" to 5 = "Very distracted"). Contains NAs for participants where `completed_study = 0`.
*   `heart_rate_avg`: **Secondary Outcome** - Average heart rate during the session, measured by simulated wearable device (Numeric: beats per minute). Contains NAs for participants where `completed_study = 0`.

**Notes:**

*   The primary analysis involves comparing `reading_score` and `math_score` between the `treatment` groups ("Silence" vs "Lyrical Music").
*   Blocking variables (`major_field`, `gpa_block` [internal], `music_habit`) were used during randomisation. `block_id` captures the specific block.
*   Heterogeneous treatment effects were simulated based on `personality_extroversion` and `music_habit`.
*   The dataset includes realistic challenges: differential attrition, MNAR missingness, and MCAR missingness.
*   Outcome variables contain NAs due to attrition.
