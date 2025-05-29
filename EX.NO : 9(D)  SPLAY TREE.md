
# EX.NO : 9(D)  SPLAY TREE 
 
# PROGRAM STATEMENT: 
 
To write the right rotate module of splay tree in CPP. 
 
# ALGORITHM:   
 
1. Start the program. 
2. Define rightRotate function: It takes a node x as input. 
3. Set y as the left child of x: Assign y = x->left. 
4. Reassign the left child of x: Set x->left = y->right. 
5. Update the right child of y: Set y->right = x. 
6. Return y: The new root after the rotation is y 
 
# PROGRAM: 
```
node *splay(node *root, int key)
{
    if (root->key == key)
        return root;
    if(root->key > key)
    {
        if (root->left == NULL) 
            return root;
        if (root->left->key > key)
        {
            root->left->left = splay(root->left->left, key);
            root = rightRotate(root);
        }
        else if(root->left->key < key)
        {
            root->left->right = splay(root->left->right, key);
 
            if (root->left->right != NULL)
                root->left = leftRotate(root->left);
        }
        return (root->left == NULL)? root: rightRotate(root);
    }
    else
    {
        if (root->right == NULL) 
            return root;
 
        if (root->right->key > key)
        {
            root->right->left = splay(root->right->left, key);
 
            if (root->right->left != NULL)
                root->right = rightRotate(root->right);
        }
        else if (root->right->key < key)
        {
            root->right->right = splay(root->right->right, key);
            root = leftRotate(root);
        }
        return (root->right == NULL)? root: leftRotate(root);
    }
}
```
# output:

![image](https://github.com/user-attachments/assets/2a10e950-8869-4b5b-af0c-dc061ed2389e)

# RESULT: 
 
Thus, the C++ program to write the right rotate module of splay tree in CPP is created successfully. 

