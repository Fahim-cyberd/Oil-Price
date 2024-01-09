from fredapi import Fred
import matplotlib.pyplot as plt

# Set up Fred with your API key
fred = Fred(api_key='API')

# Get the oil price data
oil_price = fred.get_series('DCOILWTICO', start='2020-01-01', end='2022-01-01')

# Plot the data
plt.figure(figsize=(10, 6))
plt.plot(oil_price)
plt.ylabel('Oil Price')
plt.xlabel('Date')
plt.show()

