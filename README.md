# Exercitii-in-C
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

void init_array(int t[],int n)
{
    for(int i=0;i<n;i++)
    {
        t[i]= rand()%100;
    }
}

void print_array(int w[],int n)
{
    printf("\nArray este:\n");
    for(int i=0;i<n;i++)
    {
        printf("%d ",w[i]);
    }
}

void elemente_nule(int ananas[],int n)
{
    for(int i=0;i<n;i++)
    {
        if(ananas[i]==0)
        {
            printf("\nElementul nul este pe pozitia : %d",i);
            return;
        }
    }
    printf("\nVectorul nu contine 0");
}
void main()
{
    srand(time(NULL));
    int n;
    printf("Dati n= ");
    scanf("%d",&n);
    int c[n];
    int d[n];
    init_array(c,n);
    init_array(d,n);
     c[0] = 0;
    print_array(c,n);
    print_array(d,n);
    elemente_nule(d,n);

}
