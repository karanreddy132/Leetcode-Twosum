# Leetcode-Twosum
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int,int> m;
        for(int i=0;i<nums.size();i++)
            m.insert({nums.at(i),i});
        
        for(int i=0;i<nums.size();i++){
            if(m.count(target-nums.at(i))>0 && i!=m[target-nums.at(i)])
                return {i,m[target-nums.at(i)]};
        }
        return {};
    }
};
