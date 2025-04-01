import matplotlib.pyplot as plt

# Convert 'Date' column to datetime format and sort data
df['Date'] = pd.to_datetime(df['Date'])
df = df.sort_values(by='Date')

# Plot Closing Price Trend
plt.figure(figsize=(12, 6))
plt.plot(df['Date'], df['Close'], label='Closing Price', color='blue', linewidth=2)
plt.xlabel('Date')
plt.ylabel('Closing Price')
plt.title('Stock Closing Price Trend')
plt.legend()
plt.grid(True)
plt.show()
