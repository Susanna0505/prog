//xndir 1
#include <stdio.h>
#include <stdbool.h>
#include <ctype.h>
#include <string.h>


int main() {
    int num = 0;

    printf("Please enter your number: ");

    scanf("%d", &num);

    return 0;
}

//xndir 2
int main() {
    double num = 0;

    printf("Please enter any number: ");

    scanf("%lf", &num);

    return 0;
}

//xndir 3
int main()
char num = 0;

printf("Please enter any number: ")

scanf("%c", &num);

return 0;

//xndir 4

int num1 = 0;

int num2 = 0;

int sum = 0;

printf("Enter the first number: ");
scanf("%d", &num1);

printf("Enter the second number: ";);
scanf("%d", &num2 );

sum = num1 + num2

printf("%d, %d, %d", num1, num2, sum );

return 0;

//xndir 5
int main() {
    
    int age;

   
    printf("Please enter your age: ");
    scanf("%d", &age);

    printf("You are %d years old", age);

    return 0;
}

//xndir 6
int main() {

int x = 0;

int result = 0;

printf("Please enter the number for x: ");

 scanf("%d", &x);

 result = 4 * x + 21 * x * x - 12;

printf(" %d", result);

return 0;

}

// xndir 7
int main() {
    double x, result;

    printf("Please enter the x number: ");
    scanf("%lf", &x);

    result = x / (5 + 2) + 30 * x - 51;

    printf(" %lf", result);

    return 0;
}


//xndir 8
int main() {
    int x, y;
    double result;

    printf("Please enter x: ");
    scanf("%d", &x);

    printf("Please enter y: ");
    scanf("%d", &y);

    result = x * y + 21.0 * x / y - 200;

    printf(" %lf", result);

    return 0;
}

// xndir 9
int main() {
    char sym;

    printf("uppercase letter: ");
    scanf(" %c", &sym);

    if (sym >= 'A' && sym <= 'Z') {
        char lowercaseSym = sym + ('a' - 'A');

        printf("lowercase letter is: %c\n", lowercaseSym);
    } else {
        printf(" uppercase letter.\n");
    }

    return 0;
}

// xndir 10
int main() {
    char sym;

    printf("Please enter a character: ");
    scanf(" %c", &sym);

    bool Digit = (sym >= '0' && sym <= '9');

    if (Digit) {
        printf("true");
    } else {
        printf("false");
    }

    return 0;
}


// xndir 11


int main() {
    char text[1000]; 
    int vowels = 0, consonants = 0;

    printf("Enter a text: ");
    fgets(text, sizeof(text), stdin);

    for (int i = 0; text[i] != '\0'; i++) {
        char ch = tolower(text[i]); 

        if (isalpha(ch)) {
            if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
                vowels++;
            } else {
                consonants++;
            }
        }
    }

    printf("Vowels: %d\n", vowels);
    printf("Consonants: %d\n", consonants);

    return 0;
}

//xndir 12


bool isLetter(char ch) {
    return isalpha(ch) != 0;
}

bool isPalindrome(char str[]) {
    int left = 0;
    int right = strlen(str) - 1;

    while (left < right) {
        while (!isLetter(str[left]) && left < right) {
            left++;
        }

        while (!isLetter(str[right]) && left < right) {
            right--;
        }

        if (tolower(str[left]) != tolower(str[right])) {
            return false;
        }

        left++;
        right--;
    }

    return true;
}

int main() {
    char input[1000];

    printf("Enter a string: ");
    fgets(input, sizeof(input), stdin);

    input[strcspn(input, "\n")] = '\0';

    if (isPalindrome(input)) {
        printf("The input string is a palindrome.\n");
    } else {
        printf("The input string is not a palindrome.\n");
    }

    return 0;
}

//xndir 13

int main() {
    double celsius, fahrenheit;

    printf("Enter temperature in Celsius: ");
    scanf("%lf", &celsius);

    fahrenheit = (celsius * 9.0 / 5.0) + 32.0;

    printf("Temperature in Fahrenheit: %.2lf\n", fahrenheit);

    return 0;
}

