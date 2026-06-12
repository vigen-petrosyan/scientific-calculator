# scientific-calculator
Scientific calculator built with C++ and OOP principles, supporting arithmetic, logarithmic, and trigonometric computations.


## Features
* **String Parsing:** Evaluates mathematical expressions passed as `std::string`.
* **Standard Arithmetic:** Supports addition, subtraction, multiplication, division, and modulo operations.
* **Mathematical Functions:** Includes support for trigonometry (sin, cos, tan, ctg) and logarithms (ln, log).
* **Operator Precedence:** Correctly applies the order of operations and respects nested parentheses ().
* **Unary Minus:** Handles negative numbers natively.
* **Error Handling:** Throws specific exceptions for invalid expressions and division by zero.
* **Built-in Unit Tests:** Includes automated tests using `cassert` to verify core functionality.

## Supported Operations & Functions
* **Arithmetic:** `+`, `-`, `*`, `/`, `%`
* **Trigonometry:** `sin()`, `cos()`, `tan()`, `ctg()`

* ## How It Works
The `Calculator` class processes expressions in three main stages:

* **Tokenization:** The `tokenize` method reads the raw string and splits it into logical components (numbers, operators, functions, and parentheses).
* **Infix to Postfix:** The `infixToPostfix` method uses a stack-based approach (Shunting-yard algorithm) to reorder the tokens based on operator precedence.
* **Evaluation:** The `CalculatePostfix` method iterates through the postfix tokens, applying operators and functions to a stack of numbers until the final result is computed.

## Error Handling
The class provides two custom exception types derived from `std::runtime_error`:

* **`Calculator::DivisionByZeroException`**: Thrown when attempting to divide or modulo by zero.
* **`Calculator::InvalidExpressionException`**: Thrown if the postfix syntax validation fails (e.g., mismatched parentheses or missing operands).
