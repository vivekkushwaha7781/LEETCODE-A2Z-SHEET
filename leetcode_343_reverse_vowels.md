Reverse Vowels of a String
Given a string s, reverse only all the vowels in the string and return it.

The vowels are 'a', 'e', 'i', 'o', and 'u', and they can appear in both lower and upper cases, more than once.
Example 1:

Input: s = "IceCreAm"

Output: "AceCreIm"

Explanation:

The vowels in s are ['I', 'e', 'e', 'A']. On reversing the vowels, s becomes "AceCreIm".

SOLVING WITH TWO POINTER APPROACH---
take a pointer l at index =0; and r at n-1;
see if Vowels occurrs at both l and r then just swap
else increase l and decrease r;

CODE
class Solution {
public:
bool isVowel(char &c){            // FUNCTION for checking if char is vowel or not
    if(c=='a' || c=='e' || c=='i' || c=='o' || c=='u' || c=='A' || c=='E' || c=='I' || c=='O' || c=='U') return true;
    return false;
}
    string reverseVowels(string s) {
        int i=0, j=s.length();
        while(i<j){
            if(!isVowel(s[i])){
                i++;
            }else if(!isVowel(s[j])){
                j--;
            }else{       // BOTH are vowels
                swap(s[i],s[j]);
                i++,j--;
            }
        }
        return s;
    }
};
