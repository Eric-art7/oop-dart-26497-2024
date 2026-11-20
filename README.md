part 1:
Leaving out a balance setter enforces encapsulation and data integrity:
• Prevents unauthorized changes: Without a setter, outside code cannot directly overwrite the balance to an arbitrary or fake amount (such as card.balance = 999999 or a negative number).
• Enforces business rules: Every change to _balance is forced to go through controlled methods (topUp() and pay()). This guarantees that all top-up limits and sufficient-funds checks are always respected.
part 2:
What ~/ does:
The ~/ operator performs integer division (truncating division). It divides two numbers and drops the decimal part, returning a whole integer (int).
Example & Difference:
• 237 * 17 / 100 outputs 40.29 (standard division / always returns a double with decimals).
• 237 * 17 ~/ 100 outputs 40 (integer division ~/ removes .29 and returns an int).
