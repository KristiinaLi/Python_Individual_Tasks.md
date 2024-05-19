# Bank Deposit Challenge

Easy Level
Description: Create a program where the user can input deposits into a bank account. The program should use if-else statements, input(), int() and while True loop to keep track of deposits.

Instructions:

Welcome the user to the bank
Initiate balance = 0
Ask the user to input the amount of money they want to deposit.
Add the deposit amount to the total balance
Ask the user if they want to make another deposit or exit the bank.
If they choose to make another deposit, repeat the process (while True).
If not, print the total amount deposited and exit the bank.

```python
print('Welcome to The Bank')
balance =  0

while True: 
  action = input('For making a deposit, write "deposit". For exiting The Bank, write "exit".')
  if action == "exit":
    print('Thank you. Session completed. See you next time.')
    break
  elif action == "deposit":
    deposit = int(input('What is the amount of your deposit? '))
    balance = balance + deposit
    print(f'Your deposit {deposit} € has been added to your account. Your current balance is {balance} €.')
  else:
    print('Enter either "deposit" or "exit".')

```

Hard Level
Instructions:

Add bank withdrawal (if user wants to withdraw money the balance decreases)
If the balance becomes negative, withdrawal is not possible.
Add check balance optionality
Example for hard level:

print("\nWhat would you like to do?")
print("1. Deposit money")
print("2. Withdraw money")
print("3. Check balance")
print("4. Exit")

```python
print('Welcome to The Bank')
balance =  0

actions = {1 : 'Deposit money',
           2 : 'Withdraw money',
           3 : 'Check balance',
           4 : 'Exit'}

while True: 
  action = input('\n What would you like to do? Enter \n 1 to Deposit money \n 2 to Withdraw money \n 3 to Check balance \n 4 to Exit \n')
  action = int(action)
  if action == 4:
    print(actions[4])
    print('Thank you. Session completed. See you next time.')
    break
  elif action == 1:
    print(actions[1])
    deposit = int(input('What is the amount of your deposit? '))
    balance = balance + deposit
    print(f'Your deposit {deposit} € has been added to your account. Your current balance is {balance} €.')
  elif action == 2:
    print(actions[2])
    withdrawal = int(input('How much money would you like to withdraw? '))
    if withdrawal > balance:
      print(f'It is not currently possible to withdraw {withdrawal} €, as your balance is {balance} €.')
    else:
      balance = balance - withdrawal
      print(f'{withdrawal} € taken from your account. Your remaining balance is {balance} €.')
  elif action == 3:
    print(actions[3])
    print(f'You have {balance} € on your account.')
  else:
    print('Enter which action you would like to proceed with.')
```
