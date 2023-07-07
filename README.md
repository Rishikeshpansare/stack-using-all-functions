# stack-using-all-functions
#include<stdio.h>
#include<conio.h>
#define MAX 5
 struct strack
 {
 	int a[MAX];
 	int top;
 }s1;
 void init()
 {
s1.top=-1;
 }
 int isempty()
 {
 	if(s1.top==-1)
 	return 1;
 	else
 	return 0;
 	
 }
  int isfull()
  {
 if(s1.top==MAX-1)
 return 1;
 else 
 return 0;
  }
  void push(int num)
  {
  	if(isfull())
  	printf("stack is full dont push");
  	else
  	{
  		s1.top++;
  		s1.a[s1.top]=num;
  		printf("\n push sucesfully");
	  }
   }
   void pop()
   {
   	int val;
   	if(isempty())
{
	printf("stack is empty dont pop");
	
   }
   else   
   {
     val=s1.a[s1.top];
     s1.top--;
     printf("\n poped values=%d",val);
 }
}
void disp()
{
	int i;
	for(i=s1.top;i>=0;i--)
	{
		printf("%d\n",s1.a[i]);
	}
}
int peek()
{
	return s1.a[s1.top];
}
int main()
{
	int ch,num;
	init();
	do
	{
	printf("\n 1- push \n2-pop \n 3-disp \n 4-peak");
	printf("\n entear choice");
	scanf("%d",&ch);
	switch(ch)
	{
		case 1:printf("entear numbear");
		    scanf("%d",&num);
		    push(num);
		    break;
	   case 2:pop();
	        break;
	  case 3:disp();
	        break;
       case 4: printf("peek element =%d",peek());
            break;
	  default:("invalid  choice__");
	  
	}
	}while(ch<5);
}
