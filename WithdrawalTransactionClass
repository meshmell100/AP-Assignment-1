public class WithdrawalTransaction extends BaseTransaction {

    public WithdrawalTransaction(double amount, Calendar date, String transactionID) {
        super(amount, date, transactionID);
    }

    @Override
    public void apply(BankAccount ba) throws InsufficientFundsException {
        if (ba.getBalance() >= getAmount()) {
            ba.withdraw(getAmount());
            System.out.println("Withdrew " + getAmount() + " from account " + ba.getAccountNumber());
        } else {
            throw new InsufficientFundsException("Insufficient funds for withdrawal.");
        }
    }

    // Method to reverse a withdrawal transaction
    public boolean reverse(BankAccount ba) {
        ba.deposit(getAmount());  // Reverse by depositing the same amount back
        System.out.println("Reversed withdrawal of " + getAmount() + " from account " + ba.getAccountNumber());
        return true;
    }
}
