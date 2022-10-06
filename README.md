**Name: Fady Mohsen** <br/>
**Section: 1** <br/>
**Bench NO: 48** <br/>


# Different Solutions - Fibonacci Series
![Fibonacci Series](Fibonacci-series.png) <br/> <br/> <br/> <br/>




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
<br/>

## Brief About Solutions
| Solution NO   | Decription | Time Complexity |
| ------------  | ---------- | --------------- |
| Solution No_1 | Content cell | 00:00 |
| Solution No_2 | Content cell | 00:00 |
| Solution No_3 | Content cell | 00:00 |
| Solution No_4 | Content cell | 00:00 |
| Solution No_5 | Content cell | 00:00 |
| Solution No_6 | Content cell | 00:00 |

<br/>
<br/>

#### [*My Github Account*](https://github.com/fadymohsen/fibnacci-series)
