## 169. Majority Element  
  
### Given an array nums of size n, return the majority element.  
### The majority element is the element that appears more than ⌊n / 2⌋ times. You may assume that the majority element always exists in the array.  
  

    
Method 1 :  
Sorting the nums array then returning middle element  

```cpp
class Solution  
{  
public:  
    int majorityElement(vector<int>& nums)   
    {  
        sort(nums.begin(), nums.end());  
        return (nums[nums.size()/2]);  
    }  
};
```

Method 2 :  
comparing nums[i] with nums[j], increment count  
  
```cpp  
class Solution  
{  
public:  
    int majorityElement(vector<int>& nums)  
    {  
        int x = nums.size();  
  
        for (int i = 0; i < x; i++)  
        {  
            int count = 1;  
            for (int j = i + 1; j < x; j++)
                {  
                if (nums[i] == nums[j])  
                {  
                    count++;  
                }  
            }  
            if (count > x / 2)  
            {  
                return nums[i];  
            }  
        }  
        return -1;  
    }  
};  
```
  
Method 3 :  

  

