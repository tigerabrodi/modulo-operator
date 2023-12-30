# Modulo Operator in JavaScript

Modulo operator is used to get the remainder of a division operation.

For example, 5 % 2 = 1, because 5 divided by 2 leaves a remainder of 1. Or in other words, there are 2 full 2s in 5, and 1 left over.

1. `10 % 4` equals `2` because when you divide 10 by 4, the quotient is 2 and the remainder is 2. The modulo operator returns this remainder.

2. `10 % 10` equals `0` because 10 divides evenly into 10 with no remainder.

3. `4 % 10` equals `4` because 4 divided by 10 doesn't fully complete a single division (since 4 is less than 10), leaving 4 as the remainder.

A key point to understand is that the modulo operation always returns the remainder of the division of the first number by the second number. When the first number is smaller than the second (as in `4 % 10`), the remainder is just the first number itself, since it doesn't reach the threshold to be divided even once by the second number.

## Common use cases

1. **Cycling Through Arrays or Lists (Circular Data Structures)**

   - **Use Case**: When you have a circular list (like a carousel) and want to cycle through elements repeatedly.
   - **Example**: If you have an array of 5 elements, and you're at index 4, `nextIndex = (currentIndex + 1) % arrayLength` will bring you back to index 0.

2. **Implementing Wrap-around Logic**

   - **Use Case**: Useful in games or simulations where moving off one edge of the screen or grid should "wrap around" to the other side.
   - **Example**: On a grid of width `W`, a character at `x` moving right by `dx` steps would end up at `(x + dx) % W`.

3. **Determining Even/Odd Numbers**

   - **Use Case**: Quickly check if a number is even or odd.
   - **Example**: `if (number % 2 === 0)` is true for even numbers.

4. **Finding Divisibility**

   - **Use Case**: To check if a number is divisible by another (useful in filtering or conditional logic).
   - **Example**: `if (number % divisor === 0)` means `number` is divisible by `divisor`.

5. **Hash Table Indexing**

   - **Use Case**: In hash tables, to convert a large hash code into a smaller index within the table's range.
   - **Example**: `index = hashCode % tableSize`.

6. **Time Calculations**

   - **Use Case**: For operations with time, like converting seconds to hours, minutes, and seconds.
   - **Example**: `seconds = totalSeconds % 60`.

7. **Animation and Graphics**

   - **Use Case**: In animations or graphics, for creating repeating patterns or movements.
   - **Example**: Cycling through frames of an animation or positions of a sprite.

8. **Distributing Resources Equally**

   - **Use Case**: In load balancing or distribution problems, to equally distribute items or tasks.
   - **Example**: Assigning `taskNumber % numberOfWorkers` to distribute tasks among workers.

9. **Creating Periodic Functions**

   - **Use Case**: In signal processing or generating waveforms, to create periodic functions.
   - **Example**: Generating a square wave with `if (time % period < period / 2)`.

10. **Constraining Values Within a Range**

- **Use Case**: To limit a value within a certain range, especially when the value increases continuously.
- **Example**: Keeping an angle within 0-360 degrees range: `angle % 360`.
