## Valid Parenthesis  
  
Method 1 :  
Using Stacks  
  
```cpp
class Solution
{
public:
    bool isValid(string s) 
    {
        stack<char> st;
        for(int i=0;i<s.size();i++)
        {
            if(s[i] == '{' || s[i] == '(' || s[i] == '[')
                st.push(s[i]);

            else
            {
                if(st.size() == 0)
                    return false;

                char top = st.top();
                st.pop();

                if(top == '(' && s[i] != ')' || 
                top == '[' && s[i] != ']' || 
                top == '{' && s[i] != '}')
                    return false;
            }
        }
        return st.empty();
    }
};
```
