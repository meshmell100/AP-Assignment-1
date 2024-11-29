import java.util.Calendar;

public class Main {
    public static void main(String[] args) {
        BankAccount account = new BankAccount("12345", 500.0);

        // Create a DepositTransaction
        Calendar depositDate = Calendar.getInstance();
        DepositTransaction deposit = new DepositTransaction(200.0, depositDate, "D123");
        deposit.printTransactionDetails();
        deposit.apply(account);  // Apply deposit transaction

        // Create a WithdrawalTransaction
        Calendar withdrawDate = Calendar.getInstance();
        WithdrawalTransaction withdrawal = new WithdrawalTransaction(100.0, withdrawDate, "W123");
        withdrawal.printTransactionDetails();
        try {
            withdrawal.apply(account);  // Apply withdrawal transaction
        } catch (InsufficientFundsException e) {
            System.out.println(e.getMessage());
        }

        // Reverse the withdrawal
        withdrawal.reverse(account);  // Reverse the transaction
    }
}
