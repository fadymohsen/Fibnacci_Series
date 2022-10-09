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

## Fibonacci Series Methods
- Recursion
- Dynamic Programming
- DP using memoization
- Using power of the matrix
- Space Optimized Method
- Binet Formula

<br/>
<br/>
<br/>
<br/>



### 1) Using Recursion:-
```cpp
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



### 2) Using Dynamic Programming:-
```cpp
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


### 3) DP Using Memoization:
```cpp
#include <bits/stdc++.h>

using namespace std;

int dp[10];

int fib(int n)
{
	if (n <= 1)
		return n;
		
	// temporary variables to store
	// values of fib(n-1) & fib(n-2)
	int first, second;
	
	if (dp[n - 1] != -1)
		first = dp[n - 1];
	else
		first = fib(n - 1);
	
	if (dp[n - 2] != -1)
		second = dp[n - 2];
	else
		second = fib(n - 2);
	
	// memoization
	return dp[n] = first + second;
}

// Driver Code
int main()
{
	int n = 9;
	memset(dp, -1, sizeof(dp));
	cout << fib(n);
	getchar();
	return 0;
}
```
<br/>
<br/>


### 4) Using Power of the Matrix:
```cpp
#include<bits/stdc++.h>
using namespace std;
 
// Helper function that multiplies 2
// matrices F and M of size 2*2, and
// puts the multiplication result
// back to F[][]
void multiply(int F[2][2], int M[2][2]);
 
// Helper function that calculates F[][]
// raise to the power n and puts the
// result in F[][]
// Note that this function is designed
// only for fib() and won't work as
// general power function
void power(int F[2][2], int n);
 
int fib(int n)
{
    int F[2][2] = { { 1, 1 }, { 1, 0 } };
    if (n == 0)
        return 0;
    power(F, n - 1);
    return F[0][0];
}
 
void multiply(int F[2][2], int M[2][2])
{
    int x = F[0][0] * M[0][0] +
            F[0][1] * M[1][0];
    int y = F[0][0] * M[0][1] +
            F[0][1] * M[1][1];
    int z = F[1][0] * M[0][0] +
            F[1][1] * M[1][0];
    int w = F[1][0] * M[0][1] +
            F[1][1] * M[1][1];
     
    F[0][0] = x;
    F[0][1] = y;
    F[1][0] = z;
    F[1][1] = w;
}
 
void power(int F[2][2], int n)
{
    int i;
    int M[2][2] = { { 1, 1 }, { 1, 0 } };
     
    // n - 1 times multiply the
    // matrix to [[1,0],[0,1]]
    for(i = 2; i <= n; i++)
        multiply(F, M);
}
 
// Driver code
int main()
{
    int n = 9;
    cout << " " <<  fib(n);
    return 0;
}
```
<br/>
<br/>




### 5) Using Space Optimized Method:-
```cpp
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






### 6) Using Binet Formula:-
```cpp
#include<iostream>
#include<cmath>
 
int fib(int n) {
  double phi = (1 + sqrt(5)) / 2;
  return round(pow(phi, n) / sqrt(5));
}
 
// Driver Code
int main ()
{
  int n = 9;
  std::cout << fib(n) << std::endl;
  return 0;
}
```
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>



## Brief About Solutions

| Method  | Time complexity | Space complexity |
| ------------- | ------------- | ------------- |
| Recursion  | **O(2^N)**, i.e., exponential  | **O(N)**  |
| Dynamic Programming  | **O(N)**, i.e., linear  | **O(N)**  |
| DP using memoization  | **O(N)** | **O(N)**  |
| Using Power of the Matrix  | **O(N)** | **O(1)**  |
| Space Optimized Method  | **O(N)** i.e., linear | By DP is **O(1)**  |
| Binet Formula | **O(log[n]**), because calculating res^n takes log(n) time | **O(1)**  |



<br/>
<br/>
<br/>



#### [*My Github Account*](https://github.com/fadymohsen/fibnacci-series)
