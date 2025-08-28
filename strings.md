
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

23-08-25 
Problem Sttement : Group anagrams 

class Solution {
public:
    vector<vector<string>> groupAnagrams(vector<string>& strs) {
        unordered_map<string , vector<string>> anagrams_groups;
        for(const string&word : strs){
            string sorted_word = word;
            sort(sorted_word.begin(), sorted_word.end());
            anagrams_groups[sorted_word].push_back(word);
            
        }
        vector<vector<string>>result;
        for(auto& group: anagrams_groups){
            result.push_back(group.second);
        }

        return result;
        }
};




28-08-25

Problem statement : Sum of digits of string after converting 

You are given a string s consisting of lowercase English letters, and an integer k. Your task is to convert the string into an integer by a special process, and then transform it by summing its digits repeatedly k times. More specifically, perform the following steps:

Convert s into an integer by replacing each letter with its position in the alphabet (i.e. replace 'a' with 1, 'b' with 2, ..., 'z' with 26).
Transform the integer by replacing it with the sum of its digits.
Repeat the transform operation (step 2) k times in total.
For example, if s = "zbax" and k = 2, then the resulting integer would be 8 by the following operations:

Convert: "zbax" ➝ "(26)(2)(1)(24)" ➝ "262124" ➝ 262124
Transform #1: 262124 ➝ 2 + 6 + 2 + 1 + 2 + 4 ➝ 17
Transform #2: 17 ➝ 1 + 7 ➝ 8
Return the resulting integer after performing the operations described above.


 The code i written for this problem is like its simple formula positon = ch-'a'+1 because like using ascII values we can get that like 60-57 = 3 which means 'd'-'a'+1 same thing applyes for all alphabets ch-'a'+1 

Some other thing i learned rom this solution is :
-> to convert int to str9ng we will be using to_string(xxx);
-> stox() functions like to covert string into int, float , double etc like for int stoi(string) , stof(string)->for floatv like that and the solution i written is 

code :

class Solution {
public:
    int getLucky(string s, int k) {
        string converted="";
        for(char ch:s){
            int position = ch-'a'+1;
            converted+=to_string(position);
        }
        while(k-->0){
             int sum=0;
             for(char ch: converted){
                sum+= ch-'0';
             }
             converted= to_string(sum);

        }

        
        return stoi(converted);
    }
};





American standard code for information interchange 
'A'->65
'a'->97
'0'->48

 






