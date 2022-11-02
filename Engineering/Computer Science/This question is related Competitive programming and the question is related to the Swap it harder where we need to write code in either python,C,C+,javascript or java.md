## Question :
This question is related Competitive programming and the question is related to the Swap it harder where we need to write code in either python,C,C+,javascript or java.
![image](https://user-images.githubusercontent.com/78461084/199543384-e1cdd92d-2e97-4dc8-ad5e-0d29a9aee191.png)
![image](https://user-images.githubusercontent.com/78461084/199543692-984b9426-09da-4a54-9ba5-48f3bdb2a1ca.png)
![image](https://user-images.githubusercontent.com/78461084/199543852-8d7228e3-d38d-4937-a7e3-aaa8cbedc4b9.png)
![image](https://user-images.githubusercontent.com/78461084/199543932-2180a3e1-c982-4e98-b738-029c56966a6c.png)

You only need to implement the function and please do not read the input instead use arguments to the function.Do not print output but instead return the values as specified.

## Solution :
Steps used in the solution :

- Count the frequency of all the elements through 0 to 9
- Now, the number of groups will be no more than the maximum frequency
- Using that frequency, we got our final array
- Now, we just need to count the minimum number of swaps required to make our given array the final array
- jump array denotes the true location of any array element into final array
- Now, the final aswer will be the number of inversions in array jump
- Number of inversions is calculated using set and lower bound method

Time complexity will be around O(N*logN)

Here is the implementation in C++,

```C++
#include <bits/stdc++.h>
using namespace std;
#define mod 1000000007
long long int solve(vector<int> &v, int n) {
        int freq[10] = {0};
        for(int x: v) freq[x]++;
        int maxFreq = 0;
        for(int i = 0; i < 10; i++) {
                maxFreq = max(maxFreq, freq[i]);
        }
        int lastMaxFreq;
        for(int i = 0; i < 10; i++) {
                if(freq[i] == maxFreq) {
                        lastMaxFreq = i;
                        break;
                }
        }

        vector<int> final;
        int round = 0;
        while(1) {
                int flag = 1;
                for(int i = 9; i >= 0; i--) {
                        if(freq[i] == 0) continue;
                        flag = 0;
                        if(i >= lastMaxFreq) {
                                final.push_back(i);
                                freq[i]--;
                                continue;
                        }
                        if(round + freq[i] < maxFreq) continue;
                        final.push_back(i);
                        freq[i]--;
                }
                if(flag) break;
                round++;
        }
        vector<int> indices[10];
        for(int i = n - 1; i >= 0; i--) {
                indices[v[i]].push_back(i);
        }
        int jump[n];
        int cnt = 0;
        for(int i = 0; i < n; i++) {
                int curr = final[i];
                jump[i] = indices[curr][indices[curr].size() - 1];
                indices[curr].pop_back();
        }
        long long int answer = 0;
        set<int> st;
        for(int i = 0; i < n; i++) st.insert(i);
        for(int i = 0; i < n; i++) {
                int curr = jump[i];
                int res = distance(st.begin(), st.lower_bound(curr));
                answer += res;
                answer %= mod;
                st.erase(curr);
        }
        return answer;
}
int main() {
        vector<int> v = {4, 0, 6, 0, 1, 9, 8, 0, 4};
        cout << solve(v, v.size()) << "\n";
}
```
