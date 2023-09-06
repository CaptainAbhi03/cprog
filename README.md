# include<stdio.h>
void bubbleSort(int arr[],int n)
{
    for(int i=0;i<n-1;i++)
    {

        for(int j=0;j<n-i-1;j++)
        {
            if(arr[j+1]<arr[j])
            {
                int temp= 0;
                      temp=arr[j];

                arr[j]= arr[j+1];
                arr[j+1]= temp;

            }

        }
    }

}
void selection(int arr[],int n)
{
    for(int i=0;i< n;i++)
    {
        int small = i;
        for(int j= i+1;j<n;j++)
        {
            if(arr[small]>arr[j])
            {
                small= j;

            }

        }
        int temp = arr[i];
        arr[i]= arr[small];
        arr[small]= temp;

    }



}
void insertion(int arr[],int n)
{
    for(int i=1;i<n;i++)
    {
        int prev=i-1;
        int curr= arr[i];
        while(prev>=0 &&curr < arr[prev])
        {
             arr[prev+1] = arr[prev];
            prev--;
        }
        arr[prev+1]= curr;

    }
}
void input(int arr[],int n)
{
    printf("enter elements int he array");
    for(int i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);

    }

}
void output(int arr[],int n)
{
    for(int i=0;i<n;i++)
    {
        printf("%d \n",arr[i]);

    }


}
   int main()
   {
       int n;
       printf("enter size of array");
       scanf("%d",&n);
       int arr[n];
       input(arr,n);
       insertion(arr,n);
       output(arr,n);
        return 0;
   }
