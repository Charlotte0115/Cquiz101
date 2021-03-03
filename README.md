#include <stdio.h>
#include <stdlib.h>

typedef struct stack
{
    int top;
    int capacity;
    int* array;
} Stack;

Stack* createStack(int capacity) 
{
    Stack* stack = (Stack*)malloc(sizeof(Stack));
    stack->capacity = capacity;
    stack->top = -1;
    stack->array = (int *)malloc(stack->capacity*sizeof(int));
    return stack;
}

int isFull(Stack* stack) 
{
    return stack->top == stack->capacity-1;
}

int isEmpty(Stack* stack) 
{
    return stack->top == -1;
}

void push(Stack* stack, int item) 
{
    if (isFull(stack)) 
        return;
    stack->array[++stack->top] = item;
    printf("%d pushed to stack\n", item);
}


int main()
{


    return 0;
}
