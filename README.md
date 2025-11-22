Please acknowledge the use of these scripts in any publications that make use of them.

As shown in Reservoir3setsScheme_MultiDimLongData.ipynb, <b>Lorenz-63 for the 1000-step-ahead prediction (nondimensional time of 10) achieves a MAE of 0.014</b> for the standardized dataset, computed as the mean error over the entire prediction horizon.


Comparison with Feng et al. (2025)

https://www.frontiersin.org/journals/big-data/articles/10.3389/fdata.2024.1506443/full

Feng et al. (2025) report a non-standardized MAE ≈ 1.19 for the Lorenz-63 system at t = 10 (1000 steps), computed as the mean error over the entire prediction horizon. When converted into the standardized scale, this corresponds to a standardized MAE of <b>approximately 0.10–0.12.</b>

However, their training dataset consists of only 6,000 samples, whereas ours contains 600,000, so this difference should naturally be taken into account.　Even so, under a straightforward comparison, our model clearly outperforms theirs.

---

<h2>Novelty and Significance of This Work</h2>

Predicting chaotic dynamical systems such as the Lorenz-63 model has traditionally been performed with relatively small datasets—typically a single trajectory of a few thousand time steps.
This convention stems from the widely held belief that chaotic systems do not significantly benefit from large-scale data, because prediction horizons are fundamentally limited by exponential error growth characterized by the Lyapunov time.
As a result, almost all prior studies—including recent state-of-the-art approaches such as Feng et al. (2025)—rely on training datasets of approximately 6,000 time steps, and rarely, if ever, exceed the order of 10⁴ samples.

In contrast, our approach leverages large-scale training datasets containing 6×10⁵ to 10⁶ time steps, which is two orders of magnitude larger than in existing work.
Training machine learning models on such extensive chaotic trajectories is technically challenging due to severe nonlinearity, broad state-space coverage, gradient instability, and heavy computational demands.
Consequently, to the best of our knowledge, no published study has demonstrated successful long-horizon Lorenz predictions with comparable dataset sizes.
