## "The Effect of Background Music on Focused Work Performance"

*   `participant_id`: Unique identifier for each participant (Integer: 1-3000).
*   `academic_yr`: Participant's academic year, used for block randomisation (Factor: Levels "1" [Freshman], "2" [Sophomore], "3" [Junior], "4" [Senior]).
*   `assignment`: Randomly assigned experimental condition determining the background music played during the task (Factor: "No_Music", "Jazz" [with lyrics], "Instrumental_Jazz" [without lyrics]). This is the **Treatment** variable.
*   `response_min`: **Primary Outcome 1** - Time taken by the participant to complete the standardised task (Sudoku and reading comprehension) (Numeric, in minutes). Lower values indicate higher efficiency.
*   `percent_accuracy`: **Primary Outcome 2** - The percentage of questions answered correctly on the standardised task (Numeric: Scale 0-100). Higher values indicate better performance.

**Optional Covariates (Simulated based on Section 4.6 description, not used in the core outcome generation from PAP's R code):**

*   `jazz_familiarity`: Participant's self-reported familiarity with jazz music (Numeric: Likert scale 1-5, higher = more familiar).
*   `sleep_quality_binary`: Participant's self-reported recent sleep quality (Numeric: 0=Poor/No, 1=Good/Yes).
*   `music_study_habit_binary`: Indicator if participant habitually listens to music while studying (Numeric: 0=No, 1=Yes).
*   `caffeine_binary`: Indicator if participant consumed caffeine before the task (Numeric: 0=No, 1=Yes).
*   `stress_pre_test`: Participant's self-reported stress level immediately before the task (Numeric: Likert scale 1-5, higher = more stress).

**Notes:**

*   The core analysis involves comparing `response_min` and `percent_accuracy` across the `assignment` groups, controlling for `academic_yr` (as per the regression model in the PAP).
*   The optional covariates can be used for exploratory subgroup analyses or to potentially increase precision in regression models, although they were not part of the primary data generation specified in the PAP's `DeclareDesign` code.