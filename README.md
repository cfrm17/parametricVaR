# Parametric Value At Risk Summary

Value at Risk (VaR) is the regulatory measurement for assessing market risk. It reports the maximum likely loss on a portfolio for a given probability defined as x% confidence level over N days. VaR is vital in market risk management and control. Also regulatory and economic capital computation is based on VaR results. Although VaR measure is objective and intuitive, it doesn’t capture tail risk. There are three commonly used methodologies to calculate VaR – parametric, historical simulation and Monte Carlo simulation. This presentation focuses on parametric VaR.  

Keywords:
Value at Risk, VaR, parametric VaR, market risk, financial market, trading risk, risk analytics, risk implementation

	Parametric VaR
	Definition
Value at Risk (VaR) is the regulatory measurement for assessing market risk. It reports the maximum likely loss on a portfolio for a given probability defined as x% confidence level over N days. VaR is vital in market risk management and control. 
 

	VaR Roles
	Risk measurement
	Risk management
	Risk control
	Financial reporting
	Regulatory and economic capital

	VaR Pros & Cons
	Regulatory measurement for market risk
	Objective assessment
	Intuition and clear interpretation
	Consistent, flexible and stable measurement
	Doesn’t measure risk beyond the confidence level: tail risk
	Non sub-additive

	VaR Approaches
	Parametric VaR
	Historical VaR
	Monte Carlo VaR

	Parametric VaR Methodology
	Assuming an asset return/valueChange follows normal distribution, the quantile of 99% confidence level is 2.33σ where σ is standard derivation

	Parametric VaR Implementation

	For each asset/instrument (risk factor), calibrate volatility σ_i based on daily return
	For each pair, calibrate correlation ρ_ij
	Calculate the variance of a portfolio value change
V_p^2=⌊■(∆〖(P〗_1)σ_1&…&∆(P_n)σ_n )⌋[■(ρ_11&…&ρ_1n@⋮&&⋮@ρ_n1&⋯&ρ_nn )][■(∆〖(P〗_1)σ_1@⋮@∆(P_n)σ_n )]
	The portfolio VaR is 2.33√(V_p^2 )

∆(P) = Delta * ∆(X) + 0.5 * Gamma * ∆(X)^2 + Vega*∆(V)+Theta * ∆(T)

	VaR Scaling
	Normally firms compute 1-day 99% VaR
	Regulators require 10-day 99% VaR
	Under IID assumption, 10-day VaR = √10*〖VaR〗_(1-day)

	VaR Backtest
	The only way to verify a VaR system is backtest
	At a certain day, compute hypothetic P&L (valuation date and portfolio unchanged)
If (hypothetic P&L > VaR)  breach
	For one year
If number of breaches is 0-4, the VaR system is in Green zone
If number of breaches is 5-9, the VaR system is in Yellow zone
If number of breaches is 10 or more, the VaR system is in Red zone


Reference:

https://finpricing.com/FinPricing-ProductBrochure.pdf
