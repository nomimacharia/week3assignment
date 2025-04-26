def calculate_discount(price, discount_percent):
    if discount_percent >= 20:
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
    else:
        final_price = price
    return final_price

def get_user_input():
    original_price = float(input("Enter the original price of the item: "))
    discount_percent = int(input("Enter the discount percentage: "))
    final_price = calculate_discount(original_price, discount_percent)
    if final_price == original_price:
        print("No discount was applied, so the final price is:", original_price)
    else:
        print("The final price after applying the discount is:", final_price)
