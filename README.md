#include <stdio.h>

// Sum of the numbers
void sum(float a, float b) {
    printf("Result: %f\n", a + b);
}

// Subtraction of the numbers
void sub(float a, float b) {
    printf("Result: %f\n", a - b);
}

// Multiplication of the numbers
void mult(float a, float b) {
    printf("Result: %f\n", a * b);
}

// Division of the numbers
void divi(float a, float b) {
    if (b == 0) {
        printf("Error: 0 can't be a divider\n");
    } else {
        printf("Result: %f\n", a / b);
    }
}

void screen() {
    char control;
    int input;
    float a, b;

    printf("Welcome to the calculator!\n");

    do {
        printf("\nWhich operation do you want to do?\n");
        printf("1 - Sum\n");
        printf("2 - Subtraction\n");
        printf("3 - Multiplication\n");
        printf("4 - Division\n");
        printf("Choose: ");
        scanf("%d", &input);

        printf("First number: ");
        scanf("%f", &a);
        printf("Second number: ");
        scanf("%f", &b);

        switch (input) {
            case 1:
                sum(a, b);
                break;
            case 2:
                sub(a, b);
                break;
            case 3:
                mult(a, b);
                break;
            case 4:
                divi(a, b);
                break;
            default:
                printf("Invalid operation selected. Please try again.\n");
        }

        printf("Press 'q' to quit or any other key to continue: ");
        scanf(" %c", &control);  
    } while (control != 'q');

    printf("Goodbye!\n");
}

int main() {
    screen();
    return 0;
}
