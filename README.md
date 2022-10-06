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


### 1) Using Recursion:-
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



### 2) Using Dynamic Programming:-
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

### 3) Using ................ :-
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
<br/>
<br/>
<br/>



## Brief About Solutions
<br>
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |




<br/>
<br/>
<br/>



#### [*My Github Account*](https://github.com/fadymohsen/fibnacci-series)
