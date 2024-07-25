# Wallet Manager
 If you want the easiest way to manage your money, with recommendations for investing/donating. Try Wallet Manager

# First, the program will ask user how much does he have. And the application will output if user has money or not
--------------------------------------------------------------------------------------------------------------------
        #part 1
      total = int(input("Enter the amount you want to manage (salary, advances, etc.): "))
     
      print("You have", total, "in your wallet")

            #part 2
            
            if total <= 0:
          print("You have no money left in your wallet.")
      else:
          print("You have", total, "left in your wallet.")
 
Then, when user paid Payed sum of money the user will enter how much did he pay
--------------------------------------------------------------------------------------------------------------------
     while total > 0:
         pay = int(input("How much did you pay? "))

Afer that, when user paid Payed sum of money the user will enter how much did he pay
--------------------------------------------------------------------------------------------------------------------
    if pay <= total:
        total -= pay
        print("After payment, you have", total, "left in your wallet")



Finally, The program will recommend the user according to his budget in the wallet (invest, donate, save it). If his budget is not enough, it informs him that the current budget is low, so he cannot pay at this time
--------------------------------------------------------------------------------------------------------------------

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

        
# Note that the application will automatically ask the user if there are other payments, so the user chooses yes/no
--------------------------------------------------------------------------------------------------------------------

     more_payments = input("Do you want to enter another payment? (yes/no): ").strip().lower()
         if more_payments != 'yes':
             break
