# python9
# Program 14: Check Leap Year
def is_leap_year(year):
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        return True
    else:
        return False

year = int(input("Enter a year to check if it's a leap year: "))
if is_leap_year(year):
    print(f"{year} is a leap year")
else:
    print(f"{year} is not a leap year")

# Program 15: Calculate GCD (Greatest Common Divisor)
def gcd(a, b):
    while b != 0:
        a, b = b, a % b
    return a

num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))
result = gcd(num1, num2)
print(f"The GCD of {num1} and {num2} is: {result}")

# Program 13: Bubble Sort
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]

# Example usage:
num_list = [int(x) for x in input("Enter numbers separated by space: ").split()]
bubble_sort(num_list)
print("Sorted array:", num_list)


# Program 12: Calculate Factorial
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n-1)

num = int(input("Enter a number to calculate its factorial: "))
fact = factorial(num)
print(f"The factorial of {num} is: {fact}")
