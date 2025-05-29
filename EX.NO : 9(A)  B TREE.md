
# EX.NO : 9(A)  B TREE 
 
# PROGRAM STATEMENT: 
 
To write the findMin module of the B tree in CPP. 
 
# ALGORITHM:   
 
1. Start the program. 
2. Define the function findMin: Accept the root node (myNode) of a B-Tree as input. 
3. Traverse the Leftmost Path: Initialize a pointer curr to the root node and traverse down the leftmost child (link[0]) until reaching a leaf node (i.e., a node where link[0] is NULL). 
4. Print Minimum Value: Once the leftmost node is found, print its second value (val[1]), which is the minimum value in the node's key array. 
5. End the function. 
6. End the program. 
 
# PROGRAM:
```
void findMin(BTreeNode *myNode){
    BTreeNode *curr = myNode;
    while(curr->link[0]!=NULL){
        curr = curr->link[0];
    }
    cout<<endl<<"Min="<<curr->val[1];
    
}
```

# output:

![image](https://github.com/user-attachments/assets/6ee872de-b419-4b03-8063-c04fb741c29f)

# RESULT: 
 
Thus, the C++ program to write the findMin module of the B tree in CPP is created successfully.
