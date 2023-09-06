# GeoVal

_GeoVal_ is a Python tool for evaluating grid-integrated geothermal projects. This tool combines Unit Commitment and Economic Dispatch models to optimize generator scheduling and costs. Regulators can use GeoVal to assess how adding geothermal units affects grid economics, reliability, and project profitability. It also helps analyze geothermal's role in stabilizing the electricity grid or firming renewable power.

## Model Formulation
_GeoVal_ optimizes yearly electricity generation and storage at minimal cost, factoring in hourly demand, grid reliability, and technical constraints. The goal is to minimize both investment and operational costs. Constraints include ramp rates, uptime/downtime, minimum output, and storage cycling. The model also accounts for spinning reserves, both for ramping up and down. Electricity prices are determined by merit-ordering generators based on their fixed and variable costs. Post-analysis calculates procurement costs, unserved load, emissions, curtailment, and revenue streams to assess the net revenue of each unit.

## Model Assumptions
We obtained CAPEX and Variable cost assumptions from NREL’s ATB updated in 2023. Other cost assumptions are obtained from Zhuo et al. For geothermal technologies, there are three main types of energy conversion processes: dry steam, flash steam, and binary cycles. We assume a 90% CF for flash plants, and an 80% CF for binary plants. To capture the impact of the volatility of Natural Gas (NG) prices, we used the industrial cost of NG obtained from EIA and used it as an hourly fuel cost for Natural Gas Combined Cycle (NGCC) power plants. Lastly, we assume that 50% of VRE capacity is paired with storage systems across all scenarios.
