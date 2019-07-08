# symmetrical-winner
the first repository
#include<stdio.h>
void deletsame(int arr[],int num)//删除重复元素
{
	int i;
	int curnum;
	int j;
	int k;
	curnum=num;
	for(i=0;i<curnum;i++);
	{
		for(j=i+1;j<curnum;j++){
			if(arr[i]==arr[j])
			{
				for(k=j;k<(curnum-1);k++)
				{
					arr[k]=arr[k+1];
				}
				arr[curnum-1]=-999;
				curnum--;
				printf("i=%d,j=%d:",i,j);
				for(int m=0;m<num;m++)
					printf("%2d",arr[m]);
					printf("\n");
                j--;
			}
		}
	}
}
int main(int argc,char*argv[]){
	int testarr[100];
	int M;
	printf("input a number to M");
	scanf("%d",&M);
	printf("input a number to testarr ");
	for(int l=0;l<M;l++)
	scanf("%d",&testarr[l]);
	printf("原始数组：");
	for(int n=0;n<M;n++){
		printf("%d",testarr[n]);
	printf("\n");}
	deletsame(testarr,M);
	printf("\n删除后数组：");
	for(int m=0;m<M;m++){
		printf("%d",testarr[m]);
	printf("\n");}
	return 0;
}
