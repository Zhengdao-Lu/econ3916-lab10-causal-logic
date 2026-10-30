# econ3916-lab10-causal-logic
Correlation & Causality: Confounders, Colliders and the Limits of Controls
Objective
I explored how the same observed correlation can arise from causation, confounding, or selection, and how the choice of controls affects a causal estimate.

Methodology
- I simulated three worlds with different causal structures and compared their correlations.
- I drew directed graphs for a confounder, collider, and mediator using NetworkX.
- I used regressions to compare estimates with and without controls, including a control measured before treatment.
- I wrote coef_on_d() to return the treatment coefficient for different sets of controls.
- I compared the LaLonde randomized experiment with a CPS comparison group, then adjusted the observational estimate for measured covariates.

Key Findings
The three worlds produced correlations of 0.654, 0.664, and 0.632, even though their true effects were 2.0, 0.0, and 0.0. Controlling for a collider produced an estimate of −0.592 where the true effect was 0. In the M-bias example, controlling for the pre-treatment variable gave −0.191; also controlling for u1 brought the estimate to 0.006.

The LaLonde experimental estimate was $1,794. Using the CPS comparison group gave −$8,498 without controls and $699 with controls, closing 89% of the gap to the experimental estimate.
