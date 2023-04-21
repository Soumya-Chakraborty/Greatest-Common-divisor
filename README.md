# Write a function to compute the greatest common divisor given by Euclid's algorithm, exemplified for J = 1980, K=1617 as follows: 1980/1617-11980-11617-363 1617/ 363-41617-4363-165 363/165=2363-2165=335/33-5165-533=0 Thus, the greatest common divisor is 33
#include <stdio.h>

int gcd (int a, int b) {
  // base case
  if (b == 0) {
    return a;
  }
  // recursive case
  else {
    return gcd (b, a % b);
  }
}

int main () {
  int j = 1980;
  int k = 1617;
  printf ("GCD of %d and %d is %d\n", j, k, gcd (j, k));
  return 0;
}
