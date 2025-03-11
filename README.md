1.Here’s the function that calculates the final price after applying a discount only if it's 20% or higher:

python
Copy
def calculate_discount(price, discount_percent):
    """
    Calculates the final price after applying a discount if it's 20% or higher.
    
    Parameters:
    price (float): The original price of the item.
    discount_percent (float): The discount percentage.
    
    Returns:
    float: The final price after applying the discount or the original price.
    """
    if discount_percent >= 20:
        discount_amount = (discount_percent / 100) * price
        final_price = price - discount_amount
        return final_price
    else:
        return price  # Return original price if discount is less than 20%

# Example usage:
original_price = 100
discount = 25
final_price = calculate_discount(original_price, discount)
print(f"Final price: ${final_price:.2f}")  # Output: Final price: $75.00
How It Works:
The function takes two parameters:
price: The original price of the item.
discount_percent: The percentage of the discount.
If the discount percentage is 20% or higher, it:
Calculates the discount amount.
Subtracts it from the original price.
Returns the final price.
If the discount is less than 20%, it returns the original price.


2:Here’s a complete Python program that:

Uses the calculate_discount function.
Prompts the user for the original price and discount percentage.
Prints the final price after applying the discount (if applicable).
python
Copy
def calculate_discount(price, discount_percent):
    """
    Calculates the final price after applying a discount if it's 20% or higher.

    Parameters:
    price (float): The original price of the item.
    discount_percent (float): The discount percentage.

    Returns:
    float: The final price after applying the discount or the original price.
    """
    if discount_percent >= 20:
        discount_amount = (discount_percent / 100) * price
        final_price = price - discount_amount
        return final_price
    else:
        return price  # Return original price if discount is less than 20%

# Prompt the user for input
try:
    price = float(input("Enter the original price: "))
    discount_percent = float(input("Enter the discount percentage: "))

    # Calculate the final price
    final_price = calculate_discount(price, discount_percent)

    # Display the result
    if discount_percent >= 20:
        print(f"Discount applied! Final price: ${final_price:.2f}")
    else:
        print(f"No discount applied. Final price: ${final_price:.2f}")

except ValueError:
    print("Invalid input! Please enter numeric values for price and discount.")
How It Works:
Defines calculate_discount(price, discount_percent)
Applies the discount if ≥ 20%, otherwise returns the original price.
Prompts the user for the price and discount percentage.
Handles invalid input (non-numeric values).
Displays the correct final price, indicating if a discount was applied.
Example Runs:
✅ With Discount Applied:
yaml
Copy
Enter the original price: 200
Enter the discount percentage: 25
Discount applied! Final price: $150.00
❌ No Discount Applied (Less than 20%):
yaml
Copy
Enter the original price: 100
Enter the discount percentage: 10
No discount applied. Final price: $100.00
⚠️ Invalid Input Handling:
pgsql
Copy
Enter the original price: abc
Invalid input! Please enter numeric values for price and discount.
