#include <stdio.h>

int main() {
    int n;
    printf("Введіть довжину послідовності n: ");
    scanf("%d", &n);

    int dp[n+1];
    dp[0] = 1;
    dp[1] = 2;
    dp[2] = 3;

    for (int i = 3; i <= n; i++) {
        dp[i] = (dp[i-1] + dp[i-2]) % 12345;
    }

    printf("Кількість шуканих послідовностей: %d\n", dp[n]);

    return 0;
}
