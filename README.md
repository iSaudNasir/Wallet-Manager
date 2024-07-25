# Wallet-Manager
 If you want the easiest way to manage your money, with recommendations for investing/donating. Try Wallet Manager

 
total = int(input("Enter the amount you want to manage (salary, advances, etc.): "))

print("You have", total, "in your wallet")

while total > 0:
    pay = int(input("How much did you pay? "))

    if pay <= total:
        total -= pay
        print("After payment, you have", total, "left in your wallet")

        
        if total > 1000:
            print("Consider investing some of your remaining balance.")
        elif total > 500:
            print("Consider saving a portion of your remaining balance.")
        elif total > 100:
            print("You might want to donate a small amount to charity.")
        else:
            print("Consider saving or managing your remaining balance wisely.")
    else:
        print("You cannot pay more than what you have. Please enter a valid amount.")

    more_payments = input("Do you want to enter another payment? (yes/no): ").strip().lower()
    if more_payments != 'yes':
        break

if total <= 0:
    print("You have no money left in your wallet.")
else:
    print("You have", total, "left in your wallet.")
