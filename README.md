# De Laval Nozzle: Thrust Analysis

This project investigates how the exit-to-throat area ratio of a converging-diverging (De Laval) nozzle affects its predicted thrust at different ambient pressures. The work combines an analytical nozzle-flow model, Python calculations, and parametric CAD geometry.

## Research question

How do nozzle expansion ratio and ambient pressure influence thrust when the other model inputs are held constant?

## Method

The numerical study considers five exit-to-throat area ratios (AR = 2, 3, 4, 5, and 6) and ambient pressures ranging from approximately 101.325 kPa (sea level) to 0 kPa (ideal vacuum).

The calculations use one-dimensional, isentropic compressible-flow relations to:
1. Determine the supersonic exit Mach number from the area–Mach relation.
2. Estimate the exit flow properties.
3. Calculate thrust from momentum and pressure contributions:

   `F = m_dot * v_e + (p_e - p_a) * A_e`

4. Compare predicted thrust across expansion ratios and ambient pressures.

Python, NumPy, and Matplotlib were used for the numerical analysis and plots. Parametric nozzle models were created in Onshape. The CAD geometries use a fixed throat radius with exit radius calculated as `r_e = r_t * sqrt(AR)`.

## Main observation

Under the assumptions of this model, a smaller expansion ratio gives higher predicted thrust near sea level, while a larger expansion ratio becomes more advantageous as ambient pressure approaches vacuum.

## Limitations

This is an analytical, idealized model—not an experimental validation or a CFD simulation. In particular, it does not resolve viscous losses, shock structures, boundary layers, or flow separation. Actual performance of overexpanded nozzles may therefore differ from the model's predictions.

## Project materials

- [Research notebook](De_Laval_Nozzle_Research.ipynb) — executable Python analysis and generated plots.
- CAD views and the research report will be added separately after review.

### Reproduce the calculations

Install dependencies with `pip install -r requirements.txt`, then open and run the notebook using Jupyter or Google Colab.
