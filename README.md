#include<stdio.h>
#include<conio.h>

void main()
{
    struct node{
    int data;
    struct node *prev;
    struct node *next;
    };

    struct node *head, *newnode, *temp;
    int choice=1;
    while (choice)
    {
    head=0;
    newnode=(struct node *)malloc(sizeof(struct node));
    printf("enter the data :");
    scanf("%d->", &newnode->data);

    newnode->prev=0;
    newnode->next=0;

    if(head==0)
    {
        head = temp = newnode;
    }
    else
    {
        temp->next = newnode;
        newnode->prev= temp;
       temp=newnode;
    }
    printf("do you continue?(0,1)");
    scanf("%d", &choice);
    }

   temp = head;
    while( temp!=0)
    {
        printf("%d->", temp->data);
        temp = temp->next;
    }
    getch();
}
