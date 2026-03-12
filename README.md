#!/bin/bash

# Simple Interest Calculator

echo "Simple Interest Calculator"
echo "=========================="

# Read principal amount
read -p "Enter principal amount: " principal

# Read rate of interest
read -p "Enter rate of interest (in %): " rate

# Read time period
read -p "Enter time period (in years): " time

# Calculate simple interest
interest=$(echo "scale=2; $principal * $rate * $time / 100" | bc)

# Display result
echo "=========================="
echo "Principal: $ $principal"
echo "Rate: $rate%"
echo "Time: $time years"
echo "Simple Interest: $ $interest"
echo "Total Amount: $ $(echo "scale=2; $principal + $interest" | bc)"
