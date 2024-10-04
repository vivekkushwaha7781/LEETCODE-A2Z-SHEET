String to Integer (atoi)
we  have given a string and we need to convert it in interger considering the following point-
 a)-ignore leading-white-space;
 b)-check for the - and + sign
 c)-if any other char is there other than number just return the answer
 d)-round the answer to Ignore TLE

class Solution {
public:
    string trimLeading(string s){
         int i=0;
          while(i<s.length() && s[i]==' '){
            i++;
          }
          return s.substr(i);
    }
    int myAtoi(string s) {
        if(s.length()==0) return 0;
       string str=trimLeading(s);
       if(str.length()==0) return 0;
       long long ans=0;
       bool neg=false;
       int i=0;
       if (str[0] == '-') {
            neg = true;
            i++;
        } else if (str[0] == '+') {
            i++;
        }
       for( ;i<str.length(); i++){
            char ch=str[i];
            
            if(ch>='0' && ch<='9'){
                int x= ch-'0';
                ans=ans*10+x;
                 if (!neg && ans > INT_MAX) return INT_MAX;
                if (neg && -ans < INT_MIN) return INT_MIN;
            }else{
                break;
            }
       }
       return neg ? -ans : ans;
    }
};

Breakdown the code--
1)- string trimLeading(string s){
         int i=0;
          while(i<s.length() && s[i]==' '){
            i++;
          }
          return s.substr(i);
    }

// This function removes leading spaces from the input string s

2)-  if(s.length()==0) return 0; // if initially the string s in empty just return 0;

3)- string str=trimLeading(s); //  return the  str which dont have any leading white space

4)- if(str.length()==0) return 0; // after trimming if str is empty return 0;

5)- long long ans=0; // for storing ans initallize with 0;

6)- bool neg=false; // whether the number is negative or positive

7)-int i=0;    // pointer initallise with 0 to traverse
       if (str[0] == '-') {    // checking for first sign to be negative
            neg = true;       //  if yes,, make neg bool to true
            i++;              // increase iterator
        } else if (str[0] == '+') {    // if +ve, just incrase iterator
            i++;
        }

8)-    for( ;i<str.length(); i++){
            char ch=str[i];
            
            if(ch>='0' && ch<='9'){    // if ch valued is int
                int x= ch-'0';         // convert to int --  ascii of 4=52 ans ascii of 0=48-- x=52-48=4(actual);
                ans=ans*10+x;          // intitally 0- 0*0+1(if 1 occur)=1 this way----
                 if (!neg && ans > INT_MAX) return INT_MAX;   // if number is positive and exceeding maximum 32-bit signed integer value- return INT_MAX to handle integer overflow
                if (neg && -ans < INT_MIN) return INT_MIN;
            }else{
                break;
            }
       }

9)- return neg ? -ans : ans;  // if negative return the answer with negative sign.
 
