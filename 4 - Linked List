#include<stdio.h>
#include<stdlib.h>
struct node
{
 int data;
 struct node *next;
};
 struct node* h;
 struct node* p,*q;
 struct node* temp,*todelete;
 struct node* current;
 void insertfirst()
 {
  int x;
  printf("Enter no:");
  scanf("%d",&x);
  temp=(struct node*)malloc(sizeof(struct node));
  temp->data=x;
  temp->next=h;
  h=temp;
  temp=NULL;
  printf("Node inserted at first");
 }
 void insertlast()
 {
  int x;
  printf("Enter no:");
  scanf("%d",&x);
  temp=(struct node*)malloc(sizeof(struct node));
  current=h;
  temp->data=x;
  temp->next=NULL;
  if(h==NULL)
  h=temp;
  else
  {
   while(current->next!=NULL)
   current=current->next;
   current->next=temp;
  }
  temp=NULL;
  current=NULL;
  printf("Node inserted at last");
 }
 struct node *search_list()
 {
  int x;
  printf("Enter the no:");
  scanf("%d",&x);
  current=h;
  while(current!=NULL && current->data!=x)
  current=current->next;
  return current;
 }
 struct node *del_node()
 {
  int x;
  printf("Enter number:");
  scanf("%d",&x);
  if(h==NULL)
  {
   printf("List is empty");
   return h;
  }
  current=h;
  if(h->data==x)
  {
   h=h->next;
   current->next=NULL;
   free(current);
   current=NULL;
   printf("Value deleted");
   return h;
  }
  while(current->next!=NULL && (current->next)->data!=x)
  current=current->next;
  if(current->next!=NULL)
  {
   todelete=current->next;
   current->next=todelete->next;
   todelete->next=NULL;
   free(todelete);
   todelete=NULL;
   current=NULL;
   printf("Value deleted");
   return h;
  }
  current=NULL;
  printf("VAlue not exist");
  return h;
 }
 void display(struct node *h)
 {
  current=h;
  printf("Values in the list are:");
  while(current!=NULL)
  {
   printf("%d",current->data);
   current=current->next;
  }
 }
 int main()
 {
  int m,x,a;
  do
  {
   printf("Choose operation\n1.Insertion last\n2.Insertion first\n3.Searching\n4.Deletion\n5.Display\n6.Exit\n");
   scanf("%d",&m);
   switch(m)
   {
    case 1:insertlast();
            break;
    case 2:insertfirst();
            break;
    case 3:p=search_list();
           if(p==NULL)
             printf("VAlue not found");
           else
            printf("Value found");
            break;
    case 4:h=del_node();
           break;
    case 5:display(h);
           break;
    case 6:exit(0);
    default:
     printf("Select a valid option");
   }
  printf("\nEnter 1 for continue: ");
  scanf("%d",&a);
  printf("------------------------------\n");
  }
  while(a==1);
  return 0;
}  
