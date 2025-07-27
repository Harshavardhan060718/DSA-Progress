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



# problem no 560(Sub array sum equals to k)
Topics covered -> Arrays hash tables

Example 1:

Input: nums = [1,1,1], k = 2
Output: 2
# code that i written 

class Solution {
public:
    int subarraySum(vector<int>& nums, int k) {
        int count_sub=0;
        for(int i=0;i<nums.size();i++){
            int sum=0;
            for(int j=i;j<nums.size();j++){
                sum+=nums[j];
                if(sum==k) count_sub+=1;
            }
        }
        return count_sub;
    }
};



# problem no 724(Find pivot index)
Topics covered -> Arrays and prefxix sum

Example 1:

Input: nums = [1,7,3,6,5,6]
Output: 3
Explanation:
The pivot index is 3.
Left sum = nums[0] + nums[1] + nums[2] = 1 + 7 + 3 = 11
Right sum = nums[4] + nums[5] = 5 + 6 = 11


#code that i written 

class Solution {
public:
    int pivotIndex(vector<int>& nums) {
        int totalSum = 0;
        for (int num : nums) {
            totalSum += num;
        }

        int leftSum = 0;
        for (int i = 0; i < nums.size(); ++i) {
            int rightSum = totalSum - leftSum - nums[i];
            if (leftSum == rightSum) {
                return i;  
            }
            leftSum += nums[i];  
        }

        return -1; 
    }
};



#we will update more ... 