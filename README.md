# mcu10166035.github.io
I am mcu10166035!!!

# 2022c
資傳一甲的程式設計的程式倉庫

# Week06

## (1) 考試 : 九九乘法表
考前複習、考後檢討
```cpp

#include <stdio.h>

int main()
{
	for (int i = 1; i < 10;i++)
	{
		for (int j = 1 ; j < 10; j++)
		{
			printf("%d*%d=%2d ",j,i,i*j);
		}
		printf("\n");
	}
}

```
## (2) 主題 : 畫星星(2層迴圈)
技巧 : 建立鷹架排版
```cpp
#include <stdio.h>

int main()
{
    for(int i =1;i<=5;i++)
    {
        int star = i*2-1;
        int space = 5-i;
        for (int k =0;k<space;k++)
        {
            printf(" ");
        }
        for (int k =0;k<star;k++)
        {
            printf("*");
        }
        printf(" 鷹架:%d樓 %d空格 %d星\n",i,space,star);
    }
}

```
## (3) 主題 : 最大公因數-暴力法
利用電腦一個一個試
```cpp
#include <stdio.h>

int main()
{
    printf("請輸入兩個數字: ");
    int a,b,ans;
    scanf("%d%d",&a,&b);
    for (int i =1;i<=a;i++)
    {
        if(a%i==0 && b%i==0) ans=i;
    }
    printf("找到 ans : %d ",ans);
}

```
## (4) 主題 : 輾轉相除法
利用輾轉相除法的概念設計程式
```cpp
#include <stdio.h>

int main()
{
    int a,b,c;
    printf("請輸入 2 個數字: ");
    scanf("%d%d",&a,&b);

    while(1)
    {
        c = a%b;
        printf("a: %d b: %d c: %d\n",a,b,c);
        if(c == 0) break;
        a=b;
        b=c;
    }
    printf("中的是: %d",b);
}

```

# Week07

