#include <stdio.h>
#include <stdlib.h>

int Sol(int n)
{
	int k = 10;

	while (n != 0)
	{
		if (n % 10 > k)
		{
			return 0;
		}

		k = n % 10;
		n /= 10;
	}

	return 1;
}
int main()
{
    int n;
    scanf("%d",&n);
    while (n--)
    {
        int t,res=1;
        scanf("%d",&t);
        while(t--) res*=10;
        for(int i=res/10;i<res;i++)
            { if(Sol(i)) printf("%d ",i); }
        printf("\n");

    }
    return 0;
}
