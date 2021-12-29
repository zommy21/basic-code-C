#include <stdio.h>
#include <stdlib.h>

void Sol(int a[], int n){
    int tg;
    for(int i = 0; i < n - 1; i++){
        for(int j = i + 1; j < n; j++){
            if(a[i] > a[j]){
                tg = a[i];
                a[i] = a[j];
                a[j] = tg;
            }
        }
    printf("Step %d: ",i+1);
    for(int z=0;z<n;z++) { printf("%d ",a[z]);}
    printf("\n");
    }
}

int main()
{
    int n,a[100000];
    scanf("%d",&n);
    for(int i=0;i<n;i++)
        scanf("%d",&a[i]);
    Sol(a,n);
    return 0;
}
