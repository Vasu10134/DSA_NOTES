## Missing Number  
  
Method 1 :  
comparing nums[i] to i  
  
```cpp
class Solution 
{
public:
    int missingNumber(vector<int>& nums) 
    {
        sort(nums.begin(),nums.end());
        for(int i=0;i<nums.size();i++)
        {
            if(i != nums[i])
                return i;

                continue;
        }
        return nums.size();
    }
};
```
  
Method 2 :  
XOR Method  
  
```cpp
class Solution 
{
public:
    int missingNumber(vector<int>& nums) 
    {
        int sum=nums.size();
        for(int i=0;i<nums.size();i++)
            sum ^= i ^ nums[i];
            
        return sum;
    }
};
```
  
