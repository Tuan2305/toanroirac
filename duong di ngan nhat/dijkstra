
#include<bits/stdc++.h>
using namespace std;
typedef pair <int,int> ii;
int n,m ;
vector<ii> a[1000005];

void nhap(){
    cin>>n>>m;
    for (int i = 0;i<m ;i++){
        int x,y,w;
        cin>>x>>y>>w;
        a[x].push_back({y,w});
    }
}

void dijktra(int s){
    //b1 khởi tạo
    priority_queue<ii,vector<ii>, greater<ii>> Q;//sắp xếp theo thứ tự tăng dần (greater<ii>).
    Q.push({0,s});
    vector<int> d(n+1, 1e9); // mảng phụ để lưu đường đi   
    d[s]= 0;    

    while(!Q.empty()){ // Q chưa rỗng
        ii top = Q.top();Q.pop();// top = Q.top(); Dòng này lấy phần tử hàng đầu của hàng đợi Q (đây là phần tử ưu tiên cao nhất) và gán nó cho biến top/Q.pop(); Dòng này loại bỏ phần tử hàng đầu khỏi hàng đợi Q.
        int kc = top.first, u =top.second;
        if (kc> d[u]){
            continue;
        }
        //duyệt qua các đỉnh kề với v là u
        for (ii it: a[u]){
            int v = it.first, w = it.second;
            // (u,v) = 
            if (d[v] > d[u] +w){
                d[v] = d[u] +w;
                Q.push({d[v],v} );
            }
        }
    }
    for (int i  = 1;i<=n ;i++){
        cout <<d[i]<<" ";
    }

}
int main(){
    nhap();
    dijktra(1);// bắt đầu tại điểm A
    return 0;
}
// chú ý nhập vào theo danh sách cạnh


