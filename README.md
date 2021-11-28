# python-homework
## Unit 2 | Homework Assignment: Automate Your Day Job with Python
#### Aidan J.M. Laird

### import data

import os
import csv 

### set variables

budget_data_csv = os.path.join("C:\\Users\\AJMLAIRD\\Desktop\\python-homework\\PyBank\\budget_data.csv")
with open(csvpath, newline='') as csvfile:
    csvreader = csv.reader(csvfile, delimiter=',')
    csv_header = next(csvreader)
    months = []
    revenue = []
    revenue_change = []
    monthly_change = []
    
              

### set total months 

    for row in csvreader:
        months.append(row[0])
        revenue.append(row[1])

    
### set total 

    revenue_int = map(int,revenue)
    total_revenue = (sum(revenue_int))

### set average change

    i = 0
    for i in range(len(revenue) - 1):
        profit_loss = int(revenue[i+1]) - int(revenue[i])
        
### set profit_loss

        revenue_change.append(profit_loss)
    Total = sum(revenue_change)
    
    #print(revenue_change)
    
    monthly_change = Total / len(revenue_change)
    
    
### set greatest increase in profit

    profit_increase = max(revenue_change)
    k = revenue_change.index(profit_increase)
    months_increase = months[k+1]
    
### set greatest decrease in profit

    profit_decrease = min(revenue_change)
    j = revenue_change.index(profit_decrease)
    month_decrease = month[j+1]


### print out the data 

print(f'Unit 2 | Homework Assignment: Automate Your Day Job with Python')
print(f'----------------------------'+'\n')
print(f'Financial Analysis'+'\n')
print(f'Copyright@ Aidan J.M. Laird')
print(f'Monash University FinTech Bootcamp November 2021')
print(f'----------------------------'+'\n')

print("Total Months: " + str(len(months)))
print("Total: $ " + str(total_revenue))     
print("Average Change: $" + str(monthly_change))
print(f"Greatest Increase in Profits: {month_increase} (${profit_increase})")
print(f"Greatest Decrease in Profits: {month_decrease} (${profit_decrease})")


