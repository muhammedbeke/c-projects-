#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <ctype.h>
#include <time.h>

const char *words[20] = {
   "apple","pear","banana","watermelon","melon","cherry","quince","nectarine","plum","avocado","kiwi","pineapple","mango","pomegranate","raspberry","fig","orange","mandarin","mulberry","lemon"
};

int main() {
    srand(time(NULL));
    const char *selectedWord = words[rand() % 20];
    int length = strlen(selectedWord);
    int attempts = 2 * length;
    char guessedLetters[20];
    int numberOfGuesses = 0;
	int letterFound = 5;
    
	int wordFound = 1;
    for (int i = 0; i < length; i++) {
        guessedLetters[i] = '_';
    }
    guessedLetters[length] = '\0';

    printf("Let's start the Hangman game\n");
    printf("The word you need to guess is %d letters long\n", length);

    while (numberOfGuesses < attempts) {
        printf("Guess a letter: %s\n", guessedLetters);
        char guessedChar;
        printf("Your guess: ");
        scanf(" %c", &guessedChar); 
        guessedChar = tolower(guessedChar);

        for (int i = 0; i < length; i++) {
            if (selectedWord[i] == guessedChar ) {
                guessedLetters[i] = guessedChar;
                letterFound = 0;
            }
        }
        if (letterFound == 5) {
            numberOfGuesses++;
            printf("Wrong guess\nRemaining attempts: %d\n", attempts - numberOfGuesses);
        } else {
            printf("Correct guess\n");
        }

        for (int i = 0; i < length; i++) {
            if (guessedLetters[i] == '_') {
                wordFound = 0;
                break;
            }
        }

        if (wordFound) {
            printf("Congratulations! You guessed the word correctly: %s\n", selectedWord);
            break;
        }
    }

    if (numberOfGuesses == attempts) {
        printf("You ran out of attempts. The correct word was: %s\n", selectedWord);
    }

    return 0;
}
