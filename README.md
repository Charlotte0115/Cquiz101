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

int main()
{


    return 0;
}
