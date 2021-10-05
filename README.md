# Carly-s-Clippers

# This project is to go through the lists of data that have been collected in the past couple of weeks.

hairstyles = ["bouffant", "pixie", "dreadlocks", "crew", "bowl", "bob", "mohawk", "flattop"]

prices = [30, 25, 40, 20, 20, 35, 50, 35]

last_week = [2, 3, 5, 8, 4, 4, 6, 2]

# The following codes will calculate the prices and cuts of prices list

# create variable total_price to set it to 0 that will sum up all the prices of haircuts.
total_price = 0

# loop through prices list and add each price to the variable total_price.
for price in prices:
  total_price += price

# get the average price of total price by prices
average_price = total_price/len(prices)

# print the output of the average price
print("Average Haircut Price: $" + str(average_price))

# use list comprehension to make a new prices that is minus by 5
new_prices = [p-5 for p in prices]

# print new prices output
print(new_prices)

# The following codes are to calculate the revenue.

# create total revenue to document how much was brought in last week.
total_revenue = 0

# looping steps:
for i in range(len(hairstyles)):
  total_revenue += prices[i] * last_week[i]

# print total revenue
print("Total Revenue: $" + str(total_revenue))

# calculate the average daily revenue by dividing 7 and print output.
average_daily_revenue = total_revenue/7
print(average_daily_revenue)

# reduce price by 30 to bring in more customers by advertising all haircuts
cuts_under_30 = [hairstyles[i] for i in range(len(new_prices) - 1) if new_prices[i] < 30]

# print cuts under 30
print(cuts_under_30)
