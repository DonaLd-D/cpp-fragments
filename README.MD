#### 变量、输入输出、表达式与顺序语句
```cpp
#include <iostream>

using namespace std;

int main()
{   
    int a,b;
    cin >> a >> b;
    cout << a+b << endl;
    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int main()
{
    int a,b,c,d;
    cin >> a >> b >> c >> d;
    cout << "DIFERENCA = "<<(a*b-c*d)<<endl;
    return 0;
}
```

```cpp
#include <iostream>
#include <cstdio>

using namespace std;

int main()
{
    double r;
    cin >>r;
    printf("A=%.4f",3.14159*r*r);
    return 0;
}
```

```cpp
#include <cstdio>

using namespace std;

int main()
{
    double a,b;
    scanf("%lf%lf",&a,&b);    
    printf("MEDIA = %.5lf",(a*3.5+b*7.5)/11);
    return 0;
}
```

```cpp
#include <cstdio>

using namespace std;

int main()
{
    int code,total;
    float salary;
    scanf("%d%d%f",&code,&total,&salary);
    printf("NUMBER = %d\nSALARY = U$ %.2f",code,(float)total*salary);
    return 0;
}
```

```cpp
#include <cstdio>

using namespace std;

int main()
{
    int x;
    float y;
    scanf("%d%f",&x,&y);
    printf("%.3f km/l",x/y);
    return 0;
}
```

```cpp
#include <cstdio>
#include <cmath>

using namespace std;

int main()
{
    double x1,y1,x2,y2;
    scanf("%lf%lf%lf%lf",&x1,&y1,&x2,&y2);
    printf("%.4lf",sqrt((x2-x1)*(x2-x1)+(y2-y1)*(y2-y1)));
    return 0;
}
```

```cpp
#include <cstdio>

using namespace std;

int main()
{
    int x;
    scanf("%d",&x);
    printf("%d\n",x);
    printf("%d nota(s) de R$ 100,00\n",x/100);
    x%=100;
    printf("%d nota(s) de R$ 50,00\n",x/50);
    x%=50;
    printf("%d nota(s) de R$ 20,00\n",x/20);
    x%=20;
    printf("%d nota(s) de R$ 10,00\n",x/10);
    x%=10;
    printf("%d nota(s) de R$ 5,00\n",x/5);
    x%=5;
    printf("%d nota(s) de R$ 2,00\n",x/2);
    x%=2;
    printf("%d nota(s) de R$ 1,00\n",x);
}
```

```cpp
#include <cstdio>

using namespace std;

int main()
{
    int x;
    scanf("%d",&x);
    int h=x/3600;
    x%=3600;
    int m=x/60;
    x%=60;
    printf("%d:%d:%d",h,m,x);
    return 0;
}
```

#### 判断语句
```cpp
#include <iostream>

using namespace std;

int main()
{
    int a,b;
    cin >>a >>b;
    if(a%b==0||b%a==0){
        cout <<"Sao Multiplos"<<endl;
    }else{
        cout <<"Nao sao Multiplos"<<endl;
    }
    return 0;
}
```

```cpp
#include <iostream>
#include <cstdio>

using namespace std;

int main()
{
    int x,y;
    double total;
    cin >>x >>y;
    if(x==1) total=y*4.00;
    else if(x==2) total=y*4.50;
    else if(x==3) total=y*5.00;
    else if(x==4) total=y*2.00;
    else total=y*1.50;
    printf("Total: R$ %.2lf",total);
    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int main()
{
    double x;
    cin >>x;
    if(x>=0&&x<=25) cout <<"Intervalo [0,25]"<<endl;
    else if(x>25&&x<=50) cout <<"Intervalo (25,50]"<<endl;
    else if(x>50&&x<=75) cout <<"Intervalo (50,75]"<<endl;
    else if(x>75&&x<=100) cout <<"Intervalo (75,100]"<<endl;
    else cout <<"Fora de intervalo"<<endl;
    return 0;
}
```

