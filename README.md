# Writing Docstrings for Python Functions

Docstrings, short for *documentation strings*, are a specific type of comment that is used to describe Python functions, methods, and modules. 

They serve to explain what a piece of code does, what parameters it takes, and what it returns. Writing clear and concise docstrings is essential for making your code understandable to others (and yourself) who may need to use or modify it in the future.

## Why Use Docstrings?
- **Clarity**: 
Docstrings provide clarity about what a function does, its purpose, and how it should be used.
- **Documentation**:
They serve as documentation for developers who will use your code, including your future self.
- **Readability**:
Well-written docstrings improve the readability of your code, making it easier to understand and maintain.

## Anatomy of a Docstring
A docstring typically consists of three parts:

- **Description**: A brief description of what the function does.
- **Parameters**: Explanation of each parameter the function takes, including their types and meanings.
- **Return Value**: Description of what the function returns, including its type.

Here's an example of a simple function with a docstring:

```python
def factorial(n):
    """
    Calculates the factorial of a non-negative integer.

    Parameters:
        n (int): The non-negative integer.

    Returns:
        int: The factorial of the input integer.
    """
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)
```

### Writing Docstrings Step-by-Step
- **Start with Triple Quotes**: Docstrings are enclosed within triple quotes (""" """) immediately following the function or method definition.

- **Write a Description**: Begin with a brief description of what the function does. Keep it concise but informative.

- **Document Parameters**: List each parameter the function accepts, along with its data type (e.g. str, int, float, bool, etc.) and a brief description of its purpose. Use the format `param_name (param_type): Description`.

- **Document Return Value**: If the function returns a value, describe what it returns and its data type. Use the same format as the parameter, above.

- **Add Additional Information (Optional)**: You can include additional information such as exceptions the function may raise, side effects, or usage examples.


### Best Practices
- **Be Clear and Concise**: Make sure your docstring is easy to understand.
- **Use Proper Grammar and Punctuation**: Write in complete sentences and use proper grammar.
- **Follow a Consistent Format**: Stick to a consistent format across your codebase for better readability.
- **Update Docstrings as Needed**: Update docstrings when you modify the function's behavior or signature.

With well-written docstrings, your code becomes more self-explanatory and easier to maintain, especially as it grows in complexity.

### Examples of Docstrings

#### Function without Return Value
```python
def print_greeting(name):
    """
    Prints a greeting message for the given name.

    Parameters:
        name (str): The name of the person to greet.
    """
    print(f"Hello, {name}!")
```

#### Function with Several Parameters and Default Values
```python
def calculate_rectangle_area(length, width=1):
    """
    Calculates the area of a rectangle.

    Parameters:
        length (float): The length of the rectangle.
        width (float, optional): The width of the rectangle. Defaults to 1.

    Returns:
        float: The area of the rectangle.
    """
    return length * width
```

#### Function to Calculate the Square of a Number
```python
def square(number):
    """
    Calculates the square of a number.

    Parameters:
        number (int or float): The number to square.

    Returns:
        int or float: The square of the input number.
    """
    return number ** 2
```

#### Function to Check if a Number is Even
```python
def is_even(number):
    """
    Checks if a number is even.

    Parameters:
        number (int): The number to check.

    Returns:
        bool: True if the number is even, False otherwise.
    """
    return number % 2 == 0
```

#### Function to Find the Maximum of Two Numbers
```python
def find_max(num1, num2):
    """
    Finds the maximum of two numbers.

    Parameters:
        num1 (int or float): The first number.
        num2 (int or float): The second number.

    Returns:
        int or float: The maximum of the two input numbers.
    """
    return max(num1, num2)
```

#### Function to Convert Fahrenheit to Celsius
```python
def fahrenheit_to_celsius(fahrenheit):
    """
    Converts a temperature from Fahrenheit to Celsius.

    Parameters:
        fahrenheit (float): The temperature in Fahrenheit.

    Returns:
        float: The temperature in Celsius.
    """
    return (fahrenheit - 32) * 5 / 9
```

#### Function to Print a Greeting
In this function, note the use of the `greeting_type` parameter with several options for the user to select. The parameter options are detailed in the docstring, along with default values. Test cases below show its usage.
```python
def greet(name, greeting_type='casual'):
    """
    Greets a person with a specified type of greeting.

    Parameters:
        name (str): The name of the person to greet.
        greeting_type (str, optional): The type of greeting to use.
            Valid options: 'casual', 'formal', 'friendly'.
            Defaults to 'casual'.

    Returns:
        str: The greeting message.
    """
    if greeting_type == 'casual':
        return "Hey, " + name + "!"
    elif greeting_type == 'formal':
        return "Hello, " + name + ". How are you today?"
    elif greeting_type == 'friendly':
        return "Hi, " + name + "! It's good to see you!"

# Example usage:
print(greet('Alice'))  # Output: Hey, Alice!

print(greet('Bob', 'formal'))  # Output: Hello, Bob. How are you today?

print(greet('Charlie', 'friendly'))  # Output: Hi, Charlie! It's good to see you!
```