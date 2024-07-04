# Bank Account and Transaction Classes

This project demonstrates the application of object-oriented programming to create two classes: `BankAccount` and `Transaction`. These classes are used to represent a bank account and its associated transactions.

## Classes

### Transaction Class

The `Transaction` class represents a single transaction in a bank account.

#### Fields

- `date`: The date of the transaction (automatically set to the current date).
- `amount`: The amount of the transaction. Positive amounts are money going into the account (deposit, refund). Negative amounts are money coming out of the account (a charge or debit).
- `payee`: The description or payee on the transaction.

#### Constructor

```javascript
constructor(amount, payee);
```

.amount: The amount on the transaction.

.payee: The payee or description on the transaction.
BankAccount Class

The BankAccount class represents a bank account.

Fields
.accountNumber: String representing the account number.
.owner: String representing the owner of the account.
.transactions: An array of transactions representing the history of all transactions associated with this account.

Constructor

constructor(accountNumber, owner)

.accountNumber: The account number.
.owner: The name of the person who owns this account.

Methods

.balance(): Computes and returns the current balance by summing up the amounts of all transactions.

.deposit(amt): Creates a new transaction for the deposit amount and adds it to the transactions array. It should not allow depositing a negative amount.

.charge(payee, amt): Creates a new transaction for the payee and amount and adds it to the transactions array. It should not allow charges that would make the balance dip below 0.
Usage
Example

const account = new BankAccount('123456', 'John Doe');
account.deposit(100);
account.charge('Grocery Store', 25);
console.log(account.balance()); // 75
account.charge('Gas Station', 50);
console.log(account.balance()); // 25
account.charge('Electronics Store', 30); // Insufficient funds for this charge
console.log(account.balance()); // 25

Running the Code
1:Ensure you have Node.js installed.
2:Create a file named main.js and paste the example usage code above.
3:Run the file using the command:
node main.js

Notes
.The balance method calculates the balance by summing the amounts in the transactions array.
.The deposit method ensures that only positive amounts can be deposited.
.The charge method ensures that the balance cannot go below 0 due to a charge.
