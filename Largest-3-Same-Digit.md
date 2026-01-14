## Largest 3 Same Digit Number  
  
Method 1 :  
Single-Pass Sliding Window  
  
```cpp
class Solution
{
public:
    string largestGoodInteger(string nums)
{
        char maxchar = ' ';
        for(int i=2;i<nums.size();i++)
        {
            if(nums[i] == nums[i-1] && nums[i] == nums[i-2])
            {
                maxchar = max(maxchar, nums[i]);
            }
        }
        if(maxchar == ' ')
        return "";
        else
        return string(3, maxchar);
    }
};
```
  
