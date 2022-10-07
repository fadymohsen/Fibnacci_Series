**Name: Fady Mohsen** <br/>
**Section: 1** <br/>
**Bench NO: 48** <br/>
<br/>
<br/>
<br/>


# Different Solutions - Fibonacci Series
![Fibonacci Series](Fibonacci-series.png) <br/> <br/> <br/> <br/>
<br/>
<br/>
<br/>


#### 1) Using Recursion:-
```
#include <iostream>
using namespace std;

int fib(int x) {
   if((x==1)||(x==0)) {
      return(x);
   }else {
      return(fib(x-1)+fib(x-2));
   }
}

int main() {
   int x , i=0;
   cout << "Enter the number of terms of series: ";
   cin >> x;
   cout << "\nFibonnaci Series : ";
   
   while(i < x) {
      cout << " " << fib(i);
      i++;
   }
   return 0;
}
```
<br/>
<br/>



#### 2) Using Dynamic Programming:-
```
#include <iostream>
using namespace std;


void fib(int lookup[],int n){
    for(int i=2;i<=n;i++){
        lookup[i]=lookup[i-1]+lookup[i-2];
    }
}


int main(){

    int n;
    cout << "Enter the number of terms of series: ";
    cin>>n;

    int lookup[n+1];
    lookup[0]=0;
    lookup[1]=1;
    fib(lookup,n);

    cout<<"The nth integer in the Fibonacci Sequence = ";
    cout<<lookup[n]<<endl;
}
```
<br/>
<br/>

#### 3) Using Space Optimized Method:-
```
#include<iostream>
using namespace std;

int main(){
int n, t1 = 0, t2 = 1, nextTerm = 0, i;
cout << "Enter the number of terms of series: ";
cin >> n;

if(n == 0 || n == 1)
cout << n;
else
nextTerm = t1 + t2;

for (i = 3; i <= n; ++i){
t1 = t2;
t2 = nextTerm;
nextTerm = t1 + t2;
}

cout << "Nth Term is: " <<t2<<endl<<endl;
}
```
<br/>
<bt/>

#### 4) Using Memoization:-
```
#include <iostream>
using namespace std;
#define N 1000
int dp[N];
int fibonacci(int n){
    // we will make a call if an element in array dp is -1
    if(dp[n]==-1){   
        if(n<=1){
            dp[n]=n;
        }else{
            //call to n-1  and n-2
            dp[n]=fibonacci(n-1)+fibonacci(n-2);
        }
    }
    return dp[n];
}

int main(){
   int n;
   n=10;
   // initializing values of an array to -1
   memset(dp,-1,sizeof(dp));
   cout<<fibonacci(n);
}
<br/>
<br/>
<br/>
<br/>



## Brief About Solutions
<br>

| Method  | Time complexity | Space complexity | Notes |
| ------------- | ------------- | ------------- | ------------- |
| Recursion  | T(2^N), i.e., exponential  | O(N)  | ------------- |
| Dynamic Programming  | T(N), i.e., linear  | O(N)  | ------------- |
| Space Optimized Method  | T(N) i.e., linear | By DP is O(1)  | We have to find the sum of two terms, and it is repeated n times depending on the value of n |
| Memoization | O(n) making calls for value from 1 to n only once | O(n) using an array to store values of recursive calls  | ------------- |



<br/>
<br/>
<br/>



#### [*My Github Account*](https://github.com/fadymohsen/fibnacci-series)
