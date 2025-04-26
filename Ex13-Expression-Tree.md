# Ex3.C Expression Tree
## DATE:17/3/25
## AIM:
To write a C function to construct an Expression Tree for the given Postfix Expression and display the output in the format of In-order ,Pre-order and Post-order traversal.

## Algorithm
1. Start 
2. Print node data in preorder then traverse left then right 
3. Traverse left in inorder then print node data then traverse right 
4. Traverse left in postorder then traverse right then print node data 
5. Recursive approach is used for all three traversal methods 
6. Functions handle each tree node using tree->d, tree->l, tree->r 
7. End  

## Program:
```
/*
Program to construct an Expression Tree for the given Postfix Expression and display the output in the format of In-order ,Pre-order and Post-order traversal.
Developed by:KAVINRAJ.S
RegisterNumber:  212223100019
*/
struct n { 
char d; 
struct n *l; 
struct n *r; 
};*/ 
void preOrder(struct n *tree) 
{ 
if(tree) 
{ 
printf("%c",tree->d); 
preOrder(tree->l); 
preOrder(tree->r); 
} 
} 
void inOrder(struct n *tree) 
{ 
if(tree) 
{ 
inOrder(tree->l); 
printf("%c",tree->d); 
inOrder(tree->r); 
} 
} 
void postOrder(struct n *tree) 
  
  
{ 
if(tree) 
{ 
postOrder(tree->l); 
postOrder(tree->r); 
printf("%c",tree->d); 
} 
} 
```

## Output:
![image](https://github.com/user-attachments/assets/fbd41791-2595-4c13-a44e-37313b5b9285)



## Result:

Thus, the C program to display the Expression Tree in the format of In-order ,Pre-order and Post-order traversal.
