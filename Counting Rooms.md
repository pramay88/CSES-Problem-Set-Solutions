# [Counting Rooms](https://cses.fi/problemset/task/1192/)
<img src="https://github.com/user-attachments/assets/f27880b4-1326-4342-8be0-cf5201656765" style="height: 80%;">

# Solution:
  `C++` `BFS`  
```cpp
#include<iostream>
#include<queue>
using namespace std;
int n, m, c; 
vector<vector<char>> g;
void bfs(int i, int j){
    queue<pair<int,int>> q; q.push({i,j}); g[i][j]='#';
    int d[4][2]={{0,1},{1,0},{-1,0},{0,-1}};
    while(!q.empty()){
        auto [x,y]=q.front(); q.pop();
        for(int k=0;k<4;k++){
            int nx=x+d[k][0], ny=y+d[k][1];
            if(nx>=0&&nx<n&&ny>=0&&ny<m&&g[nx][ny]=='.') g[nx][ny]='#',q.push({nx,ny});
        }
    }
}
int main(){
    ios::sync_with_stdio(0); cin.tie(0);
    cin>>n>>m; g.resize(n, vector<char>(m));
    for(auto &r:g) for(auto &c:r) cin>>c;
    for(int i=0;i<n;i++) for(int j=0;j<m;j++) if(g[i][j]=='.') bfs(i,j), c++;
    cout<<c;
}

```

# Complexity Analysis
<img src="https://github.com/user-attachments/assets/35c2c1b5-1e93-4927-85df-af087c45748b" style="width: 80%;">


