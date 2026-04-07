#include <stdio.h>

int nCr(int n, int r){
    if(r == 0 || r == n){
        return 1;
    } 
    if(r > n/2) {
        r = n - r;
    }
    return nCr(n-1, r-1) + nCr(n-1, r);
}

int main(){
    int n, r;
    printf("25331A05D6\n");
    printf("Enter n and r:\n");
    scanf("%d %d", &n, &r);
    if(n < r) {
        printf("Invalid input\n");
    } else {
        printf("%d\n", nCr(n, r));
    }

    return 0;
}
