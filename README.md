This is homework 2 - Python

 

\# From the pathlib library, import the main class Path

from pathlib import Path

import csv

\# Check the current directory where the Python program is executing from

print(f"Current Working Directory: {Path.cwd()}")

\# Set the path using Pathlib \# Open the file in "read" mode ('r') and

\# store the contents in the variable 'file'

input_path = Path('../PyBank/budget_data.csv')

with open (input_path, 'r') as file:

    text = file.read()

print (text)

 

Output exceeds the size limit. Open the full output data in a text editor

Current Working Directory: C:\\Users\\jimp\\Homework\\python-homework\\PyBank
Date,Profit/Losses Jan-10,867884 Feb-10,984655 Mar-10,322013 Apr-10,-69417
May-10,310503 Jun-10,522857 Jul-10,1033096 Aug-10,604885 Sep-10,-216386
Oct-10,477532 Nov-10,893810 Dec-10,-80353 Jan-11,779806 Feb-11,-335203
Mar-11,697845 Apr-11,793163 May-11,485070 Jun-11,584122 Jul-11,62729
Aug-11,668179 Sep-11,899906 Oct-11,834719 Nov-11,132003

Nov-16,795914 Dec-16,60988 Jan-17,138230 Feb-17,671099

 

\# Assessing data on profit figures per month from 2010 - 2017.

\# Need to sum the number of months, and the net resulting Profit and loss
figure for those months

\# Formulas needed:  averages of changes in Profit and Losses over the full
period

\# greatest increase in profits date and amount over full period

\# greatest decrease in profits - date and amount over full period

\# Initialize the metric variables

count = 0

total = 0

average = 0

maximum = 0

minimum = 0

\#read in all text in the file as string

text = file.read()

    \# Parse the file line by line -  splitting the string by the newline
character '\\n'

for line in text.split('\\n'):

        \# Convert the number in the text file from string to int

        number = int(line)

        \# Sum the total and count of the numbers in the text file

        profit_total += number

        month_count += 1

\# Print out profit_total and month_count

print(f"profit_total: {profit_total}")

print(f"month_count: {month_count}")

print("-----------------------")

\# Calculate the average of profit/loss changes (including date and amount over
the entire period)

change_average = profit_total / month_count

print(f"change_average: {change_average}")

\# Set output file name

output_path = 'output.txt'

\# Open the output path as a file object

with open(output_path, 'w') as file:

    \# Write daily_average to the output file, convert to string

    file.write(f"There were {customer_total} customers over the course of
{day_count} days.\\n")

    file.write(f"The average daily customer traffic is {daily_average} customers
per day.")

\# Calculate the average

average = round(total / count, 2)

  
  


 

 
