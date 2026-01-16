#include <stdio.h>
#include <math.h>
int main() {
   int n, i, isPrime = 1;
   printf("Enter a positive integer: ");
   scanf("%d", &n);
   if (n <= 1) {
       isPrime = 0;
   } else if (n > 2 && n % 2 == 0) {
       isPrime = 0;
   } else {
       for (i = 3; i <= sqrt(n); i += 2) {
           if (n % i == 0) {
               isPrime = 0;
               break;
           }
       }
   }
   if (isPrime)
       printf("%d is a Prime Number\n", n);
   else
       printf("%d is NOT a Prime Number\n", n);
   return 0;
}
