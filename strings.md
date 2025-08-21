# Strings 

1 Concept that i have leanred using Two pointers 

well two pointer techinque pretty simple where it will be consisting of two variables in that one will be pointing at the starting location and,
 the other one will be points at last locatipon given string. 

Problem Statement 

Valid Palindrome:

the problem is about we will be having an input where it will be consisting of alphanumeric leeters and so other so what wb e have to do means first get filter the 
given input which shoukd only contain alphanumeric letters ((A-Z) and (0-9)) and afyter getting only alphanumeric letters revrse them and compare with the actuall array and return the answer 

-> So we can solve this by using two pointer technique as well as by using for loop where both will be consisting of O(n) complexity 

class Solution {
public:
    bool isPalindrome(string s) {
        int left = 0, right = s.length() - 1;

        while (left < right) {
            // Move left pointer to the next alphanumeric character
            while (left < right && !isalnum(s[left])) left++;
            // Move right pointer to the previous alphanumeric character
            while (left < right && !isalnum(s[right])) right--;

            // Compare characters ignoring case
            if (tolower(s[left]) != tolower(s[right])) return false;

            left++;
            right--;
        }

        return true;
    }
};


Date: 21-08-25

Problem statement :
Spliting a sub string into balanced 

Balanced strings are those that have an equal quantity of 'L' and 'R' characters.

Given a balanced string s, split it into some number of substrings such that:

Each substring is balanced.
Return the maximum number of balanced strings you can obtain.

 
Solution i written for this code is :

class Solution {
public:
    int balancedStringSplit(string s) {
        int r_count=0, l_count=0 , sub_strings=0;
        for(int i=0 ; i<s.length(); i++){
            if(s[i] == 'R') r_count++;
            else if (s[i] == 'L') l_count++;
            if(r_count == l_count) sub_strings+=1;
            }

       return sub_strings ;
    }
};




just used brute force tell me is there any other way of solving this better than this 

