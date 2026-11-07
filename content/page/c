#include <stdio.h>
#include <time.h>

//(1) O(n)
void func1(int n, long long *cnt)
{
    *cnt = 0;
    int i;
    for(*cnt=0, i=1; i<=n; i++)
        (*cnt)++;
}
//(2) O(log n)
void func2(int n, long long *cnt)
{
    *cnt = 1;
    while(*cnt <= n)
        (*cnt) *= 2;
}
//(3) O(n)
void func3(int n, long long *cnt)
{
    *cnt = 1;
    while(2*(*cnt) <= n)
        (*cnt)++;
}
//(4) O(n log n)
void func4(int n, long long *cnt)
{
    *cnt = 0;
    int i,j;
    for(i=1; i<=n; i++)
        for(j=1; j<=n; j*=3)
            (*cnt)++;
}
//(5) O(n^2)
void func5(int n, long long *cnt)
{
    *cnt = 0;
    int i,j;
    for(i=1; i<=n; i++)
        for(j=1; j<=i; j++)
            (*cnt)++;
}

int main()
{
    int N;
    printf("请输入N：");
    scanf("%d",&N);
    clock_t start,end;
    long long count;
    double time;

    start=clock(); func1(N,&count); end=clock();
    time=(double)(end-start)/CLOCKS_PER_SEC;
    printf("(1) O(n)  count=%lld, 耗时=%.6fs\n",count,time);

    start=clock(); func2(N,&count); end=clock();
    time=(double)(end-start)/CLOCKS_PER_SEC;
    printf("(2) O(logn) count=%lld, 耗时=%.6fs\n",count,time);

    start=clock(); func3(N,&count); end=clock();
    time=(double)(end-start)/CLOCKS_PER_SEC;
    printf("(3) O(n)  count=%lld, 耗时=%.6fs\n",count,time);

    start=clock(); func4(N,&count); end=clock();
    time=(double)(end-start)/CLOCKS_PER_SEC;
    printf("(4) O(nlogn) count=%lld, 耗时=%.6fs\n",count,time);

    start=clock(); func5(N,&count); end=clock();
    time=(double)(end-start)/CLOCKS_PER_SEC;
    printf("(5) O(n²) count=%lld, 耗时=%.6fs\n",count,time);
    return 0;
}
