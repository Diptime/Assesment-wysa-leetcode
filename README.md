# Assesment-wysa-leetcode

Solution to the leetcode question 98. Validate Binary Search Tree

Submission Link - https://leetcode.com/submissions/detail/1087746729/


Explanation : 

1. The code starts by defining the structure of a binary tree node using the struct TreeNode class. Each node contains an integer value (val) and two pointers to the left and right child nodes.

2. The isValidBST function is a member function of a class called Solution. It takes a single argument, which is a pointer to the root node of the binary tree.

3. Within the isValidBST function, there's a global variable prev declared and initialized to NULL. This variable will be used to keep track of the previous node visited in an inorder traversal of the tree.

4. The isValidBST function uses a recursive approach to check if the tree is a valid BST. It returns true if the tree is a valid BST and false if it's not.

5. The base case for the recursion is when root is NULL, which is considered a valid BST because there are no nodes to check.

6. The function then recursively calls itself on the left subtree (root->left). If the left subtree is not a valid BST (!isValidBST(root->left) returns false), it immediately returns false.

7. Next, it checks whether the current node's value is greater than or equal to the value of the previous node (prev). If this condition is true, it returns false, indicating that the tree is not a valid BST. Otherwise, it updates prev to the current node.

8. Finally, the function recursively calls itself on the right subtree (root->right). If the right subtree is not a valid BST (!isValidBST(root->right) returns false), it returns false.

9. If none of the above conditions cause the function to return false, it returns true` at the end, indicating that the tree is a valid BST.

In summary, this code uses an inorder traversal approach to check whether the binary tree is a valid BST by comparing the values of nodes and ensuring they are in ascending order. If all nodes meet the BST criteria, the function returns true; otherwise, it returns false
