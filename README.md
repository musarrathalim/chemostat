# chemostat
Chemostat Simulation and Sensitivity Analysis
Project Overview
This project simulates a continuous stirred-tank bioreactor (chemostat) using Monod kinetics and performs parameter sensitivity analysis to study the impact of key variables on microbial growth.
The project is designed for beginners in biochemical engineering / systems biology, yet it demonstrates research-relevant analysis, including steady-state behavior, washout phenomena, and sensitivity to biological and process parameters.

Objectives


Simulate chemostat behavior over a range of dilution rates.


Identify the washout point, where biomass cannot sustain itself.


Perform sensitivity analysis for key parameters:


Maximum specific growth rate (μmax)


Half-saturation constant (Ks)


Biomass yield coefficient (Yx/s)


Feed substrate concentration (S_in)




Visualize the results using growth curves, substrate profiles, and heatmaps.



Background
A chemostat is a continuous bioreactor in which fresh medium is added and culture broth is removed at a constant rate (dilution rate, D). The Monod equation describes the microbial growth rate as a function of substrate concentration:
μ(S)=μmaxSKs+S\mu(S) = \mu_{max} \frac{S}{K_s + S}μ(S)=μmax​Ks​+SS​
Where:


μ(S) = specific growth rate (1/h)


μmax = maximum specific growth rate (1/h)


Ks = half-saturation constant (g/L)


S = substrate concentration (g/L)


The mass balances for biomass (X) and substrate (S) in a chemostat are:
dXdt=(μ(S)−D)X\frac{dX}{dt} = (\mu(S) - D) XdtdX​=(μ(S)−D)X
dSdt=D(Sin−S)−μ(S)Yx/sX\frac{dS}{dt} = D(S_\text{in} - S) - \frac{\mu(S)}{Y_{x/s}} XdtdS​=D(Sin​−S)−Yx/s​μ(S)​X
Where Yx/s is the biomass yield coefficient (g biomass / g substrate).


How to Run


Open chemostat_sensitivity.ipynb in Google Colab or Jupyter Notebook.


Run all cells to simulate:


Biomass and substrate over a range of dilution rates


Sensitivity analysis for μmax, Ks, Yx/s, and S_in


2D heatmap of steady-state biomass as a function of μmax and Ks




All plots are automatically generated and saved in the figures/ folder.



Key Results


Chemostat Sweep:


Steady-state biomass decreases with increasing D.


Washout occurs when D ≈ μmax.


Substrate concentration increases at high D because microbes cannot consume it fast enough.




Sensitivity Analysis:


μmax and Yx/s have the largest impact on steady-state biomass.


Ks affects biomass moderately; higher Ks reduces growth efficiency.


S_in affects biomass linearly up to saturation.


Heatmap visualizes combined effects of μmax and Ks on biomass.




These insights demonstrate critical parameters for continuous fermentation optimization.

Extensions / Future Work


Include product formation and inhibition in the model.


Explore substrate inhibition using Haldane kinetics.


Simulate multiple microbial species in a co-culture chemostat.


Optimize dilution rate and feed concentration for maximum productivity.



Technologies Used


Python


numpy – numerical arrays


scipy.integrate.odeint – solve ODEs


matplotlib – plotting


seaborn – heatmaps







esearch applications.
Do you want me to do that?