//xndir 14

int main() {
    int age;

    printf("Please enter your age: ");
    scanf("%d", &age);

    if (age < 18) {
        printf("Duk anchapahas ek");
    } else if (age >= 18 && age <= 65) {
        printf("Duk chapahas eq");
    } else {
        printf("Duk tarec qaxaqaci eq");
    }

    return 0;
}

//xndir 15


int main() {
    int score;

    printf("Please enter the student's score: ");
    scanf("%d", &score);

    if (score >= 90 && score <= 100) {
        printf("Grade A\n");
    } else if (score >= 80 && score <= 89) {
        printf("Grade B\n");
    } else if (score >= 70 && score <= 79) {
        printf("Grade C\n");
    } else if (score >= 60 && score <= 69) {
        printf("Grade D\n");
    } else {
        printf("Grade E\n");
    }

    return 0;
}

// xndir 16

int main() {
    int height;

    printf("Please enter your height in centimeters: ");
    scanf("%d", &height);

    if (height >= 150) {
        printf("Duk hamapatasxan ek");
    } else {
        printf("Duk chek hamapatasxanum");
    }

    return 0;
}

// xndir 17
int main() {
    bool A, B;

    printf("Truth Table for A && B || !B ^ A\n");
    printf("A\tB\tResult\n");

    for (A = false; A <= true; A = !A) {
        for (B = false; B <= true; B = !B) {
            bool result = A && B || !B ^ A;
            printf("%d\t%d\t%d\n", A, B, result);
        }
    }

    return 0;
}

// xndir 18


int main() {
    bool A, B;

    printf("Truth Table for A || B && !(B || A)\n");
    printf("A\tB\tResult\n");

    for (A = false; A <= true; A = !A) {
        for (B = false; B <= true; B = !B) {
            bool result = A || (B && !(B || A));
            printf("%d\t%d\t%d\n", A, B, result);
        }
    }

    return 0;
}


//xndir 19
int main() {
    bool A, B;

    printf("Truth Table for !(A && B) || A && !B\n");
    printf("A\tB\tResult\n");

    for (A = false; A <= true; A = !A) {
        for (B = false; B <= true; B = !B) {
            bool result = !(A && B) || (A && !B);
            printf("%d\t%d\t%d\n", A, B, result);
        }
    }

    return 0;
}

// xndir 20
int main() {
    int number;

    printf("Please enter an integer: ");
    scanf("%d", &number);

    if (number % 2 == 0) {
        printf("%d is even", number);
    } else {
        printf("%d is odd", number);
    }

    return 0;
}

//21
int main() {
    char letter;

    printf("Please enter a letter: ");
    scanf(" %c", &letter);

    letter = tolower(letter);

    if (isalpha(letter)) {
        if (letter == 'a' || letter == 'e' || letter == 'i' || letter == 'o' || letter == 'u') {
            printf("%c is a vowel.\n", letter);
        } else {
            printf("%c is a consonant.\n", letter);
        }
    } else {
        printf("Invalid input. Please enter a letter.\n");
    }

    return 0;
}

//22
#include <stdio.h>

int main() {
    double num1, num2;

    printf("Enter the first number: ");
    scanf("%lf", &num1);

    printf("Enter the second number: ");
    scanf("%lf", &num2);

    if (num1 > num2) {
        printf("The largest number is %.2lf\n", num1);
    } else if (num2 > num1) {
        printf("The largest number is %.2lf\n", num2);
    } else {
        printf("Both numbers are equal.\n");
    }

    return 0;
}

//23

