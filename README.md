# symmetrical-winner
the first repository
#include "stdio.h"
void main()
{   int i,j,M;
int c=0,d,z[4100];
printf("input M");
		scanf("%d",&M);
		printf("please input to shuzu:");
for(i=0;i<M;i++)
{
scanf("%d",&z[i]);}
	//输出原始数据
    for(i=0;i<M;i++)
		printf("%d ",z[i]);
	putchar('\n');
	//删除相同数据
for(i=0;i<M-1-c;i++)
{
	for(j=i+1;j<M;j++)
	{ 
		if(z[j]==z[i])
        {

			c++;//记录总共有几个不同的数据
			for(d=j;d<M;d++)
			z[d]=z[d+1];
		    j--;
		}

    }

}
//输出最终数据
for(i=0;i<M-c;i++)·
		printf("%d ",z[i]);
	putchar('\n');			

}

