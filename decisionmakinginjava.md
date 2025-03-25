## 🔢 Decision Making in Java

### 📌 Problem Statement
Given two integers, `n` and `m`, determine their relationship:
- Return **"lesser"** if `n < m`.
- Return **"equal"** if `n == m`.
- Return **"greater"** if `n > m`.

### 🔍 Approach
1. **🔢 Compare Values**: Use conditional statements to check the relation between `n` and `m`.
2. **🎯 Return the Result**: Based on the comparison, return the appropriate string.
3. **⚡ Efficient Logic**: Use `if-elif-else` structure to ensure proper execution.

### 🐍 Python Implementation
```python
class Solution:
    def compareNM(self, n: int, m: int) -> str:
        # Compare the two numbers
        if n < m:
            return "lesser"
        elif n > m:
            return "greater"
        
        return "equal"
```

### 💡 Explanation
- 🔍 The function checks whether `n` is less than, greater than, or equal to `m`.
- 🏆 Returns the respective string based on the condition met.

### 🏗 Example Usage
```python
sol = Solution()
print(sol.compareNM(4, 8))  # Output: "lesser"
print(sol.compareNM(8, 8))  # Output: "equal"
print(sol.compareNM(8, 4))  # Output: "greater"
```

### 🔑 Key Takeaways
- **📌 Conditional Statements**: `if-elif-else` provides clear decision-making logic.
- **🚀 Efficient Execution**: The function executes in constant time `O(1)`.
- **🔄 Simple Comparison**: Works efficiently for any integer values within constraints.
