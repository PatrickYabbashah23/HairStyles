# HairStyles
#This Program goes through multiple list of data that have been collected over the weeks

#List for types of hairstyles

hairstyles = ["bouffant", "pixie", "dreadlocks", "crew", "bowl", "bob", "mohawk", "flattop"]

#List for prices of each hairstyle

prices = [30, 25, 40, 20, 20, 35, 50, 35]

#List of the number of hairstyles that were purchahed last week

last_week = [2, 3, 5, 8, 4, 4, 6, 2]

#All hairstyle prices added together

total_price = 0

#Adds each hairstyle price to the variable "total_price" 

for price in prices:
  total_price += price
  
#Average price for hairstyles

average_price = total_price / len(prices)
  
#Prints out the average cost of the hairstyles  

print("Average Haircut Prices: " + str(average_price))  
  
#A new list that cuts all hairstyle prices by $5

new_prices = [price - 5 for price in prices]
print(new_prices)

#Total revenue of sales from hairstyles

total_revenue = 0

#Adds the prices of hairstyles along with the number of hairstyles that was purchased last week to calculate the total revenue 

for i in range(len(hairstyles)):
  total_revenue += prices[i] * last_week[i] 
print(total_revenue) 

#Finds the daily average revenue

average_daily_revenue = total_revenue / 7
print("Average Daily Revenue: " + str(average_daily_revenue))

#Creates a new list of hairstyles that are under $30

cuts_under_30 = [hairstyles[i] for i in range(len(hairstyles)) if new_prices[i] < 30]
print(cuts_under_30)  

