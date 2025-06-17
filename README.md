#include <iostream>
#include <cstdlib> // For rand(), srand()
#include <ctime>   // For time()

int main() {
    std::srand(std::time(0)); // Set random seed
    int answer = std::rand() % 100 + 1; // Random number between 1 and 100
    int guess;
    int tries = 0;

    std::cout << "=== Number Guessing Game ===" << std::endl;

    do {
        std::cout << "Enter a number between 1 and 100: ";
        std::cin >> guess;
        tries++;

        if (guess > answer) {
            std::cout << "Too high!" << std::endl;
        } else if (guess < answer) {
            std::cout << "Too low!" << std::endl;
        } else {
            std::cout << "Correct! You guessed it in " << tries << " tries!" << std::endl;
        }

    } while (guess != answer);

    return 0;
}
