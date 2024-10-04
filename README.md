Pow(x, n)
question description---
~ 2^8=256
~ 3^4=243
intution--
brute force-
 2^8 ==> muliply 2 for 8 times-- O(n) n=power

optimised- 
2^8=> 4^4 => 16^2 => 256^1=> 256  taking half of previous approach
2^9=>* Note this case: here the case of odd power what we will do--
       . We will store in res to 2^1 rest will become 2^8
       . we will do it the same way as our above


code---

    double myPow(double x, int n) {
        if (n == 0) return 1; 
        
        long long int N = n; 
        if (N < 0) {
            x = 1 / x;  
            N = -N;
        }
        
        double res = 1;
        while (N > 0) {
            if (N % 2 == 1) res *= x; 
            x *= x;                   
            N /= 2;                  
        }
        return res;
    }

Explaination of code--

1)-  if (n == 0) return 1;   // if power is 0 then the result is 1 

2)- long long int N = n;    // To avoid overflow we uses long long int

3)-  if (N < 0) {       // Handeling negative power 
            x = 1 / x;  // like 3^-2 ==> 1/3^2
            N = -N;     // power from -2 to 2
        }
    
4)-  double res = 1;  // to store result in double as to return in double

5)-  while (N > 0) { 
            if (N % 2 == 1) res *= x;  // if odd power multiply in res
            x *= x;        // squaring base            
            N /= 2;        // halving power          
        }

 Calculate the power using Exponentiation by Squaring: The algorithm squares the base x and reduces N by half each iteration, 
 multiplying the result by x whenever N is odd.       

Time Complexity: O(logn); 
Space Complexity: O(1);