int main() {
    double num1, num2, num3;

    printf("Enter the first number: ");
    scanf("%lf", &num1);

    printf("Enter the second number: ");
    scanf("%lf", &num2);

    printf("Enter the third number: ");
    scanf("%lf", &num3);

    if (num1 == num2 && num2 != num3) {
        printf("The largest number is %.2lf\n", (num1 > num3) ? num1 : num3);
    } else if (num1 == num3 && num2 != num3) {
        printf("The largest number is %.2lf\n", (num1 > num2) ? num1 : num2);
    } else if (num2 == num3 && num1 != num3) {
        printf("The largest number is %.2lf\n", (num2 > num1) ? num2 : num1);
    } else {
        printf("No two numbers are equal.\n");
    }

    return 0;
}

//24...

//25
int main() {
    int year;

    printf("Enter a year: ");
    scanf("%d", &year);

    if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
        printf("%d is a leap year.\n", year);
    } else {
        printf("%d is not a leap year.\n", year);
    }

    return 0;
}

//26

int gcd(int a, int b) {
    if (b == 0) {
        return a;
    } else {
        return gcd(b, a % b);
    }
}

int main() {
    int num1, num2, num3;

    printf("Enter the first number: ");
    scanf("%d", &num1);

    printf("Enter the second number: ");
    scanf("%d", &num2);

    printf("Enter the third number: ");
    scanf("%d", &num3);

    int result = ayb(num1, num2);

    result = ayb(result, num3);

    printf("amenamec yndhanur bajanarary %d, %d, and %d is %d\n", num1, num2, num3, result);

    return 0;
}


//27...

//28...

//29...

//30
int main() {
    for (int i = 0; i <= 100; i++) {
        printf("%d\n", i);
    }

    return 0;
}

//31
int main() {
    for (int i = 1; i <= 100; i += 2) {
        printf("%d\n", i);
    }

    return 0;
}

//32

int main() {
    int number, reversed = 0;

    do {
        printf("Enter an integer greater than 12: ");
        scanf("%d", &number);

        if (number <= 12) {
            printf("Please enter a valid integer greater than 12.\n");
        }
    } while (number <= 12);

    while (number > 0) {
        int digit = number % 10;
        reversed = reversed * 10 + digit;
        number /= 10;
    }

    printf("Number in reverse order: %d\n", reversed);

    return 0;
}

//33
int main() {
    int number, sum = 0;

    printf("Enter a number: ");
    scanf("%d", &number);

    if (number < 0) {
        printf("Please enter a non-negative number.\n");
        
    }

    int originalNumber = number; 
    while (number > 0) {
        int digit = number % 10;
        sum += digit;
        number /= 10;
    }

    printf("The sum of the digits of %d is %d\n", originalNumber, sum);

    return 0;
}

//34...

//35
int main() {
    int number;

    do {
        printf("Enter a positive number: ");
        scanf("%d", &number);

        if (number <= 0) {
            printf("Please enter a positive number.\n");
        }
    } while (number <= 0);

    printf("Multiplication table for %d:\n", number);
    for (int i = 1; i <= 10; i++) {
        printf("%d x %d = %d\n", number, i, number * i);
    }

    return 0;
}

//36...

//37...

//38

int main() {
    int sideLength;

    printf("Enter the side length of the square: ");
    scanf("%d", &sideLength);

    if (sideLength <= 0) {
        printf("Please enter a positive side length.\n");
        return 1; // Exit the program with an error code
    }

    // Print the square
    for (int i = 0; i < sideLength; i++) {
        for (int j = 0; j < sideLength; j++) {
            printf("* ");
        }
        printf("\n");
    }

    return 0;
}

//39

int main() {
    int legLength;

    printf("Enter the length of the leg of the triangle: ");
    scanf("%d", &legLength);

    if (legLength <= 0) {
        printf("Please enter a positive leg length.\n");
        return 1; 
    }

    for (int i = 1; i <= legLength; i++) {
        for (int j = 1; j <= legLength - i; j++) {
            printf(" ");
        }
        
        for (int j = 1; j <= 2 * i - 1; j++) {
            printf("*");
        }

        printf("\n");
    }

    return 0;
}

//40ic heto chem karoghacel ((
