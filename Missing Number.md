# [Missing Number](https://cses.fi/problemset/task/1083)
<img src="https://github.com/user-attachments/assets/c612ff40-807a-48ef-a148-5232df5fbbc1" width="700">

# Solution
```cpp
#include <iostream>
using namespace std;
int main(){
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    int n;
    cin >> n;
    long long reqSum = (1LL * n * (n + 1)) / 2;
    long long sum = 0, num;
    for (int i = 0; i < n - 1; i++) {
        cin >> num;
        sum += num;
    }
    cout << reqSum - sum << '\n';
    return 0;
}
```
