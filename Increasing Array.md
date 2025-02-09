# [Increasing Array](https://cses.fi/problemset/task/1094)

![Screenshot 2025-02-09 155547](https://github.com/user-attachments/assets/d66d8ba3-dbf7-41cb-9c76-b64b721e4fbd)

# Solution

```cpp
#include <iostream>
using namespace std;
int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    int n, prev, curr;
    long long moves = 0;
    cin >> n >> prev;
    while (--n) {
        cin >> curr;
        if (curr < prev) moves += prev - curr;
        else prev = curr;
    }
    cout << moves;
    return 0;
}
```
