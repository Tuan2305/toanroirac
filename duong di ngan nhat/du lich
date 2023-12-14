#include<bits/stdc++.h>
using namespace std;

int a[100][100];
int n;
int chuaxet[100],x[100];
int s= 0;
int MIN = 999999;
int cmin = 999999;
void nhap(){
    cin>>n;
    for (int i = 1; i<= n ;i++){
        for (int j = 1;j<=n; j++){
            cin>>a[i][j];
            if (a[i][j] != 0 && a[i][j] < cmin ) {
                cmin = min(cmin,a[i][j]);// tìm c min nhỏ nhất của ma trận
             }
        }
    } 
}

void xuat(){
    for (int i =1; i <=n ;i++){
        for (int j = 1;j <= n ;j++){
            cout << a[i][j]<<" ";
        }
        cout <<endl;
    }
    cout <<endl;
}


void Try(int i){
    if ( s + cmin*(n - i + 1) >= MIN){// so tien toi thieu de di / can f(x)
        return;
    }
    else{
        for (int j = 1; j <= n; j++){
            if (chuaxet[j] == 1){// chua được đi qua
                x[i] = j;
                chuaxet[j] = 0;// da di qua 
                s += a[x[i-1]][j];
                if ( i == n){
                     if (s + a[x[n]][x[1]] < MIN){// so tien di tu thanh pho n ve 1
                        MIN = s + a[x[n]][x[1]];
                    }    
                }
                else Try(i+1);
                s -= a[x[i-1]][j];
                chuaxet[j] =1;// danh dau la chua di qua
            }   
        }
    }
}

int main(){
    for (int i = 2;i<=n;i++){
        chuaxet[i] = 1;
    }
    // memset(chuaxet,1,sizeof(chuaxet));// gan cho toan bo mang chua xet=1 
    chuaxet[1] = 0;
    x[1] = 1; // thanh pho dau tien     
    nhap();
    xuat();
    Try(2);
   
    cout <<MIN;
    return 0;
}
