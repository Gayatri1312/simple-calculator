# simple-calculator
develop a calculator program that performs basic arithmetic operation such addition and division by using c++

#include <iostream>

int main() {
    double num1, num2, result;
    char operation;

    // Input
    std::cout << "Enter first number: ";
    std::cin >> num1;

    std::cout << "Enter second number: ";
    std::cin >> num2;

    std::cout << "Choose operation (+, -, *, /): ";
    std::cin >> operation;

    // Perform calculation based on the chosen operation
    switch (operation) {
        case '+':
            result = num1 + num2;
            break;
        case '-':
            result = num1 - num2;
            break;
        case '*':
            result = num1 * num2;
            break;
        case '/':
            // Check for division by zero
            if (num2 != 0) {
                result = num1 / num2;
            } else {
                std::cout << "Error: Division by zero is not allowed." << std::endl;
                return 1;  // Exit with an error code
            }
            break;
        default:
            std::cout << "Invalid operation. Please choose +, -, *, or /." << std::endl;
            return 1;  // Exit with an error code
    }

    // Output the result
    std::cout << "Result: " << result << std::endl;

    return 0;
}
