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
```cpp
#include <iostream>
#include <cstdio>

using namespace std;

int main()
{
    int arr[10];
    for(int i=0;i<10;i++){
        cin >>arr[i];
        if(arr[i]<=0) arr[i]=1;
        printf("X[%d] = %d\n",i,arr[i]);        
    }
    return 0;
}
```

```cpp
#include <iostream>
#include <cstdio>
#include <cmath>

using namespace std;

int main()
{
    int v;
    cin >>v;
    for(int i=0;i<10;i++){
        printf("N[%d] = %d\n",i,v*(int)pow(2,i));
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
    double x;
    for(int i=0;i<100;i++){
        if(cin >>x &&x<=10){
            printf("A[%d] = %.1lf\n",i,x);
        }
    }

    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int main()
{
    int l;
    cin >>l;
    char c;
    cin >>c;
    double sum=0,x;
    for(int i=0;i<12;i++){
        for(int j=0;j<12;j++){
            if(cin >>x && i==l) sum+=x;
        }
    }
    printf("%.1lf\n",c=='S'?sum:sum/12);
}
```

```cpp
#include <iostream>
#include <cstdio>

using namespace std;

int main()
{
    char c;
    cin >>c;
    double sum=0,x,idx=0;
    for(int i=0;i<12;i++){
        for(int j=0;j<12;j++){
            if(cin >>x&&j>i){
                sum+=x;
                idx++;
            }
        }
    }
    printf("%.1lf\n",c=='S'?sum:sum/idx);

    return 0;
}
```

```cpp
#include <iostream>
#include <cstdio>

using namespace std;

int main()
{
    char c;
    cin >>c;
    double sum=0,x,count=0;
    for(int i=0;i<12;i++){
        for(int j=0;j<12;j++){
            if(cin >>x && j+i<11){
                sum+=x;
                count++;
            }
        }
    }
    printf("%.1lf\n",c=='S'?sum:sum/count);

    return 0;
}
```

```cpp
#include <iostream>
#include <cstdio>

using namespace std;

int main()
{
    char c;
    cin >>c;
    double sum=0,x,count=0;
    for(int i=0;i<12;i++){
        for(int j=0;j<12;j++){
            if(cin >>x && j>i && j<11-i){
                sum+=x;
                count++;
            }
        }
    }
    printf("%.1lf\n",c=='S'?sum:sum/count);

    return 0;
}
```

```cpp
#include <iostream>
#include <cstdio>

using namespace std;

int main()
{
    char c;
    cin >>c;
    double sum=0,x,count=0;
    for(int i=0;i<12;i++){
        for(int j=0;j<12;j++){
            if(cin >>x && j<i && i+j<11){
                sum+=x;
                count++;
            }
        }
    }
    printf("%.1lf\n",c=='S'?sum:sum/count);

    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int main(){
    int n;
    while(cin >>n && n){
        for(int i=1;i<=n;i++){
            for(int j=1;j<=n;j++){
                int up=i,down=n-i+1,left=j,right=n-j+1;
                cout <<min(min(up,down),min(left,right)) <<' ';
            }
            cout <<endl;
        }
        cout <<endl;
    }
    return 0;
}
```

#### 字符串
```cpp
#include <iostream>
#include <string>

using namespace std;

int main()
{
    string str;
    getline(cin,str);
    cout <<str.size()<<endl;

    return 0;
}
```

```cpp
#include <iostream>
#include <string>

using namespace std;

int main()
{
    string str;
    getline(cin,str);
    int count=0;
    for(int i=0;i<str.size();i++){
        if(str[i]>='0' &&str[i]<='9') count++;
    }
    cout <<count;

    return 0;
}
```

```cpp

```

```cpp
#include <iostream>
#include <string>

using namespace std;

int main()
{
    string a,b;
    getline(cin,a);
    for(int i=0;i<a.length();i++){
        b=b+a[i]+' ';
    }
    cout <<b <<endl;

    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int main(){
    string str;
    char s;
    cin >>str >>s;
    for(int i=0;i<str.length();i++){
        if(str[i]==s) str[i]='#';
    }
    cout <<str;

    return 0;
}
```

```cpp
#include <iostream>
#include <string>

using namespace std;

int main(){
    string a,b;
    while(cin >>a >>b){
        int p=0;
        for(int i=1;i<a.size();i++){
            if(a[i]>a[p]) p=i;
        }
         cout <<a.substr(0,p+1)+b+a.substr(p+1) <<endl;
    }

    return 0;
}
```

```cpp

```