```cpp
#include <iostream>
#include <cstdio>

using namespace std;

int main()
{
    double a,b,c;
    cin >>a >>b >>c;
    double maxi=a>b?(a>c?a:c):(b>c?b:c);
    bool case1=maxi==a&&maxi<(b+c),case2=maxi==b&&maxi<(a+c),case3=maxi==c&&maxi<(a+b);
    if(case1||case2||case3) printf("Perimetro = %.1lf",a+b+c);
    else printf("Area = %.1lf",(a+b)*c/2);
    return 0;
}
```

```cpp
#include <iostream>
#include <cstdio>

using namespace std;

int main()
{
    int a,b,sustain;
    cin >>a >>b;
    if(a>b) sustain=24+b-a;
    else if(a==b) sustain=24;
    else sustain=b-a;
    printf("O JOGO DUROU %d HORA(S)",sustain);
    return 0;
}
```

```cpp
#include <iostream>
#include <cstdio>

using namespace std;

int main()
{
    double salary,pay,rise,perc;
    cin >>salary;
    pay=salary;
    if(salary<=400){
        perc=0.15;
        rise=salary*perc;
        pay+=rise;
    }else if(salary<=800){
        perc=0.12;
        rise=salary*perc;
        pay+=rise;
    }else if(salary<=1200){
        perc=0.1;
        rise=salary*perc;
        pay+=rise;
    }else if(salary<=2000){
        perc=0.07;
        rise=salary*perc;
        pay+=rise;
    }else{
        perc=0.04;
        rise=salary*perc;
        pay+=rise;
    }
    printf("Novo salario: %.2lf\nReajuste ganho: %.2lf\nEm percentual: %.0lf %\n",pay,rise,perc*100);

    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int main()
{
    string a,b,c,d;
    cin >>a >>b >>c;
    if(a=="vertebrado"){
        if(b=="ave"){
            if(c=="carnivoro") d="aguia";
            else d="pomba";
        }else{
            if(c=="onivoro") d="homem";
            else d="vaca";
        }
    }else{
        if(b=="inseto"){
            if(c=="hematofago") d="pulga";
            else d="lagarta";
        }else{
            if(c=="hematofago") d="sanguessuga";
            else d="minhoca";
        }
    }
    cout <<d <<endl;
    return 0;
}
```
#### 循环语句
```cpp
#include <iostream>

using namespace std;

int main()
{
    for( int i=2;i<=100;i+=2)
        cout <<i <<endl;
    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int main()
{
    int x;
    cin >>x;
    for(int i=1;i<=x;i+=2) cout <<i <<endl;

    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int main()
{
    int count=0;
    double x;
    for(int i=1;i<=6;i++){
        cin >>x;
        if(x>0) count++;
    }
    cout <<count <<" positive numbers"<<endl;

    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int main()
{
    int x,y,total=0;
    cin >>x >>y;
    if(x>y){
        int t=y;
        y=x;
        x=t;
    }
    for(int i=x+1;i<y;i++){
        if(i%2!=0) total+=i;
    }
    cout <<total;

    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int main()
{
    int x,maximun=0,idx=1;
    for( int i=1;i<101;i++){
        cin >>x;
        if(x>maximun){
            maximun=x;
            idx=i;
        }
    }
    cout <<maximun <<endl;
    cout <<idx;

    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int main()
{
    int x;
    while(cin >>x &&x){
        for(int i=1;i<=x;i++) cout <<i <<" ";
        cout <<endl;
    }
    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int main(){
    int a,n,sum=0;
    cin >>a;
    while(cin >>n,n<=0);

    sum+=a*n;
    for(int i=0;i<n;i++) sum+=i;
    cout <<sum <<endl;

    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int main()
{
    int n;
    cin >>n;
    for(int i=1;i<=n;i++){
        if(n%i==0) cout <<i<<endl;
    }
    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int main()
{
    int n,m;
    cin >>n >>m;
    for(int i=1;i<=n*m;i++){
        if(i%m==0) cout <<"PUM"<<endl;
        else cout <<i <<" ";
    }
    return 0;
}
```

#### 数组

