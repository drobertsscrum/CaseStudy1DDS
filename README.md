# CaseStudy1DDS
MSDS 6306: Doing Data Science Case Study 1 repository

Executive Summary: The State of the Workforce
Analysis of the current Frito Lay workforce reveals an attrition rate of 16.1%, representing a total headcount loss of 140 employees. This analysis shifts the strategic focus from "The Probability Trap"—high-percentage risks that involve low total headcount—to "The Volume Reality," where the actual financial exposure resides.

Our core finding demonstrates that proactive retention is a profit-preservation engine. A targeted $200 retention intervention can prevent departures that cost the organization up to $237,384 per executive role. After rigorous algorithmic validation, the k-NN model is identified as the definitive mathematical winner. It provides maximum protection for high-value assets while maintaining superior operational efficiency, saving the organization capital by reducing false-positive incentive expenditures.

Project Context and Objectives
The mission is to maximize the Return on Investment (ROI) of human capital by predicting and preventing employee attrition. We move beyond simple percentage-based reporting to quantify the catastrophic financial risk of losing specialized talent.

Core Objectives:
Mitigate Financial Risk: Prioritize retention for roles where replacement costs reach 4.0x salary.
Overcome The Probability Trap: Identify drivers that move the needle on headcount volume rather than statistical outliers.
Predictive Optimization: Identify the machine learning model that catches the most leavers with the highest operational efficiency.
Data Dictionary and Feature Engineering
To ensure technical reproducibility, the following features have been extracted and engineered from the Frito Lay dataset. Ordinal scales are defined per the standard technical documentation.
Feature Name:

Age
Attrition
BusinessTravel
Department
DistanceFromHome
Education
EducationField
EnvironmentSatisfaction
JobInvolvement
JobLevel
MonthlyIncome
OverTime
PerformanceRating
StockOptionLevel

Attrition Driver Analysis
The Volume Reality
While factors like "Frequent Travel" show high probability, they represent lower total headcount loss and act as financial distractions. 
To maximize ROI, we target the high-volume drivers:
Zero Stock Options: 98 Employees Lost.
Job Level 1 (Entry Level): 86 Employees Lost.
Mandatory OverTime: 80 Employees Lost.

Actionable vs. Noise
Technical analysis distinguishes between root causes and "The False Signal."
The Noise: Performance Rating = 3 shows 117 leavers. However, this is a baseline state (the majority of employees receive a 3) and does not indicate a causal driver for departure.
The Target: We focus on actionable variables—equity, job level support, and workload—that directly correlate with the 140-person loss.

Financial Impact Modeling
Using the median annual salary of $59,346, we quantify the liability associated with reactive replacement. A $200 proactive investment represents a fraction of the cost of losing an employee.
Replacement Liability Scorecard
Scenario
Replacement Cost
0.5x Salary (Entry Level)
$29,673
1.0x Salary (Professional)
$59,346
2.0x Salary (Management)
$118,692
4.0x Salary (Executive)
$237,384

Predictive Modeling and Comparison
Model Confusion Matrix Scorecard
We evaluated k-Nearest Neighbors (k-NN) and Naive Bayes to identify flight risks.
Model
TP
FP
TN
FN
Accuracy
Sensitivity
Specificity
Precision
k-NN (k=23, t=0.09)
27
75
144
15
65.5%
64.3%
65.8%
26.5%
Naive Bayes (t=0.11)
27
86
133
15
61.3%
64.3%
60.7%
23.9%

Both models achieve an identical Sensitivity of 64.3%, catching exactly 27 actual leavers. This provides the same level of safeguard against the catastrophic costs of Because protection levels are equal, the choice depends on Operational Efficiency. k-NN demonstrates higher Specificity (65.8% vs 60.7%).

Financial Impact: By generating 11 fewer false alarms (75 vs 86), k-NN requires an upfront incentive cost of $20,400 compared to 22,600forNaiveBayes.Utilizingk−NNresultsinanimmediate∗∗2,200 savings gap** in upfront incentive capital.

Repository Usage and Reproducibility
/data: Contains the raw HR Analytics dataset and the extended Data Dictionary.
/scripts: Includes R scripts for model tuning (k=23) and confusion matrix generation.
/results: Houses the financial impact visualizations and model performance scorecards.
To replicate these results, execute the model scripts using the provided tuning parameters (k=23, t=0.09) to maintain the specificity advantage required for maximum ROI.
