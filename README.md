**Name: Fady Mohsen** <br/>
**Section: 1** <br/>
**Bench NO: 48** <br/>


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
   cout << "Enter the number of terms of series : ";
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
    cout<<"Enter n to find the nth number in the Fibonacci Sequence : ";
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















<br/>
<br/>
<br/>

## Brief About Solutions
| Solution NO   | Decription | Time Complexity |
| ------------  | ---------- | --------------- |
| Solution No_1 | Recursion | 00:00 |
| Solution No_2 | Dynamic Programming | 00:00 |
| Solution No_3 | Content cell | 00:00 |
| Solution No_4 | Content cell | 00:00 |
| Solution No_5 | Content cell | 00:00 |
| Solution No_6 | Content cell | 00:00 |

<br/>
<br/>

#### [*My Github Account*](https://github.com/fadymohsen/fibnacci-series)
