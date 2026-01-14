## Valid Anagram

Method 1 : 
Using Maps

```cpp
class Solution {
public:
    bool isAnagram(string s, string t) {
        map<char, int> mp;
        for(auto i:s)
            mp[i]++;

        for(auto i:t)
            mp[i]--;

        for (auto &p : mp) 
        {
        if (p.second != 0)
            return false;
        }
        return true;
    }
};
```

Method 2 : 
Using Sorting

```cpp
class Solution 
{
public:
    bool isAnagram(string s, string t) 
    {
        sort(s.begin(), s.end());
        sort(t.begin(), t.end());
        
        if(s == t)
        return true;
        else
        return false;
    }
};
```
