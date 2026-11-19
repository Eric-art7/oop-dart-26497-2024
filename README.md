Leaving out a balance setter enforces encapsulation and data integrity:
• Prevents unauthorized changes: Without a setter, outside code cannot directly overwrite the balance to an arbitrary or fake amount (such as card.balance = 999999 or a negative number).
• Enforces business rules: Every change to _balance is forced to go through controlled methods (topUp() and pay()). This guarantees that all top-up limits and sufficient-funds checks are always respected.
