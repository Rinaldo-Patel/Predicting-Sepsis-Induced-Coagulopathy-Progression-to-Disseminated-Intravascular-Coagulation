# Predicting-Sepsis-Induced-Coagulopathy-Progression-to-Disseminated-Intravascular-Coagulation
Dynamic Two-Stage Early Warning System for Sepsis-Induced Coagulopathy and Progression to Disseminated Intravascular Coagulation: A MIMIC-IV Study

##Contributors - Rinaldo Brendon Patel, Amisha Kelkar, Chaitali Deshmukh, Pratik Mahajan

##Abstract - Sepsis leading to Sepsis-induced coagulopathy (SIC) is an
early manifestation of dysregulated host response and a
recognized precursor to disseminated intravascular
coagulation (DIC), a life-threatening critical condition
associated with organ failure and high mortality. These
disorders evolve dynamically, often before clinical signs
appear, and timely recognition is essential to guide the
intensity of monitoring, and early therapeutic interventions.
Current diagnostic tools are based on static laboratory
thresholds and are usually applied only well after
Coagulopathy has been established. Clinicians thus do not
have real-time support to identify which patients will likely
develop SIC or progress from SIC to DIC, potentially
delaying intervention during a narrow window when
outcomes might be most modifiable. Currently, there are no
approaches that integrate both stages of coagulopathy as a
unified warning system meeting diagnostic criteria. A
strategy that could more promptly detect SIC and stratify the
risk of subsequent progression toward DIC may allow for
more timely management and possibly improve patient
outcomes.

##Objectives - To develop and validate a dynamic two-stage early-warning
system that predicts SIC onset 24 hours before diagnostic
criteria are met and identifies among patients with SIC
those at risk of progression to life-threatening DIC, using
high-granularity clinical data from MIMIC-IV .

#Results - The Stage 1 model for early identification of sepsis-induced
coagulopathy (SIC) demonstrated strong discrimination and
calibration. CatBoost achieved an AUROC of 0.93 and an
AUPRC of 0.92, with high sensitivity (0.88) and specificity
(0.85) at the optimal threshold. SHAP analyses revealed
physiologically coherent predictors, decreasing platelet count,
rising INR/PT, metabolic acidosis (base excess), and SOFA
trajectory features, indicating early coagulopathy and
evolving organ dysfunction. 
In Stage 2, 813 SIC-positive patients were evaluated for
progression to disseminated intravascular coagulation (DIC),
of whom 56% progressed. Logistic regression captured major
linear effects (AUROC 0.64, AUPRC 0.70). CatBoost
improved performance (AUROC 0.68, AUPRC 0.72) and
enabled clinically relevant threshold selection. An
F1-optimized threshold (T = 0.256) yielded very high
sensitivity (0.95), suitable for early deterioration alerts. A
Youden-optimized threshold (T = 0.310) produced a more
balanced profile (sensitivity 0.89, specificity 0.39). SHAP
values identified inflammation (WBC), coagulation pathway
dysfunction (platelets, PT/INR, fibrinogen), renal impairment
(BUN), tissue hypoperfusion (lactate), and respiratory failure
indicators (PaO₂, A-a gradient) as dominant signals of DIC
progression.Across both stages, distributional analyses such
as Mann–Whitney U, chi-square, odds ratios, Cohen’s d, and
Cramér’s V confirmed statistically significant differences
between progression and non-progression groups. Fairness
evaluation across gender and race showed no systematic
disparities in accuracy, true-positive rates, false-positive rates, or selection rates.
