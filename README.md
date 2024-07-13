# BMI Calculator Project

## Table of Contents
1. [Project Overview](#Project-Overview)
2. [Tools](#Tools)
3. [Code](#Code)
4. [Limitations](#Limitations)
5. [References](#References)

## Project Overview
This project involves creating a BMI (Body Mass Index) calculator using Python. The purpose of the project is to develop a simple tool that calculates BMI based on user inputs and classifies the result into different health categories.

## Tools
- Python
- Jupyter Notebook

## Code
```python
# Defining the BMI calculation formula
def calculate_bmi(weight, height):
    return (weight * 703) / (height * height)

# Taking user input for name, weight, and height
name = input('Enter your name: ')
weight = int(input('Enter your weight in pounds: '))
height = int(input('Enter your height in inches: '))

# Calculating BMI using the formula
BMI = calculate_bmi(weight, height)

# Ensuring the first name will always be capitalized regardless of input
cap_name = name.capitalize()

# Print the BMI value
print(f"{cap_name}'s BMI is: {BMI:.1f}")

# Determine the BMI category and print the result
if BMI > 0:
    if BMI < 18.5:
        print(f"{cap_name} is Underweight.")
    elif BMI <= 24.9:
        print(f"{cap_name} is Normal Weight.")
    elif BMI <= 29.9:
        print(f"{cap_name} is Overweight.")
    elif BMI <= 34.9:
        print(f"{cap_name} is Obese and has High health risks.")
    elif BMI <= 39.9:
        print(f"{cap_name} is Severely Obese and has Very High health risks.")
    elif BMI >= 40:
        print(f"{cap_name} is Morbidly Obese and has Extremely High health risks.")
else:
    print('Enter valid input')
``` 

## Limitations
- The calculator relies solely on BMI and does not consider other health indicators such as body fat percentage, muscle mass, etc.

## References
- Centers for Disease Control and Prevention (CDC): [BMI Information](https://www.cdc.gov/healthyweight/assessing/bmi/index.html)
