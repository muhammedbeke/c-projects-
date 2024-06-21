#include <stdio.h>

void findDayOfWeek(int, int, int);

int main() {
    int day, month, year;
    printf("Enter your birth day (DD): ");
    scanf("%d", &day);
    printf("Enter your birth month (MM): ");
    scanf("%d", &month);
    printf("Enter your birth year (YYYY): ");
    scanf("%d", &year);
    findDayOfWeek(day, month, year);
    printf("Your birth date: %d/%d/%d\n", day, month, year);
    return 0;
}

void findDayOfWeek(int day, int month, int year) {
    if (month < 3) {
        month += 12;
        year -= 1;
    }
    int k = year % 100;
    int j = year / 100;

    int f = day + (13 * (month + 1)) / 5 + k + (k / 4) + (j / 4) - 2 * j;
    int dayOfWeek = f % 7;
    if (dayOfWeek < 0) {
        dayOfWeek += 7;
    }

    const char *daysOfWeek[7] = {"Saturday", "Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday"};
    printf("Your birth day is: %s\n", daysOfWeek[dayOfWeek]);
}