## (1) 考試 : 畫星星(金字塔)
考前複習、考後檢討
```cpp

#include <stdio.h>

int main()
{
	int n;
	scanf("%d",&n);
	for (int i = 1; i <= n;i++)
	{
		int space = n-i,star=2n-1;
		for (int j = 0 ; j < space; j++) printf(" ");
		for (int j = 0 ; j < star; j++) printf("*");
		printf("\n");
	}
}

```
## (2) 主題 : long long int 各種類別
技巧 : long long int
```cpp
#include <stdio.h>

int main()
{
    int n = 1234567812345678;
    printf("%d\n",n);

    long long int a = 1234567812345678;
    printf("%lld\n",a); /// 小寫 LLD
}
```
## (3) 主題 : 最大公因數
技巧 : long long int 暴力拆解法
```cpp
#include <stdio.h>

int main()
{
    printf("請輸入兩個數字: ");
    long long int a,b,ans;
    scanf("%lld %lld",&a,&b);
    for (long long int i =1;i<=a;i++)
    {
        if(a%i==0 && b%i==0) ans=i;
    }
    printf("答案是 : %lld ",ans);
}
```
## (4) 主題 : 最大公因數
技巧 : long long int 輾轉相除法
```cpp
#include <stdio.h>

int main()
{
    long long int a,b,c;
    printf("請輸入 2 個數字: ");
    scanf("%lld%lld",&a,&b);

    while(1)
    {
        c = a%b;
        printf("a: %lld b: %lld c: %lld\n",a,b,c);
        if(c == 0) break;
        a=b;
        b=c;
    }
    printf("答案是: %lld\n",b);
}
```
## (5) 主題 : 剝皮法(10進位)
技巧 : 剝皮法
```cpp
#include <stdio.h>

int main()
{
    printf("請輸入一個數字 : ");
    int n ;
    scanf("%d",&n);

    while(n>0)
    {
        printf("%d\n",n%10);
        n = n/10;
    }
}
```
![week07-4](https://user-images.githubusercontent.com/114201423/197105855-88870f4c-7492-48b0-b004-c105e6047026.png)

# Week08

## (1) 考試 : 最大公因數-輾轉相除法
考前複習、考後檢討
```cpp
#include <stdio.h>

int main()
{
    int a,b,c ;
    scanf("%d%d",&a,&b);

    while(1)
    {
        c =a%b;
	if (c==0) break;
	a=b;
	b=c;
    }
    printf("%d",b);
}

```

## (2) 主題 : for迴圈金字塔
技巧 : 2個 for
```cpp
#include <stdio.h>

int main()
{
    int n;
    scanf("%d",&n);

    for (int i =1;i<=n;i++)
    {
        for (int k =1;k<=n;k++)
        {
            if (k<= n-i)
            {
                printf(" ");
            }
            else printf("*");
        }
        printf("\n");
    }
}
```

## (3) 主題 : while 迴圈金字塔
技巧 : 2個 while
```cpp
#include <stdio.h>

int main()
{
    int n;
    scanf("%d",&n);

    int i = 0;
    while(i<n)
    {
        int k = 0;
        while(k<n)
        {
            if (k<n-i-1) printf(" ");
            else printf("*");
            k++;
        }
        printf("\n");
        i++;
    }
}

```
## (4) 主題 : 質數判斷
技巧 : 
```cpp
#include <stdio.h>

int main()
{
    printf("要判斷你輸入的數字是不是孤獨的質數: ");
    int n;
    scanf("%d",&n);
    int bad = 0;
    for (int i =2;i<n;i++)
    {
        if(n%i==0) bad=1;
    }
    if (bad==0) printf("%d 是質數",n);
    else printf("%d 不是質數",n);
}

```
## (5) 主題 : 列出質數
技巧 : 
```cpp
#include <stdio.h>

int main()
{
    int a;
    scanf("%d",&a);

    for (int n=2;n<=a;n++)
    {
        int bad = 0;
        for (int i =2;i<n;i++)
        {
            if(n%i==0) bad=1;
        }
        if (bad==0) printf("%d ",n);
    }
}

```
## (6) 主題 :
技巧 : 
```cpp

```
![week08-6](https://user-images.githubusercontent.com/114201423/198499676-df4c34bb-9ed1-4deb-b227-c59c28fec95e.PNG)



# Week10

## (1) 考試 : 列出質數
考前複習、考後檢討
```cpp
#include <stdio.h>

int main()
{
    int a;
    scanf("%d",&a);

    for (int n=2;n<=a;n++)
    {
        int bad = 0;
        for (int i =2;i<n;i++)
        {
            if(n%i==0) bad=1;
        }
        if (bad==0) printf("%d ",n);
    }
}


```
## (2) 主題 : 陣列
技巧 : 
```cpp
#include <stdio.h>

int main()
{
    int a[4] = {10,20,30,40};

    printf("a[0]:%d\n",a[0]);
    printf("a[1]:%d\n",a[1]);
    printf("a[2]:%d\n",a[2]);
    printf("a[3]:%d\n",a[3]);
}

```
![week10-1](https://user-images.githubusercontent.com/114201423/201259955-28c930b7-40f8-4537-aa97-a37878f63124.png)

## (3) 主題 : 陣列-倒著印
技巧 : 
```cpp
#include <stdio.h>

int main()
{
    int a[4] = {10,20,30,40};
    for(int i=0;i<4;i++)
    {
        printf("a[%d]:%d\n",i,a[i]);
    }
    for(int i=3;i>=0;i--)
    {
        printf("%d ",a[i]);
    }
}

```
![week10-2](https://user-images.githubusercontent.com/114201423/201259994-fbdc6680-e3ba-4dcf-8d11-8b031bd23506.png)

## (4) 主題 : 輸入 100 個數字，並倒著列出來
技巧 : 
```cpp
#include <stdio.h>

int main()
{
	int a[100];
	for (int i=0;i<100;i++)
	{
		scanf("%d",&a[i]);
	}
	for (int i=99;i>=0;i--)
	{
		printf("%d\n",a[i]);
	} 
}
```
## (5) 主題 : github upload 
技巧 : 
```cpp
# cd 2022c
# git status
# git add .
# git status
# git config --global user.email mcu10166035@me.mcu.edu.tw
# git config --global user.name mcu10166035
# git commit -m "week10"
# git push
# git pull --rebase 
# git status
```
![week10-3](https://user-images.githubusercontent.com/114201423/201260022-c66133be-e7dd-499d-8025-f8b97a1582f6.png)

# Week11

## (1) 考試 : 百數反印
考前複習、考後檢討
```cpp
#include <stdio.h>

int main()
{
	int a[100];
	
	for (int i=0;i<100;i++)
	{
		scanf("%d",&a[i]);
	}
	
	for (int i=99;i>=0;i--)
	{
		printf("%d\n",a[i]);
	}
}

```
## (2) 主題 : 三數排列
技巧 : 
```cpp
#include <stdio.h>

int main()
{
    int a =90,b=80;

    printf("a:%d b:%d\n",a,b);

    int temp =a;
    a =b ;
    b =temp;

    printf("a:%d b:%d\n",a,b);
}

```
![week11-1](https://user-images.githubusercontent.com/114201423/202610306-a3d55c99-5208-4bf4-b328-ceae54499ac9.png)

## (3) 主題 : 三數排列2
技巧 : 
```cpp
#include <stdio.h>

int main()
{
    int a =90,b=80,c =70;

    if (a>b)
    {
        int temp =a;
        a =b ;
        b =temp;
    }
    if (b>c)
    {
        int temp =b;
        b =c ;
        c =temp;
    }
    if (a>b)
    {
        int temp =a;
        a =b ;
        b =temp;
    }

    printf("a:%d b:%d c:%d\n",a,b,c);
}

```
![week11-2](https://user-images.githubusercontent.com/114201423/202610327-d051c1aa-c9ff-47c0-9d87-6802b79ed925.png)


## (4) 主題 : 百數排列
技巧 : 
```cpp
#include <stdio.h>

int main()
{
    int a[10]={90,80,70,60,50,40,30,20,10,0};

    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");

    for (int i=0;i<10-1;i++)
    {
        if (a[i]>a[i+1])
        {
            int temp =a[i];
            a[i] = a[i+1];
            a[i+1] = temp;
        }
    }
    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");
}

```

![week11-3](https://user-images.githubusercontent.com/114201423/202610342-5ed6b946-97fd-4bf6-9adf-b3c62915fec0.png)

## (5) 主題 : 百數排列2
技巧 : 
```cpp
#include <stdio.h>

int main()
{
    int a[10]={90,80,70,60,50,40,30,20,10,0};
    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");

    for (int i=0;i<10-1;i++)
    {
        if (a[i]>a[i+1])
        {
            int temp =a[i];
            a[i] = a[i+1];
            a[i+1] = temp;
        }
    }

    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");
    for (int i=0;i<10-1;i++)
    {
        if (a[i]>a[i+1])
        {
            int temp =a[i];
            a[i] = a[i+1];
            a[i+1] = temp;
        }
    }

    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");
    for (int i=0;i<10-1;i++)
    {
        if (a[i]>a[i+1])
        {
            int temp =a[i];
            a[i] = a[i+1];
            a[i+1] = temp;
        }
    }
    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");

    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");
    for (int i=0;i<10-1;i++)
    {
        if (a[i]>a[i+1])
        {
            int temp =a[i];
            a[i] = a[i+1];
            a[i+1] = temp;
        }
    }
    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");

    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");
    for (int i=0;i<10-1;i++)
    {
        if (a[i]>a[i+1])
        {
            int temp =a[i];
            a[i] = a[i+1];
            a[i+1] = temp;
        }
    }
    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");

    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");
    for (int i=0;i<10-1;i++)
    {
        if (a[i]>a[i+1])
        {
            int temp =a[i];
            a[i] = a[i+1];
            a[i+1] = temp;
        }
    }
    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");

    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");
    for (int i=0;i<10-1;i++)
    {
        if (a[i]>a[i+1])
        {
            int temp =a[i];
            a[i] = a[i+1];
            a[i+1] = temp;
        }
    }
    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");

    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");
    for (int i=0;i<10-1;i++)
    {
        if (a[i]>a[i+1])
        {
            int temp =a[i];
            a[i] = a[i+1];
            a[i+1] = temp;
        }
    }
    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");

    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");
    for (int i=0;i<10-1;i++)
    {
        if (a[i]>a[i+1])
        {
            int temp =a[i];
            a[i] = a[i+1];
            a[i+1] = temp;
        }
    }
    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");
}

```
![week11-4](https://user-images.githubusercontent.com/114201423/202610363-761ce756-0bd9-4bed-b8e6-e608e75633e4.png)


## (6) 主題 : 百數排列3
技巧 : 泡泡排序法 Bubble sort
```cpp
#include <stdio.h>

int main()
{
    int a[10]={90,80,70,60,50,40,30,20,10,0};
    for (int i=0;i<10;i++) printf("%d ",a[i]);
    printf("\n");
    for (int k=0;k<10-1;k++)
    {
        for (int i=0;i<10-1;i++)
        {
            if (a[i]>a[i+1])
            {
                int temp =a[i];
                a[i] = a[i+1];
                a[i+1] = temp;
            }
        }

        for (int i=0;i<10;i++) printf("%d ",a[i]);
        printf("\n");
    }
}
```
![week11-5](https://user-images.githubusercontent.com/114201423/202610376-0829fd71-640b-4bc1-b98f-03ce6a7111f8.png)

# Week12

## (1) 考試 : 百數反印
考前複習、考後檢討
```cpp
#include <stdio.h>

int a[100]

int main()
{   
    for (int i=0;i<10;i++) {
    	scanf("%d",&a[i]);
    }
    for (int k=0;k<100;k++){
        for (int i=0;i<100;i++){
            if (a[i]>a[i+1]){
                int temp =a[i];
                a[i] = a[i+1];
                a[i+1] = temp;
            }
        }
    }
    for (int i=0;i<100;i++){ 
	printf("%d\n",a[i]);
    }
}
```

## (2) 主題 : 排序-選擇排序法
技巧 : 
```cpp
#include <stdio.h>

int a[5]={7,52,43,99,1};

int main()
{
    for(int i=0;i<5;i++){
        for(int j=i+1;j<5;j++){
            if (a[i]>a[j]){
                int temp=a[i];
                a[i]=a[j];
                a[j]=temp;
            }
        }
    }
    for(int i=0;i<5;i++){
        printf("%d ",a[i]);
    }
}

```
![week12-1](https://user-images.githubusercontent.com/114201423/203896180-cd78fefb-c81f-4727-8716-7881e7f173d8.png)

## (3) 主題 : 2D 陣列
技巧 : 
```cpp
#include <stdio.h>

int main()
{
    int a;
    int b=10;
    int c[3];
    int d[3]={10,20,30};
    int g[2][3];
    int h[2][3]={{10,20,30},{40,50,60}};
    for(int i=0;i<2;i++){
        for(int j=0;j<3;j++){
            printf("%d ",h[i][j]);
        }
        printf("\n");
    }
}

```
![week12-2](https://user-images.githubusercontent.com/114201423/203896206-f07fd871-56fe-451c-9715-b01f9187427d.png)
![week12-3](https://user-images.githubusercontent.com/114201423/203896218-cf3c164f-29b3-447f-b193-fcd928fa78b8.png)

## (4) 主題 : 矩陣加法
技巧 : 
```cpp
#include <stdio.h>

int main()
{
    int a[10][10],b[10][10],c[10][10];

    int n;

    scanf("%d",&n);

    for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
            scanf("%d",a[i][j]);
        }
    }

    for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
            scanf("%d",b[i][j]);
        }
    }

    for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
            c[i][j]=a[i][j]+b[i][j];
        }
    }

    for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
            printf("%3d",c[i][j]);
        }
    }
}

```
![week12-4](https://user-images.githubusercontent.com/114201423/203896235-0711fffb-5c08-44ec-a945-358aa30297c0.png)

## (5) 主題 : 矩陣乘法
技巧 : 
```cpp
#include <stdio.h>

int main()
{
	int a[10][10],b[10][10],c[10][10];
	int n;
	
	scanf("%d",&n);
	
	for(int i=0;i<n;i++){
		for (int j=0;j<n;j++){
			scanf("%d",&a[i][j]);
		}
	}
	for(int i=0;i<n;i++){
		for (int j=0;j<n;j++){
			scanf("%d",&b[i][j]);
		}
	}
	for(int i=0;i<n;i++){
		for (int j=0;j<n;j++){
			c[i][j]=0;
			for (int k=0;k<n;k++){
				c[i][j]+= a[i][k]*b[k][j];
			}
		}
	}
	for(int i=0;i<n;i++){
		for (int j=0;j<n;j++){
			printf("%3d ",c[i][j]);
		}
		printf("\n");
	}
}
```
![week12-5](https://user-images.githubusercontent.com/114201423/203896263-bfaf9bed-2bd0-49b1-8605-65444cd113b2.png)
