# QTM 385 Lecture 8 - Quiz Questions

**Instructions:** Each question has one correct answer (marked ✔️). Questions progress from basic concepts to applied analysis.

1. What is the primary purpose of blocking in experimental design?
A) Reduce total sample size  
B) Balance treatment groups within homogeneous subgroups ✔️  
C) Increase between-group variance  
D) Simplify random assignment procedures  

2. Intra-cluster correlation (ICC) approaching 1 indicates:
A) Perfect balance between clusters  
B) Maximum similarity within clusters ✔️  
C) Optimal power calculations  
D) Invalid treatment effects  

3. Which formula correctly calculates effective sample size (ESS) with clustering?
A) ESS = n/(1 + k*ICC)  
B) ESS = n/(1 + (k-1)*ICC) ✔️  
C) ESS = n*(1 - ICC)  
D) ESS = k/(n + ICC)  

4. In the community gardening program example, blocking was used to account for:
A) Neighborhood population density  
B) Baseline social cohesion differences ✔️  
C) Political affiliations  
D) Income inequality levels  

5. A cluster-randomized trial with 50 clusters (25 treated) and ICC=0.1 would need:
A) More clusters than individual randomization  
B) Fewer clusters than individual randomization  
C) Same number as individual randomization  
D) Cluster count doesn't affect power ✔️  

6. Which design feature most improves power in small samples?
A) Larger effect sizes  
B) Blocking on prognostic variables ✔️  
C) Increasing alpha level  
D) Using one-tailed tests  

7. The DeclareDesign code `declare_assignment(Z = block_ra(blocks = W))` implements:
A) Complete randomization  
B) Blocked randomization ✔️  
C) Cluster randomization  
D) Stratified sampling  

8. Pair matching in cluster RCTs helps address:
A) Treatment contamination  
B) Small number of clusters ✔️  
C) Missing data issues  
D) Selection bias  

9. Which ICC value would require the largest sample adjustment (N=1000, k=20)?
A) 0.00  
B) 0.05  
C) 0.20 ✔️  
D) 0.50  

10. In the power formula β = Φ(δ√N/(2σ) - Φ⁻¹(1-α/2)), δ represents:
A) Significance level  
B) Standard deviation  
C) Treatment effect size ✔️  
D) Cluster size  

11. Blocking is particularly advantageous when:
A) Sample sizes are very large  
B) Treatment effects are homogeneous  
C) Important subgroups exist ✔️  
D) Using linear regression models  

12. Which R function calculates cluster-robust standard errors?
A) lm()  
B) lm_robust() ✔️  
C) glm()  
D) coxph()  

13. The design effect formula for cluster sampling is:
A) 1 + (k-1)*ICC ✔️  
B) 1 + k*ICC  
C) k/(1-ICC)  
D) ICC/(k-1)  

14. In the community garden simulation, blocking reduced:
A) Treatment effect magnitude  
B) Estimate variance ✔️  
C) Sample size requirements  
D) Measurement error  

15. Which statement about power is FALSE?
A) Increases with sample size  
B) Decreases with variance  
C) Higher when using one-tailed tests  
D) Independent of effect size ✔️  

16. The Imai et al. (2009) matching method recommends:
A) Ignoring cluster sizes  
B) Pairing by geographic proximity  
C) Matching on covariates and cluster sizes ✔️  
D) Using post-treatment variables  

17. Which code implements blocked cluster randomization?
A) block_ra(blocks = neighborhood)  
B) cluster_ra(clusters = schools)  
C) block_and_cluster_ra() ✔️  
D) complete_ra(N = 100)  

18. An ICC of 0.15 with k=10 implies ESS reduction of:
A) 15%  
B) 43% ✔️ (1 + 9*0.15 = 2.35 → 1/2.35 ≈ 0.425)  
C) 58%  
D) 85%  

19. Which diagnostic is NOT provided by diagnose_design()?
A) Power  
B) Coverage  
C) Bias  
D) ICC value ✔️  

20. The "Lin estimator" improves power by:
A) Increasing sample size  
B) Adding covariate interactions ✔️  
C) Using Bayesian methods  
D) Reducing alpha level  

21. In cluster RCTs, valid inference requires:
A) Large number of clusters ✔️  
B) Equal cluster sizes  
C) ICC < 0.05  
D) Blocked assignment  

22. Which matching method creates pairs before randomization?
A) Propensity score matching  
B) Optimal pair matching ✔️  
C) Post-stratification  
D) Coarsened exact matching  

23. DeclareDesign's potential_outcomes() function specifies:
A) Randomization procedure  
B) Outcome model under treatment/control ✔️  
C) Covariate distributions  
D) Power calculations  

24. A Type II error occurs when we:
A) Reject a true null  
B) Accept a false null ✔️  
C) Overestimate effects  
D) Use wrong standard errors  

25. Which factor most improves power in fixed budget?
A) Larger clusters  
B) More clusters ✔️  
C) Higher ICC  
D) Smaller effects  

26. The simulation comparing blocked/unblocked designs showed:
A) No difference in estimates  
B) Lower variance with blocking ✔️  
C) Higher ATE with blocking  
D) Increased bias  

27. In power analysis, α typically sets to:
A) 0.01  
B) 0.05 ✔️  
C) 0.10  
D) 0.20  

28. Which is NOT a blocking benefit?
A) Balanced covariates  
B) Reduced variance  
C) Smaller required N  
D) Eliminates clustering need ✔️  

29. The formula ICC = σ²_b/(σ²_b + σ²_w) measures:
A) Treatment heterogeneity  
B) Between/within cluster variance ratio ✔️  
C) Blocking efficiency  
D) Power loss  

30. diagnose_design() reports all EXCEPT:
A) Power  
B) Bias  
C) RMSE  
D) Optimal block size ✔️