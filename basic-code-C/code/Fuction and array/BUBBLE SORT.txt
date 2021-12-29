#include <stdio.h>

void swap (int *xp, int *yp)
{
    int temp = *xp;
    *xp = *yp;
    *yp = temp;
}

void Xuat (int a[], int n)
{
    int i;
    for ( i = 0 ; i < n; i++)
        printf ("%d ", a[i] );
    printf ("\n");
}
void bubbleSort (int a[] , int n){
    int i , j,res=1;
    for ( i = n-1 ; i >0 ; i--){
        int d=0;
        for ( j = 0 ; j <  i ; j++)
            while ( a[j] > a[j+1] ){
                swap ( &a[j] , &a[j+1] );
                d=1;
            }
    if(d==1) { printf("Step %d: ", res); res ++ ;  Xuat( a , n);}
    }
}


int main()
{
    int n , a[100000];
    scanf("%d", &n);
    for( int i = 0 ; i < n; i++)
        scanf("%d", &a[i]);
    bubbleSort ( a , n);
    return 0;
}