Please acknowledge the use of these scripts in any publications that make use of them.

As shown in Reservoir3setsScheme_MultiDimLongData.ipynb, the <b>1100-step-ahead prediction (nondimensional time of 11) achieves a MAE of 0.128</b> (for the standardized dataset).


Comparison with Feng et al. (2025)

Feng et al. (2025) report a non-standardized MAE ≈ 1.19 at t = 10 (1000 steps), computed as the mean error over the entire prediction trajectory.
In contrast, our model attains a standardized MAE = 0.11 specifically at t = 11, evaluated at the most challenging point of the free-rollout horizon and averaged over many test initial conditions.
When converted back to the original scale, this corresponds to a non-standardized error of roughly 1.1–1.3, despite being measured only at the final, hardest prediction time rather than diluted by earlier, easier steps.

Because Feng et al.’s metric benefits from averaging over the entire trajectory while ours reflects the single most error-amplified point of a longer prediction window, this performance difference is substantial.
Under directly comparable scaling, our model delivers markedly stronger long-horizon predictive accuracy, outperforming Feng et al.’s results under a significantly more stringent evaluation criterion.
