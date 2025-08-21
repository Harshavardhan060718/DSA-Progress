#Arrays Problems on leet code 

#problem no 1732( Highest Altitude)
Topics covered -> Arrays , PrefixSum

Example 1:

Input: gain = [-5,1,5,0,-7]
Output: 1
Explanation: The altitudes are [0,-5,-4,1,1,-6]. The highest is 1.

# code that i written 

class Solution {
public:
    int largestAltitude(vector<int>& gain) {
        int n= gain.size();
        vector<int>prefix(n+1,0);
        for(int i=1;i<=gain.size();i++){
            prefix[i]= prefix[i-1] + gain[i-1];
        }
        return *max_element(prefix.begin(),prefix.end());
        
        
    }
};



