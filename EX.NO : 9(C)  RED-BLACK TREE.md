
# EX.NO : 9(C)  RED-BLACK TREE 
 
# PROGRAM STATEMENT: 
 
To write the Right rotate module of the red black tree in CPP. 
 
# ALGORITHM:   
 
1. Start the program. 
2. Define rightrotate: Perform a right rotation on temp. 
3. Reassign left and right children: Set left to temp->l and update temp->l to left->r. Update the parent pointer of temp->l if necessary. 
4. Update parent of left: Set left->p to temp->p. If temp->p is NULL, set root to left. 
5. Update parent's child pointer: Adjust temp->p->l or temp->p->r to point to left. 
6. Complete rotation: Set left->r to temp, and temp->p to left. 
7. End the program. 
 
# PROGRAM: 
```
void rightrotate(node* temp)
{
    node *left=temp->l;
    temp->l=left->r;
    if(temp->l){
        temp->l->p=temp;
    }
    left->p=temp->p;
    if(!temp->p){
        root=left;
    }
    else if(temp==temp->p->l){
        temp->p->l=left;
    }
    else{
        temp->p->r=left;
    }
    left->r=temp;
    temp->p=left;
}
```


# output:

![image](https://github.com/user-attachments/assets/2f604755-e37c-41e9-9bed-6bad44885e8f)

# RESULT: 
 
Thus, the C++ program to write the Right rotate module of the red black tree in CPP is created successfully. 
