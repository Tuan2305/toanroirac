
#include<bits/stdc++.h>
using namespace std;

struct edge{
    int x, y, w;
};
const int INF = (int)1e9;
int n, m;
vector<edge> E;
int d[1005];
void nhap(){
    cin >> n >> m;
    for(int i = 0; i < m; i++){
        int x, y, w; cin >> x >> y >> w;
        E.push_back((edge){x, y, w});
    }
}
void BellmanFord(int s){
    fill(d + 1, d + n + 1, INF);
    d[s] = 0;
    for(int i = 1; i <= n - 1; i++){
        for(edge e : E){
            int u = e.x, v = e.y, w = e.w;
            if(d[u] < INF){
            d[v] = min(d[v], d[u] + w);
        }
    }
}
for(int i = 1; i <= n; i++) {
    cout << d[i] << ' ';
    }
}
int main(){
    nhap();
    BellmanFord(1);
    return 0;
}
