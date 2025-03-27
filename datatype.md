## 📝 Data Type Size Function in Python

### 📌 Problem Statement
Geek is learning a new programming language and needs help determining the size of fundamental data types. Given a data type as input, return its size in bytes. If the input data type is invalid, return `-1`.

### 🔍 Approach
1. **📖 Use a Dictionary**: Store predefined sizes for each data type in a dictionary.
2. **✅ Check Membership**: Verify if the given data type exists in the dictionary.
3. **📏 Return the Size**: If found, return the corresponding size; otherwise, return `-1`.
4. **⚠️ Handle Edge Cases**: Ensure that invalid inputs return `-1` instead of causing an error.

### 🐍 Python Implementation
```python
class Solution:
    def dataTypeSize(self, data_type):
        # Define a dictionary with sizes of common data types
        datatypes = {"Character": 1, "Integer": 4, "Long": 8, "Float": 5, "Double": 2}

        # Check if the input data type exists in the dictionary
        if data_type in datatypes:
            return datatypes[data_type]
        
        # Return -1 if the data type is not found
        return -1
```

### 💡 Explanation
- 📚 The dictionary `datatypes` holds the predefined sizes of different data types.
- 🔍 `if data_type in datatypes:` checks if the given input is a valid key in the dictionary.
- 🎯 If found, it returns the corresponding size.
- ❌ If not found, `return -1` ensures an invalid input is handled properly.

### 🏗 Example Usage
```python
sol = Solution()
print(sol.dataTypeSize("Character"))  # Output: 1
print(sol.dataTypeSize("Integer"))    # Output: 4
print(sol.dataTypeSize("String"))     # Output: -1 (Invalid input)
```

### 🔑 Key Takeaways
- **⚠️ Indentation Matters**: Ensure all return statements are correctly indented inside the function.
- **⚡ Dictionary Lookup**: Provides an efficient way to map data types to their sizes.
- **🛑 Error Handling**: Returns `-1` for invalid inputs to prevent unexpected errors.
