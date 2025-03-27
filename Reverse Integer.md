# Reverse Integer - Explanation

## Code:
```python
class Solution:
    def reverse(self, x: int) -> int:
        str_num = str(x)  # Step 1: Convert the integer 'x' to a string
        
        if str_num[0] == "-":  
            # Step 2: If 'x' is negative, ignore the first character ('-'), 
            # reverse the remaining digits, and convert back to integer with a negative sign
            output = -int(str_num[1:][::-1])  
        else:
            # Step 3: If 'x' is positive, reverse the string and convert back to integer
            output = int(str_num[::-1])  

        # Step 4: Check if the reversed integer is within the 32-bit signed integer range
        if output < -2**31 or output > 2**31 - 1:
            return 0  # If out of bounds, return 0
        else:
            return output  # Otherwise, return the valid reversed integer
```

## **Time Complexity:**
- **O(n)** where **n** is the number of digits in `x`, because string reversal takes **O(n)**.

## **Space Complexity:**
- **O(1)** because only a few variables are used, and no extra space is allocated proportional to the input size.

---

### **Example Walkthrough**

#### **Example 1:**
**Input:** `x = 123`  
**Processing:**  
- Convert `123` to string `"123"`
- Reverse it to `"321"`
- Convert back to integer `321`
- Since `321` is within the valid range, return `321`

**Output:** `321`

---

#### **Example 2:**
**Input:** `x = -123`  
**Processing:**  
- Convert `-123` to string `"-123"`
- Reverse only `"123"` → `"321"`
- Add back `"-"` to get `-321`
- Since `-321` is within the valid range, return `-321`

**Output:** `-321`

---

#### **Example 3:**
**Input:** `x = 120`  
**Processing:**  
- Convert `120` to string `"120"`
- Reverse it to `"021"`
- Convert back to integer `21`
- Since `21` is within the valid range, return `21`

**Output:** `21`

---

#### **Edge Case:**
**Input:** `x = 1534236469`  
**Processing:**  
- Convert `1534236469` to string `"1534236469"`
- Reverse it to `"9646324351"`
- Convert back to integer `9646324351`
- Since `9646324351` is **out of 32-bit range**, return `0`

**Output:** `0`
