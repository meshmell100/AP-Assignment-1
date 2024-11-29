import java.util.Calendar;

public abstract class BaseTransaction implements TransactionInterface {
    private double amount;
    private Calendar date;
    private String transactionID;

    public BaseTransaction(double amount, Calendar date, String transactionID) {
        this.amount = amount;
        this.date = date;
        this.transactionID = transactionID;
    }

    @Override
    public double getAmount() {
        return this.amount;
    }

    @Override
    public Calendar getDate() {
        return this.date;
    }

    @Override
    public String getTransactionID() {
        return this.transactionID;
    }

    @Override
    public void printTransactionDetails() {
        System.out.println("Transaction ID: " + transactionID);
        System.out.println("Amount: " + amount);
        System.out.println("Date: " + date.getTime());
    }

    // Abstract method for applying a transaction on a bank account
    public abstract void apply(BankAccount ba);
}
