#include <iostream>
using namespace std;

float add(float x, float y) {
    return x + y;
}

float subtract(float x, float y) {
    return x - y;
}

float multiply(float x, float y) {
    return x * y;
}

float divide(float x, float y) {
    if (y != 0)
        return x / y;
    else {
        cout << "Error! Division by zero." << endl;
        return 0;
    }
}

int main() {
    float num1, num2;
    int choice;

    cout << "Select operation:" << endl;
    cout << "1. Addition" << endl;
    cout << "2. Subtraction" << endl;
    cout << "3. Multiplication" << endl;
    cout << "4. Division" << endl;

    cout << "Enter choice (1/2/3/4): ";
    cin >> choice;

    if (choice >= 1 && choice <= 4) {
        cout << "Enter first number: ";
        cin >> num1;
        cout << "Enter second number: ";
        cin >> num2;

        switch(choice) {
            case 1:
                cout << "The result is: " << add(num1, num2) << endl;
                break;
            case 2:
                cout << "The result is: " << subtract(num1, num2) << endl;
                break;
            case 3:
                cout << "The result is: " << multiply(num1, num2) << endl;
                break;
            case 4:
                cout << "The result is: " << divide(num1, num2) << endl;
                break;
        }
    } else {
        cout << "Invalid input" << endl;
    }

    return 0;
}
