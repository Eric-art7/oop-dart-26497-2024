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

 output 
 Error: name too short
 Owner: semana munezero eric  | Balance: 25000 RWF
 Owner: semana munezero eric | Balance: 25000 RWF
 Error: top-up must be 500 to 50000 RWF
 2
 Paid 3000 RWF
 Owner: semana munezero eric | Balance: 21000 RWF
 Student discount: 400 RWF
 Paid 1600 RWF
 Owner: semana munezero eric  | Balance: 18400 RWF
 Student card: 20% off
  
 Exited.

part 4:
 
  
| Bug            | The line                           | Why it is wrong (your words)                  | Your fix                                 |
| :------------- | :--------------------------------- | :-------------------------------------------- | :--------------------------------------- |
| 1              | `String _brand;` `int _battery;`   | Fields need starting values in Dart.          | Set `_brand = '';` and `_battery = 0;`.  |
| 2              | `SmartPhone(...) {`                | Does not pass values to parent `Phone`.       | Add `: super(brand, battery)`.           |
| 3              | `@override`                        | `Phone` has no `restart()` method.            | Remove `@override`.                      |
| 4              | `p.battery = 100;`                 | `Phone` has no setter for `battery`.          | Add `set battery` (accepting 0–100).     |
| 5              | `print(p.battery());`              | `battery` is a getter, not a method.          | Remove `()`: `print(p.battery);`.        |
| **Not a bug**  | `Phone p = new Phone(...);`        | `new` is optional in Dart, so it still works. | (none)                                   |


part 5:

 The code will print:
 1
 5
 Why:
 • a starts at 0, adds 1, and ignores -5 because the setter blocks negative numbers. So a prints 1.
 • b adds 2 each time add() runs (2 + 2 = 4), then adds 1 more (4 + 1 = 5). So b prints 5.

 
 Actual Output:
 1
 5 
  but to be honest some to understand it difcult due to that the language is new to me and honstly my prediction i would be wrong but with ai by searching 
  try to under stand is how i worked with it not full my side !!!!.