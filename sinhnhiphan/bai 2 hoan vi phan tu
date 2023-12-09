#include<bits/stdc++.h>
using namespace std;

int n,m,a[100],ok;
void khoitao(){
    for (int i = 1;i <= n;i++){
        a[i] = i;    
    }
}
void sinh(){
    int i = n -1;
    while( i >= 1 && a[i] > a[i+1]){
        i--;
    }
    if ( i ==0 ){
        ok = 0;
    }
    else{
        int j = n;
        while(a[i] > a[j]){
            --j;
        }
        swap(a[i],a[j]);
        int l = i+1 ,r = n;
        while (l < r)
        {
            swap(a[l], a[r]);
            l++;
            r--;
        }
        
    }
}
int main(){
    cin>>n ;
    ok = 1;
    khoitao();
    while(ok){
        for (int i = 1;i<= n;i++){
            cout <<a[i]<<" ";
        }
        cout <<endl;
        sinh();
    }
    return 0;   
}
