# Ins8
#include <stdio.h>
#include <math.h>
int power(int a, int b, int P)
if (b == 1)
return a;
else
return ((int) pow(a, b)) % P);
int main ()
int P, G, x, a, y, b, ka, kb;
P = 23;
i printf("The value of P :%d\n", P);
G = 9;
printf("The value of G :%d\n", G);
a = 4;
printf("The private key a for Alice : %d\n", a);
x = power(G, a, P);
b = 3;
printf("The private key b for Bob : %d\n", b);
y = power(G, b, P);
ka = power(y, a, P);
kb = power(x, b, P);
printf("Secret key for the Alice is : %d\n", ka);
printf("Secret key for the Bob is : %d\n", kb);
return 0;
