# Stacks, Queues - LIFO, FIFO

* resource

https://alx-intranet.hbtn.io/rltoken/0KVWTdE8xXy__jUfBfakCw

# objective

    What do LIFO and FIFO mean
    What is a stack, and when to use it
    What is a queue, and when to use it
    What are the common implementations of stacks and queues
    What are the most common use cases of stacks and queues
    What is the proper way to use global variables

# Data Structures

data structures for this project; include them in your header file.

/**
 * struct stack_s - doubly linked list representation of a stack (or queue)
 * @n: integer
 * @prev: points to the previous element of the stack (or queue)
 * @next: points to the next element of the stack (or queue)
 *
 * Description: doubly linked list node structure
 * for stack, queues, LIFO, FIFO
 */
typedef struct stack_s
{
        int n;
        struct stack_s *prev;
        struct stack_s *next;
} stack_t;

/**
 * struct instruction_s - opcode and its function
 * @opcode: the opcode
 * @f: function to handle the opcode
 *
 * Description: opcode and its function
 * for stack, queues, LIFO, FIFO
 */
typedef struct instruction_s
{
        char *opcode;
        void (*f)(stack_t **stack, unsigned int line_number);
} instruction_t;

#compilation 

$ gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty

# monty #

The goal of this project is to create an interpreter for Monty ByteCodes files.
There is not more than one instruction per line. 
There can be any number of spaces before or after the opcode and its argument. ie

julien@ubuntu:~/monty$ cat -e bytecodes/000.m
push 0$
push 1$
push 2$
  push 3$
                   pall    $
push 4$
    push 5    $
      push    6        $
pall$
julien@ubuntu:~/monty$


#this is goint to be tough!

# *AUTHOR 

KEMUNTO MAIRURA
