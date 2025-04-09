# Studying with Music: Benefit or Harm on Academic Performance
## Angela Xie, Esther Yang, Zhiyi (Yolanda) Li, Elizabeth Shin, Emily Choi

This is a very good Pre-Analysis Plan. The motivation for the study is clear, and the literature is well-connected to your main research questions. There are a few areas where clarification or additional detail would make it even stronger, which I've outlined below.

## Strengths:

You have clearly defined the research question and distinguished well between primary and secondary hypotheses. These seem to be well based in theory (like the limited cognitive resources idea), and your specific predictions about reading vs. maths performance is also supported by the literature cited.

It's good that you plan to examine potential differences across subgroups (majors, GPA, personality, music habits), and you provide good justification for exploring these variations.

The detailed consent process and privacy measures are well considered. Very good job!

Using both objective (tests, heart rate) and subjective (self-reports) measures is also a good idea, and mentioning potential measurement errors is indeed the correct approach`

The stratified block randomisation is well-explained.

## Areas for Improvement and Considerations:

You list both reading and maths performance as primary estimands. It would be helpful to designate *one* as the single primary outcome you are most focused on, with the other(s) as secondary. This helps focus the interpretation later.

While you discuss compliance, the analysis plan should specify how you will handle cases where participants do not fully adhere to the assigned condition (e.g., listen to music when they shouldn't). Consider stating whether you will use an intention-to-treat (ITT) approach (usually recommended, as we saw in class) or an as-treated (AT) approach.

You list covariates clearly, but the analysis section could be more specific about *how* they will be included in the regression models. For instance, which specific interaction terms do you plan to test? Defining this now helps avoid potential concerns about "p-hacking" or data fishing later when you analyse the results.

You mention inverse-probability weighting for missing data. Briefly explaining *why* you chose this method over alternatives (like multiple imputation, for example) would strengthen this section. I know we discussed this in class, but a brief justification here would be good.

Even in a single-session study, some participants might drop out partway through or refuse to complete certain tasks. It would be useful to add a sentence or two on how you plan to track and report this, and explain what you will do with such cases.

## Minor Technical Points:

Code Check: The example regression code `model <- lm_lin(X~Y, covariates = ~ majors + GPAs + personalities + study_habits, data = mydata)` appears to have the dependent (Y) and independent (X/treatment) variables reversed. It should likely be something like `model <- lm_lin(Y ~ treatment, covariates = ~ major + GPA + personality + study_habits, data = mydata)`.
Terminology: The description of standard errors could be slightly clearer. Ensure it explicitly states they represent the uncertainty around your estimated *treatment effect*, not just uncertainty related to the covariates.

Well done, and good luck with your study! :)