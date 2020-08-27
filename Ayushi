#include<stdio.h>
#include<string.h>
#define MAX 3
typedef struct Basic
{
    int top;
    int array[MAX];
}Basics;

void implementation(Basics *Struc);
int isFull(Basics Struc);
int isEmpty(Basics Struc);
void push(Basics *Struc,int element);
int pop(Basics *Struc);
void Display(Basics *Struc);

int main()
{
    Basics Struc;
    implementation(&Struc);
    printf("\t\t\t\t\t\tMENU\n1. Push\n2. Pop\n3. IsEmpty\n4. IsFull\n5. Display\n6. Exit\n");
    while (1)
    {
        char str[10];
        printf("\nEnter your choice from Menu: ");
        scanf("%s",str);
        for (int i = 0; str[i]!='\0'; i++)
        {
            if(str[i] >= 'a' && str[i] <= 'z')
            {
                str[i] = str[i] -32;
            }
        }
        if(strcmp(str,"PUSH") == 0)
        {
            int element;
            printf("Enter the element to inserted: ");
            scanf("%d",&element);
            push(&Struc, element);
        }
        else if(strcmp(str,"POP") == 0)
        {
            int item = pop(&Struc);
            if(item==1)
                printf("Empty stack\n");
            else
                printf("Popped item is %d\n",item);
        }
        else if(strcmp(str,"ISFULL") == 0)
        {
            int num = isFull(Struc);
            if(num==1)
            {
                printf("Stack is Full\n");
            }
            else
            {
                printf("More Element can be inserted\n");
            }
        }
        else if(strcmp(str,"ISEMPTY") == 0)
        {
            int num = isEmpty(Struc);
            if(num==1)
            {
                printf("Stack is Empty\n");
            }
            else
            {
                printf("Not an Empty Stack\n");
            }
        }
        else if(strcmp(str,"DISPLAY") == 0)
        {
            Display(&Struc);
        }
        else if(strcmp(str,"EXIT") == 0)
        {
            return 0;
        }
    }
        
}
void implementation(Basics *Struc)
{
    Struc->top = -1;
}
int isFull(Basics Struc)
{
    if (Struc.top == MAX-1)
        return 1;
    else
        return 0;
}
int isEmpty(Basics Struc)
{
    if (Struc.top == -1)
        return 1;
    else
        return 0;
}
void push(Basics *Struc,int element)
{
    if (isFull(*Struc) == 1)
        printf("Stack overflow\n");
    else
    {
        Struc->top++;
        Struc->array[Struc->top] = element;
    }
}
int pop(Basics *Struc)
{
    if (isEmpty(*Struc) == 1)
        return 1;
    else
    {
        return Struc->array[Struc->top--];
    }
}
void Display(Basics *Struc)
{
    printf("The list is: ");
    for(int i = Struc->top; i >= 0;i--)
    {
        printf("%d ",Struc->array[i]);
    }
    printf("\n");
}
