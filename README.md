# Data-structure-practical-program-17class Solution {
  public:
    bool twoSum(vector<int>& arr, int target) {
        unordered_set<int> s;

        for(int i = 0; i < arr.size(); i++) {
            int need = target - arr[i];

            if(s.find(need) != s.end()) {
                return true;
            }

            s.insert(arr[i]);
        }

        return false;
    }
};
