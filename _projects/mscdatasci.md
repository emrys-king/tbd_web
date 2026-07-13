---
layout: project
title: 'Imperial Data Science Challenge'
author-profile: true
collection: projects
sort_date: 2026.07
display_date: "2026"
github: "https://github.com/emrys-king/datasci-challenge"
---

The 2026 MSc Statistics Data Science Challenge was held from July 7-9. We were tasked with analysing the RE-Europe Dataset, a landmark dataset combining renewable energy supply and demand data across 26 European countries. In particular, the data tracked inflows and outflows of wind- and solar-generated energy from over 1,400 buses (power stations). My team focused on residual load, which in this case is calculated via:

$$
R_{t,n} = L_{t,n} - \texttt{CF}_{t,n}^{\textrm{wind}}\alpha_{\textrm{wind}} C_n^{\textrm{wind}} - \texttt{CF}_{t,n}^{\textrm{solar}}\alpha_{\textrm{solar}} C_n^{\textrm{solar}}
$$

where $$R_{t,n}$$ is the residual load (in MWh), $$L_{t,n}$$ is the load (in MWh), $$\texttt{CF}_{t,n}$$ the capacity factor, $$C_n$$ the layout capacity, and $$\alpha$$ the penetration rate. These are indexed in time (representing hourly observations) and by bus. Intuitively, one can think of the load as the demand for energy across a certain population, and the two product terms as the supply of each type of energy, such that the residual load becomes the difference between total energy demand and renewable energy supply. Thus, a high residual load means that most of the energy demand is not being met through renewable means.

Of particular interest to my group were the penetration rates, $$\alpha_{\textrm{wind}}$$ and $$\alpha_{\textrm{solar}}$$. These are not available from the data but rather set manually to reflect the rate of adoption of the energy by the surrounding population. In the dataset as given to us, these were set to the cross-Europe average at the start of data collection, in 2012. We compared these rates with current (2026) adoption rate estimates and projected adoption rates for 2030. 

Our data analysis was mainly exploratory given time constraints. I particularly enjoyed looking at parametric curve-fitting for the distributions of ramp rates, which are simply rate of change between time points of residual load. Finding a proper distribution is key to forecasting stress events on the grid, as stress events will typically only occur with a large positive ramp rate (corresponding to high demand) or large negative ramp rate (high supply). The key insight we found was that as adoption increased, the variance of the parameters from country to country increased as well, indicating that a continental-level forecasting method would be less useful than a more localized model.