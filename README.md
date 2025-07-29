# LC7-Reverse-Integer
LeetCode7 – Reverse Integer  Given a 32-bit signed integer, the task is to reverse its digits. If the reversed integer overflows the 32-bit signed range, return 0. This problem focuses on the careful handling of integer overflow, digit manipulation without string conversion, and efficiently managing signs for both positive and negative integers.

# 🚀 Reverse Integer — LeetCode Problem #7

## 🧩 Problem Statement

Given a signed 32-bit integer `x`, the task is to reverse its digits and return the reversed number. However, if reversing `x` causes the value to go outside the signed 32-bit integer range (`[-2^31, 2^31 - 1]`), then the function should return 0.

> 💡 The environment **does not allow storing 64-bit integers**, so extra care must be taken to avoid overflow during calculations.

### 🔍 Example

| Input    | Output |
|----------|--------|
| x = 123  | 321    |
| x = -123 | -321   |
| x = 120  | 21     |

---

## 🧠 Approach & Logic

To solve this problem, I used a **mathematical digit manipulation technique** rather than converting the number to a string. Here's a breakdown of the approach:

### ✅ Step-by-step Logic:

1. **Handle Negativity:**
   - Store the original sign of the input number.
   - If the number is negative, convert it to positive for ease of processing and reverse it later.

2. **Reverse Using Modulus & Division:**
   - Extract the last digit of the number using `x % 10`.
   - Append this digit to the result using: `res = res * 10 + last_digit`.
   - Shrink the original number by dividing it by 10 using integer division.

3. **Overflow Handling:**
   - Check if the reversed number goes beyond the limits of a 32-bit signed integer.
   - If so, return `0` as instructed in the problem.

4. **Restore Sign:**
   - If the original number was negative, make the final result negative again.

---

### LeetCode Submission Screenshot
![Accepted Screenshot](./screenshot/lc7-accepted-code.png)
