#include<stdio.h>
int main()
{
    int choice;
    double a,b,result;

    printf("===Your calculator is here===\n\n");
    jump:

    printf("1. addition\n");
    printf("2. subddition\n");
    printf("3.multiplication\n");
    printf("4. devition\n");

    printf("\n\nEnter your choice: ");
    scanf("%d",&choice);

    if(choice != 1 && choice != 2 && choice != 3 && choice != 4)
    {
    printf("ERROR: INVALID CHOICE \n\n");
    goto jump;
    }

    printf("\nEnter your 1st number: ");
    scanf("%lf",&a);

     printf("\nEnter your 2nd number: ");
    scanf("%lf",&b);

    if(choice <=4 && choice >=1)
    {
        if(choice==1)
        {
            result=a+b;
             printf("\n Your result is: %lf + %lf = %lf",a,b,result);
        }

         if(choice==2)
        {
            result=a-b;
             printf("\n Your result is: %lf - %lf = %lf",a,b,result);
        }
         if(choice==3)
        {
            result=a*b;
             printf("\n Your result is: %lf * %lf = %lf",a,b,result);
        }
         if(choice==4)
        {
           if(b!=0)
           {
             result=a/b;
             printf("\n Your result is: %lf / %lf = %lf",a,b,result);
           }
           else
           {
              printf("%lf never devided by %lf \n\n",a,b);
              goto jump;
           }
        }


    }
    else
        {
            printf("input a number between 1 to 4");
        }
    return 0;

}
