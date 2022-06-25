# Data-Structures-and-Algorithms-on-different-scenarios

## Lab-1

Using linked list, write a program to add, subtract and evaluate polynomials: P1(x), P2(x), P3(x) and P4(x) where P1(x) and P2(x) are input polynomials and P3(x) = P1(x)+P2(x) and P4(x)=P1(x)-P2(x). Each node in the linked list correspond to a term in the polynomial. So, in your node structure - you may keep two data components – integers pow and coeff; and one pointer to the next node.

### Input Format:

First line mentions K i.e. the number of test cases. Then there are three lines for each test case, In the first two lines of a test case, First number indicate the highest degree of polynomials N and then there are N+1 integers which are the coefficients of polynomial terms in descending order. In the third (and last line) of a test case, there is one integer i.e. value of x for which you need to evaluate the polynomials. (Constraints: 0≤K≤50, 0≤N≤9, -2≤x≤2, and Input coefficient terms would be between -100 to +100; Assume you can safely do calculations for each polynomial term without worrying about underflow/overflow issues).

### Note: 

There is a single space before and after =, +, -, and : in the output. There should be NO nodes in the linked list for the polynomial terms having 0 coefficient value. In the above example, the polynomials f1 and f2 were to be represented using 4 and 2 nodes in the linked list, respectively

### Remarks: 
There are three test cases in 2nd Sample Input. Remember to appropriate free the memory space after each test case. Input would be read from terminal (i.e. stdin) and not from any file

## Lab-2

Question 1:-

You have a stack with push, pop and stackTop functionality. Assume that you have a sequence of n integers 1,2,3,….,n in this order. Using the given stack and the built-in functionality as mentioned already, state whether it is possible to construct a given output sequence or not. If yes, then show the sequence. (You can read the input only sequentially. Similarly, you can write on the output only sequentially, and once the output is written, you can’t read or modify it later.)

Example 1: 

Given input n = 3. (i.e. sequence available to you is 1,2,3). And given sequence: 2,1,3.

Answer: Yes. It is possible by the following sequence of operations: push(1), push(2), pop(), pop(), push(3), pop(). (i.e., we can create the sequence 2,1,3 using a stack.)

Example 2: 

Given input n=3. Given sequence: 3,1,2.

Answer: Not possible.

Your program should first read a given n from the user. And then read a sequence of length n. User will provide the sequence with space between the elements. That is, for the sequence 1,2,3, you will get 1 2 3. The program should output Yes/No, followed by the sequence of push/pop steps as already shown in example 1 above (of course, this push/pop list should be output only when the answer is yes).

Question 2:-

Convert a given Infix expression to Postfix expression. And then evaluate this postfix expression. The following operators are allowed in the input:

(i) +, –, *, / (with + and – having same level of precedence, which is lower than that of * and /)

(ii) ( and ) having higher precedence than all other operators

(iii) ^ (unary squaring operator, having higher precedence than +,-,*,/ but lower than brackets). Example: 3^ evaluates to 9.

(iv) << and >> : bitwise binary operators for left shift and right shift. Have same level of precedence as ^. Example: 1<<3 evaluates to 8. And 8>>2 evaluates to 2. That is, the left operand is binary shifted left or right, and the number of bits shifted is given by the right operand. (These are two < or > symbols, without any space between them).

Example Input: 2+(3^ + 4)<<2

Example output line 1: 2, 3^, 4, +, <<, +

Example output line 2: 54

(that is, 2 + (9+4)<<2 = 2 + 13<<2 = 2+ 52 = 54)

You can assume that the input length is not more than 100 characters. In case the input is wrong, you should print an error message. For example, these are some wrong inputs: 1 + (3 (i.e. no closing bracket), / 4 ( no left operand).

We assume that unary – is not present in the input. The only way – is used is in binary format.

Question 3:-

You created a singly linked lists in the first assignment. Use the previous codes (create nodes, insert node and display the list) to construct a linked list from the given inputs. Say, with given input 12, 45 and 7, you should create a singly linked list with 3 nodes in this order, i.e. head pointing to the node having data 12. Use the display list function to show the current state of the list.

Then write a non-recursive program to reverse this linked list. That is, the new list should have the same nodes but in the reversed order. You should not allocate new memory andcreate another linked list. Just modify the pointers of the current linked list suitably. Then display the list. (For the given example, we expect 7, 45, 12 now, and the head of the list should point to the node containing the data 7).

Input: n integers, with space between the values (you can assume that the data values are within -1000 to 1000), and that n will be a small integer.

Output: first display the list (this should be matching with the input), then display the list again after the reverse function is called (this time the list should be reversed). 

## Lab-3

A binary search tree (BST) is a special kind of binary tree, in which the following is true:

For each node, data at the left node is smaller than the data at the right node. (Recall that a node contains a data field, and two pointers).

Assume that we construct a BST with values 5,8,9,4,6 in this order. Then the resultant tree will look like

On the other hand, if the input data sequence was 8,9,5 (or 8,5,9) then a balanced binary tree with height 1 will be obtained. (We always start with the root and go left or right, recursively, depending on the input value being smaller or larger). To delete a node from the binary tree, one needs to readjust the other nodes so that the BST property still holds. For example, to delete 9 from the above tree, simply delete the node containing value 9. However, to delete 8, we will need to move 9 up. The resultant tree will look like:


1. Write a C program to do the following: (Maintain a global pointer to the root of the BST. Display a menu after each operation. And depending on user input, call appropriate function with inputs provided by the user. Assume that all the values in the BST are distinct and positive).

(i) On menu input 1, call a function to insert data into a BST (which is initially empty). The input will be given as a sequence of positive integers. The length of the sequence is not pre-specified, and hence you should allocate the necessary memory dynamically. Ex. We can say, 2,4,3,7,5,1 and the appropriate BST with 6 nodes should be constructed.

(ii) On menu input 2, call a function to delete a node from the BST. The node value will be input by the user. (If there is no node with such a value then print ‘error’). Ex. In the BST constructed by you in step (i), we may ask you to delete 4 (i.e. the node containing the value 4). At one time, we will ask you to delete only one node, but we can call the same function multiple times in succession. You should take care of the BST being empty when node deletion function is called. (Take care to handle deletion of an internal node with one child or with two children; a leaf; or the root itself).

(iii) On menu input 3, display the number of leaves, the number of internal nodes, and the height of the tree. (Assume that the root is at height 0. That is, the maximum level number and the height are equal.)

(iv) On menu input 4, display the in- order traversal of the tree. (Non-recursive code. No marks for the recursive version. However, you should verify your code by checking that the output matches with the recursive version in every case.)

(v) On menu input 5, display the pre-order traversal of the tree. (Non-recursive code. Same comment as in (iv) above.)

(vi) On menu input 5, display the post-order traversal of the tree. (Non-recursive code. Same comment as in (iv) above.)

## Lab-4

## Lab-5

## Lab-6

## Lab-7