#### 函数
```cpp
#include <iostream>

using namespace std;

int fact(int n){
    if(n==1) return 1;
    else return n*fact(n-1);
}

int main(){
    int n;
    cin >>n;
    cout <<fact(n)<<endl;
    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int max(int x,int y){
    return x>y?x:y;
}

int main()
{
    int x,y;
    cin >>x >>y;
    cout <<max(x,y) <<endl;

    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int min(int x,int y){
    return x<y?x:y;
}

int gcd(int a,int b){
    int m=min(a,b);
    int target;
    for(int i=m;i>0;i--){
        if(a%i==0&&b%i==0){
            target=i;
            break;
        }
    }
    return target;
}

int main(){
    int a,b;
    cin >>a >>b;
    cout <<gcd(a,b) <<endl;

    return 0;
}

```

```cpp
#include <iostream>

using namespace std;

void swap(int& x ,int& y){
    int temp=x;
    x=y;
    y=temp;
}

int main(){
    int x,y;
    cin >>x >>y;
    swap(x,y);
    cout <<x <<' ' <<y <<endl;
    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

void print(int a[],int size){
    for(int i=0;i<size;i++){
        cout <<a[i] <<' ';
    }
}

int main(){
    int n,size;
    cin >>n >>size;
    int a[n];
    for(int i=0;i<n;i++){
        cin >>a[i];
    }
    print(a,size);

    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

void print2D(int a[100][100], int row ,int col){
    int x;
    for(int i=0;i<row;i++){
        for(int j=0;j<col;j++){
            cin >>x;
            cout <<x <<' ';
        }
        cout <<endl;
    }
}

int main(){
    int row,col;
    cin >>row >>col;
    int a[100][100];
    print2D(a,row,col);

    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int multiply(int x){
    if(x==1) return 1;
    return x*multiply(x-1);
}

int main(){
    int x;
    cin >>x;
    cout <<multiply(x) <<endl;

    return 0;
}
```

```cpp
#include <iostream>

using namespace std;

int f(int n){
    if(n==1||n==2) return 1;
    return f(n-1)+f(n-2);
}

int main(){
    int n;
    cin >>n;
    cout <<f(n);

    return 0;
}
```

#### 结构体、类、指针、引用
```cpp
class Solution {
public:
    int Fibonacci(int n) {
        if(n==0) return 0;
        else if(n==1) return 1;
        else return Fibonacci(n-1)+Fibonacci(n-2);
    }
};
```

```cpp
class Solution {
public:
    string replaceSpaces(string &str) {
        string res;
        for(int i=0;i<str.size();i++){
            if(str[i]==' ') res+="%20";
            else res+=str[i];
        }
        return res;
    }
};
```

```cpp
class Solution {
public:
    int getSum(int n) {
        return n==1?1:n+getSum(n-1);
    }
};
```

```cpp
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
    void deleteNode(ListNode* node) {
        node->val=node->next->val;
        node->next=node->next->next;
    }
};
```

```cpp
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
    ListNode* merge(ListNode* l1, ListNode* l2) {
        auto ln=new ListNode(-1),tail=ln;
        while(l1&&l2){
            if(l1->val < l2->val){
                tail->next=l1;
                tail=tail->next;
                l1=l1->next;
            }else{
                tail->next=l2;
                tail=tail->next;
                l2=l2->next;
            }
        }
        if(l1){
            tail->next=l1;
        }else{
            tail->next=l2;
        }

        return ln->next;
    }
};
```

#### STL容器、位运算与常用库函数
```cpp
class Solution {
public:
    int getNumberOfK(vector<int>& nums , int k) {
        int cnt=0;
        for(auto it=nums.begin();it!=nums.end();it++){
            if(*it==k) cnt++;
        }

        return cnt;
    }
};
```

```cpp
class Solution {
public:
    int getMissingNumber(vector<int>& nums) {
        int sum1=0,sum2=0;
        for(int i=0;i<=nums.size();i++){
            if(i!=nums.size()) sum1+=nums[i];
            sum2+=i;
        }

        return sum2-sum1;
    }
};
```

```cpp
class Solution {
public:
    void reOrderArray(vector<int> &array) {
         for(int i=0;i<array.size();i++){
             for(int j=i+1;j<array.size();j++){
                 if(array[j]%2!=0&&array[i]%2==0){
                     int temp=array[j];
                     array[j]=array[i];
                     array[i]=temp;
                 }
             }
         }
    }
};
```

```cpp
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
    vector<int> printListReversingly(ListNode* head) {
        vector<int> a;
        for(auto it=head;it;it=it->next) a.push_back(it->val);
        reverse(a.begin(),a.end());

        return a;
    }
};
```
