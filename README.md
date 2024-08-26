# Merton

The Merton model is a structural credit risk model that treats a company's equity as a call option on its assets, with the strike price being the value of the company's debt. This model helps in assessing the likelihood of a company defaulting on its debt obligations by modeling the company's assets as a stochastic process (typically a geometric Brownian motion). The key concept is that default occurs if the value of the company's assets falls below its debt at maturity.


Asset Value Dynamics:
The value of the company's assets is assumed to follow a geometric Brownian motion, which can be described by the stochastic differential equation:
dV = V * (mu * dt + sigma * dW)
Here:
V is the value of the company's assets.
mu is the drift rate (expected return on assets).
sigma is the volatility of the asset value.
dt is a small time increment.
dW is a Wiener process (or Brownian motion).

Distance to Default:
The distance to default represents how many standard deviations the current asset value is from the default threshold (i.e., the debt value). It is calculated as:
Distance to Default = (log(V / D) + (r + 0.5 * sigma^2) * T) / (sigma * sqrt(T))
Here:
V is the current value of the company's assets.
D is the face value of the company's debt (default point).
r is the risk-free interest rate.
sigma is the volatility of the asset value.
T is the time to maturity of the debt.

Default Probability:
The probability that the company will default on its debt is the probability that the asset value will fall below the debt value by the time the debt matures. This is calculated using the cumulative distribution function (CDF) of the standard normal distribution:
Default Probability = N(-Distance to Default)
Here:
N() is the cumulative distribution function of the standard normal distribution.
Distance to Default is calculated as shown above.


Asset Value Dynamics:
dV = V * (mu * dt + sigma * dW)

Distance to Default:
Distance to Default = (log(V / D) + (r + 0.5 * sigma^2) * T) / (sigma * sqrt(T))

Default Probability:
Default Probability = N(-Distance to Default)
