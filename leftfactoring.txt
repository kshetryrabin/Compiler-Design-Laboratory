#include<stdio.h>
//#include<conio.h>
#include<string.h>
void main()
{
	char a[10],a1[10],a2[10],a3[10],a4[10],a5[10],a6[10],a7[10],a8[25];
	int i,j=0,k,l,p;
//clrscr();
	printf("enter any productions A->");
	gets(a);
	for(i=0;a[i]!='/';i++,j++)
	a1[j]=a[i];
	a1[j]='\0';
	for(j=++i,i=0;a[j]!='\0';j++,i++)
	a2[i]=a[j];
	a2[i]='\0';
	//
	for(p=++j,i=0;a[p]!='\0';p++,i++)
	a6[i]=a[p];
	a6[i]='\0';
	//
	k=0;
	l=0;
	for(i=0;i<strlen(a1)||i<strlen(a2)||i<strlen(a6);i++)
		{
			if(a1[i]==a2[i] && a1[i]==a6[i])
			{
				a3[k]=a1[i];
				k++;
			}
			else
			{
				a4[l]=a1[i];
				a5[l]=a2[i];
				a7[l]=a6[i];
				l++;
			}
		}
	a3[k]='X';
	a3[++k]='\0';
	a4[l]='/';
	//a5[l]='\0';
	//a5[l]='/';
	a7[l]='\0';
	a4[++l]='\0';
	a5[++l]='\0';
	//a7[++l]='\0';
	//strcat(a4,a5);
	printf("\n %s",a4,"%s",a5);
	printf("\n %s",a4);
	strcat(a4,a7);
	printf("\n A->%s",a3);
	printf("\n X->%s",a4);
	printf("\n ");
//getch();
}
