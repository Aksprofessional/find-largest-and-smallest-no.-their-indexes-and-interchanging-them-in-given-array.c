# find-largest-and-smallest-no.-their-indexes-and-interchanging-them-in-given-array.c
find largest and smallest no. ,their indexes and interchanging them in given array.
// C program to find largest and smallest no. ,their indexes and interchanging them in given array.

#include <stdio.h>

int main() {
    int s,sm,i,n,l,n2,n3;

    printf("Enter the size of the array: ");
    scanf("%d", &s);

    int a[s]; 
    printf("Enter elements:\n");
    
    for (int i=0;i<s;i++)
        scanf("%d",&a[i]);
        
    sm=a[0];
     for (int i = 1; i <s; i++){
        if(sm>a[i]){
         sm=a[i];
         n=i;
        }
    }
    printf("index=%d\n",n);
    printf("smallest no.=%d\n",sm);
    
    l=a[0];
     for (int i = 1; i < s; i++){
        if(l<a[i]){
         l=a[i];
         n2=i;
        }
}
    printf("index=%d\n",n2);
    printf("largest no.=%d\n",l);
    
    n3=a[n];
    a[n]=a[n2];
    a[n2]=n3;
    
    printf("Array elemts after interchange are=");
       
      for (int i=0;i<s;i++)
         printf("%d\n",a[i]);
      
    return 0;
}
