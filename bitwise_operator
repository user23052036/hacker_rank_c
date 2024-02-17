#include<stdio.h>
#include<math.h>

void deci_to_binary_assign(int*,int*,int,int);
int main()
{
    int n,k,a,b;
    int result1,result2,result3;
    int max1=0 ,max2=0  ,max3 = 0 ;
    int a_byte[10], b_byte[10];

    scanf("%d%d",&n,&k);

    for(a=1; a<n; a++)
    {
        for(b=a+1; b<=n; b++)
        {
            result1=0 ,result2 = 0, result3 = 0;
            deci_to_binary_assign(a_byte,b_byte,a,b);

            for(int i=0; i<10; i++)
            {
                if(a_byte[i] == 1 && b_byte[i] == 1)
                    result1 = result1 + pow(2,i);

                if(a_byte[i] == 1 || b_byte[i] == 1)
                    result2 = result2 + pow(2,i);

                if(a_byte[i] != b_byte[i])
                    result3 = result3 + pow(2,i);
            }

            if(result1 < k && result1 > max1)
                max1 = result1;
            if(result2 < k && result2 > max2)
                max2 = result2;
            if(result3 < k && result3 > max3)
                max3 = result3; 
        }
    }
    printf("%d\n%d\n%d",max1,max2,max3);
    return 0;
}

void deci_to_binary_assign(int *a_byte, int *b_byte, int num1, int num2)
{   
    for(int i=0; i<10; i++)
        a_byte[i] = 0, b_byte[i] = 0;

    for(int i=9; i>=0; i--)
    {
        if(num1 >= pow(2,i))
        {
            a_byte[i] = 1;
            num1 = num1 - pow(2,i);
        }

        if(num2 >= pow(2,i))
        {
            b_byte[i] = 1;
            num2 = num2 - pow(2,i);
        }
    }
}
