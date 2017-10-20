# The-first-research-I-do
#include <stdio.h>
#define line 4
#define size 4

int main()
{
	int a,b,c,d,e,f,g,h;
	int num[size][line]={2,3,5,8,
	                     4,2,3,6, 
						 5,3,2,7,
						 9,4,3,8};
	
	a=num[0][0];
	b=num[0][1];
	c=num[0][2];
	d=num[0][3];
	e=0;
	f=0;
	g=0;
	h=0;
	for(int i=1;i<size;i++)
	{
	    if(num[i][0]<a)
	    {
	    	a=num[i][0];
	    	e=i;
		}
    }
	for(int j=1;j<size;j++)
	{
	    if(num[j][1]<b)
	    {
	    	b=num[j][1];
	    	f=j;
		}
    }
	for(int k=1;k<size;k++)
	{
	    if(num[k][2]<c)
	    {
	    	c=num[k][2];
	    	g=k;
		}
    }
	for(int l=1;l<size;l++)
	{
	    if(num[l][3]<d)
	    {
	    	d=num[l][3];
	    	h=l;
		}
    }
    printf("%d %d %d %d\n",e,f,g,h);
	if(num[e][0]>num[e][1]&&num[e][0]>num[e][2]&&num[e][0]>num[e][3])
	    printf("该二维数组在第%d行第一列上的数为靶点.\n",e+1);
	if(num[f][1]>num[f][0]&&num[f][1]>num[f][2]&&num[f][1]>num[f][3])
	    printf("该二维数组在第%d行第二列上的数为靶点.\n",f+1);
	if(num[g][2]>num[g][0]&&num[g][2]>num[g][1]&&num[g][2]>num[g][3])
	    printf("该二维数组在第%d行第三列上的数为靶点.\n",g+1);
	if(num[h][3]>num[h][0]&&num[h][3]>num[h][1]&&num[h][3]>num[h][2])
	    printf("该二维数组在第%d行第四列上的数为靶点.\n",h+1);
	else
	    printf("该二维数组没有靶点.\n");
		
	return 0;										 
}
