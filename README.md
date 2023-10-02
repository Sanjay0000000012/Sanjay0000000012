#include <stdio.h>

void fibonacciSeries(int range) {
    int first = 0, second = 1, next;

    for (int i = 1; i <= range; ++i) {
        if (i == 1) {
            printf("%d ", first);
            continue;
        }
        if (i == 2) {
            printf("%d ", second);
            continue;
        }
        next = first + second;
        first = second;
        second = next;
        printf("%d ", next);
    }
}

int main() {
    int range;
    printf("Enter the range of the Fibonacci series: ");
    scanf("%d", &range);

    printf("Fibonacci series up to %d: \n", range);
    fibonacciSeries(range);

    return 0;
}
