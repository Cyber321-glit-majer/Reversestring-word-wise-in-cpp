# Reversestring-word-wise-in-cpp
reverse a word c++

**PROBLEM STATEMENT**

Reverse the given string word-wise. The last word in the given string should come at 1st place, the last-second word at 2nd place, and so on. Individual words should remain as it is.

Input Format:

The first and only line of input contains a string without any leading and trailing spaces.

Output Format :

The only line of the output prints the Word wise reversed string.

Constraints :

0 <= |S| <= 10^5

where |S| represents the length of string, S.

Sample Input 1:

Welcome to Coding Ninjas

Sample Output 1:

Ninjas Coding to Welcome

Sample Input 2:

Always indent your code

Sample Output 2:

code your indent Always


**CODE**
```


#include <bits/stdc++.h>
using namespace std;
void solve(string s)
{
    int n=s.size();
    stack<string>st;
    for(int i=0;i<n;i++)
    {
        string word="";
        while(s[i]!=' ' && i<n)
        {
            word+=s[i];
            i++;
        }
        st.push(word);
    }
    while(!st.empty())
    {
        cout<<st.top()<<" ";
        st.pop();
    }
    cout<<endl;
}
int main ()
{
  string s;
 // cin>>s;
   getline(cin, s);
  solve(s);
  
  return 0;
}

