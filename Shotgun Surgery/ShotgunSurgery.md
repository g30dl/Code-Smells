<h1><strong>Shotgun Surgery</strong></h1>


Shotgun surgery is a change that requires code to be multiple pieces of code to be changed.

Example:
```java
public class Account {
    private double amount;

    public Account(double amount) {
        this.amount = amount;
        // Initialize account with the given amount
    }

    public void debit(double debitAmount) {
        if (this.amount <= 1000) {
            throw new IllegalArgumentException("Minimum balance should be over 1000");
        }
        // Subtract the debit amount from the account balance
    }

    public void transfer(Account to, double transferAmount) {
        if (this.amount <= 1000) {
            throw new IllegalArgumentException("Minimum balance should be over 1000");
        }
        // Transfer the specified amount from one account to another
    }
}

```
adapted from: https://luzkan.github.io/smells/refused-bequest
