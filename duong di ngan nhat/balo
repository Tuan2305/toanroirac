#include<bits/stdc++.h>
using namespace std;

int n,m;// n la so luong , m la gia tri mon do
struct balo
{
    int w,val;
};

balo arr[10000];
bool cmp(balo a, balo b){
    return float(a.val/a.w) > (float)b.val/b.w;
}
int Try(int i, long  w , long val)
{
    if(w > m)
        return 0;
    if(i == n)
    {
        if(w <= m)
        return val;
        else return 0;
    }
        int l = Try(i + 1 ,w + arr[i].w, val + arr[i].val);
        int r = Try(i + 1, w , val);
        return max(l ,r);
    }
int main(){
    cin>>n>>m;
    for (int i = 0;i<n;i++){
        cin>> arr[i].w>>arr[i].val;
    }
    sort(arr,arr+n,cmp);
    cout <<Try(0,0,0);


    return 0;
}
