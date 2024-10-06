Count Good Numbers
A digit string is good if the digits (0-indexed) at even indices are even and the digits at odd indices are prime
For example, "2582" is good because the digits (2 and 8) at even positions are even and the digits (5 and 2) at odd positions are prime.
However, "3245" is not good because 3 is at an even index but is not even.

intituion--
using permutation -> property of multiplicity of number filling
fill even place with 0,2,4,6,8 => 5 options
fill odd place with prime 2,3,5,7 => 4 option

what we will do -
 a)-we will calculate the odd and even number
 even=n/2+n%2; (as it is 0-indexed)
 odd=n/2

 b)- taking power 5^even and 4^odd ans multiply them but we can't use pow in built fn directly as we have to take mod to avoid overflow

 c)- we will make user-defined power fn considering the modulus term

 CODE IS-
 
class Solution {
private:
    const long long mod = 1e9 + 7;
public:
    long long power(long long x, long long y) {
        if (y == 0)
            return 1;
        long long ans = power(x, y / 2);
        ans = (ans * ans) % mod;
        if (y % 2 != 0) {
            ans = (ans * x) % mod;
        }
          return ans;
    }
    int countGoodNumbers(long long n) {
        long long odd = n / 2;
        long long even = n / 2 + n % 2;
        long long first = (power(5, even)) % mod;
        long long second = (power(4, odd)) % mod;
        return (int)(first * second % mod);
    }
};

CODE Explanation--
1)-const long long mod = 1e9 + 7;  // to avoid overflow we declare mod to use

2)-   long long power(long long x, long long y) {        //x^y
        if (y == 0)
            return 1;                                   // base case if power become zero return 1 as x^0=1(x can be any number)
        long long ans = power(x, y / 2);                // keep divind power with 2 until it become zero
        ans = (ans * ans) % mod;                        // store answer
        if (y % 2 != 0) {                               // if power is odd 
            ans = (ans * x) % mod;                      // multiply with the number
        }
          return ans;
    }

 3)-   int countGoodNumbers(long long n) {
        long long odd = n / 2;
        long long even = n / 2 + n % 2;           
        long long first = (power(5, even)) % mod;
        long long second = (power(4, odd)) % mod;  
        return (int)(first * second % mod);            // type cast to integer
    }

