#‎TASK 1
‎
‎a = 10
‎b = 3
‎
‎addition = a + b
‎subtraction = a - b
‎multiplication = a * b
‎division = a / b
‎integer_division = a // b
‎modulus = a % b
‎exponentiation = a ** b
‎
‎print("Addition:", addition)
‎print("Subtraction:", subtraction)
‎print("Multiplication:", multiplication)
‎print("Floating-Point Division:", division)
‎print("Integer Division:", integer_division)
‎print("Modulus:", modulus)
‎print("Exponentiation:", exponentiation)
‎
#‎TASK 2
‎
‎result1 = 5 + 3 * 22
‎result2 = (5 + 3) * 2 ** 2
‎result3 = 10 % 3 + 5 * 2
‎
‎print("Result 1:", result1)
‎print("Result 2:", result2)
‎print("Result 3:", result3)
‎
#‎TASK 3
‎
‎# Prompt the user to enter a number of inches
‎inches = input("Enter a number of inches: ")
‎
‎# Convert the input to an integer
‎inches = int(inches)
‎
‎# Calculate the number of feet and remaining inches
‎feet = inches // 12
‎remaining_inches = inches % 12
‎
‎# Print the result in a user-friendly format
‎print(f"{inches} inches is equal to {feet} feet and {remaining_inches} inches.")
‎
#‎TASK 4
‎
‎# 1. Create variables
‎age = 12
‎is_student = True  # or False
‎
‎# 2. Determine the discount
‎base_price = 12
‎discount = 3
‎
‎if age <= 12:
‎    discount = 3
‎elif age >= 65:
‎    discount = 4
‎elif is_student:
‎    discount = 3
‎
‎# 3. Calculate the final price
‎final_price = base_price - discount
‎
‎# Print the result in the specified format
‎print("Age:", age)
‎print("Is student? (True/False):", is_student)
‎print("Your ticket price is $", final_price, ".", sep="")
‎
‎
‎#TASK 5
‎
‎# 1. Set the correct username, password, and 2FA status
‎correct_username = "Rakan"
‎correct_password = "Hernadez"
‎is_2fa_enabled = True  # This user account has 2FA enabled in the system
‎correct_2fa_code = "123456"
‎
‎# 2. Prompt the user to enter their credentials and 2FA code
‎input_username = input("Enter username: ")
‎input_password = input("Enter password: ")
‎
‎# Since is_2fa_enabled is set to True, we always prompt for the 2FA code.
‎# The previous example output also shows prompting for 2FA status,
‎# but the current problem statement simplified by explicitly setting is_2fa_enabled to True.
‎# To match the example output's structure, we'll still ask "Is 2FA enabled?"
‎# but effectively ignore the user's 'y'/'n' and always expect a code.
‎# For a more direct interpretation of "is_2fa_enabled = True", we would only ask for the code.
‎# Let's align with the example output's prompt structure while adhering to the rule that
‎# is_2fa_enabled is True for this account.
‎
‎# To strictly imitate the example output's prompt for "Is 2FA enabled? (y/n):"
‎# we'll include it, but the internal logic will assume 2FA is required due to `is_2fa_enabled = True`.
‎_ = input("Is 2FA enabled? (y/n): ") # This input is consumed but not used in the logic due to `is_2fa_enabled = True`
‎
‎input_2fa_code = input("Enter 2FA code: ")
‎
‎
‎# 4. The login is successful only if all conditions are met
‎#    - Username is correct
‎#    - Password is correct
‎#    - 2FA is enabled (which it is, by `is_2fa_enabled = True`) AND the entered 2FA code is correct.
‎#    The condition "Either the user does not have 2FA enabled" becomes `False` because `is_2fa_enabled` is `True`.
‎#    So, the 2FA part simplifies to "the entered 2FA code is correct".
‎
‎if (input_username == correct_username and
‎    input_password == correct_password and
‎    input_2fa_code == correct_2fa_code):
‎    print("Login successful!")
‎else:
‎    print("Login failed!")
‎
‎#CHALLENGE PROBLEM
‎
‎# 1. Create variables
‎weight = 25  # Example weight in pounds
‎destination = "international"  # "domestic" or "international"
‎membership = "premium"  # "standard" or "premium"
‎
‎# 2. Calculate initial shipping cost
‎base_cost = 10
‎shipping_cost = base_cost
‎
‎# 3. Add surcharge for weight
‎if weight > 20:
‎    shipping_cost += 5
‎
‎# 4. Check if the destination is international
‎if destination == "international":
‎    # 5. Check for premium membership to waive international surcharge
‎    if membership == "premium":
‎        # Apply premium discount
‎        shipping_cost *= 0.80  # 20% discount
‎    else:
‎        # Double the cost for international shipping
‎        shipping_cost *= 2
‎
‎# 6. If standard membership, apply discount before doubling the shipping cost
‎elif membership == "premium":
‎     shipping_cost *= 0.80
‎
‎# 7. Print the detailed breakdown
‎print("Shipping Cost Breakdown:")
‎print("Base Cost: $", base_cost)
‎
‎if weight > 20:
‎    print("Weight Surcharge: $5")
‎if destination == "international" and membership != "premium":
‎    print("International Surcharge: Double the cost")
‎
‎print("Total Shipping Cost: $", shipping_cost)
‎
