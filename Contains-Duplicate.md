## Contains Duplicate  
  
Method 1 :  
Hashset  
  
```cpp
class Solution
{
public:
    bool containsDuplicate(vector<int>& nums)
    {
        unordered_set<int> s;
        for (int x : nums)
        {
            if (s.count(x)) return true;
            s.insert(x);
        }
        return false;
    }
};
```
  
Method 2 :  
Sorting + Scanning  
  
```cpp
class Solution
{
public:
    bool containsDuplicate(vector<int>& nums)
      {
        sort(nums.begin(), nums.end());
        for (int i = 1; i < nums.size(); i++)
        {
            if (nums[i] == nums[i-1])
                return true;
        }
        return false;
    }
};
```
  
