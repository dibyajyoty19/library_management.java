Implement Binary Search Tree with Following functions:
- search
- insert
- delete

------------------------------------------------------------------------ CODE ---------- CODE ------------- CODE -----------------------------------------------------------------------------

class Node {
    int key;
    Node left, right;

    public Node(int item) {
        key = item;
        left = right = null;
    }
}

class BinarySearchTree {
    Node root;

    BinarySearchTree() {
        root = null;
    }

---------- Insert a key into the BST ----------
  
    void insert(int key) {
        root = insertRec(root, key);
    }

    Node insertRec(Node root, int key) {
        if (root == null) {
            root = new Node(key);
            return root;
        }
        if (key < root.key)
            root.left = insertRec(root.left, key);
        else if (key > root.key)
            root.right = insertRec(root.right, key);
        return root;
    }

---------- Search for a key in the BST ----------
  
    boolean search(int key) {
        return searchRec(root, key) != null;
    }

    Node searchRec(Node root, int key) {
        if (root == null || root.key == key)
            return root;
        if (key < root.key)
            return searchRec(root.left, key);
        return searchRec(root.right, key);
    }

---------- Delete a key from the BST ----------
  
    void delete(int key) {
        root = deleteRec(root, key);
    }

    Node deleteRec(Node root, int key) {
        if (root == null) return root;

        if (key < root.key)
            root.left = deleteRec(root.left, key);
        else if (key > root.key)
            root.right = deleteRec(root.right, key);
        else {
            if (root.left == null)
                return root.right;
            else if (root.right == null)
                return root.left;

            root.key = minValue(root.right);
            root.right = deleteRec(root.right, root.key);
        }
        return root;
    }

    int minValue(Node root) {
        int minValue = root.key;
        while (root.left != null) {
            minValue = root.left.key;
            root = root.left;
        }
        return minValue;
    }

---------- InOrder Traversal ----------
  
    void inorder() {
        inorderRec(root);
    }

    void inorderRec(Node root) {
        if (root != null) {
            inorderRec(root.left);
            System.out.print(root.key + " ");
            inorderRec(root.right);
        }
    }

---------- PreOrder Traversal ----------

    void preorder() {
        preorderRec(root);
    }

    void preorderRec(Node root) {
        if (root != null) {
            System.out.print(root.key + " ");
            preorderRec(root.left);
            preorderRec(root.right);
        }
    }

---------- PostOrder Traversal ----------
  
    void postorder() {
        postorderRec(root);
    }

    void postorderRec(Node root) {
        if (root != null) {
            postorderRec(root.left);
            postorderRec(root.right);
            System.out.print(root.key + " ");
        }
    }

    public static void main(String[] args) {
        BinarySearchTree bst = new BinarySearchTree();

        bst.insert(50);
        bst.insert(30);
        bst.insert(20);
        bst.insert(40);
        bst.insert(70);
        bst.insert(60);
        bst.insert(80);

        System.out.println("InOrder traversal:");
        bst.inorder();
        
        System.out.println("\nPreOrder traversal:");
        bst.preorder();
        
        System.out.println("\nPostOrder traversal:");
        bst.postorder();

        System.out.println("\n\nSearch for 40: " + bst.search(40));
        System.out.println("Search for 100: " + bst.search(100));

        System.out.println("\nDelete 20");
        bst.delete(20);
        System.out.println("InOrder traversal after deletion:");
        bst.inorder();

        System.out.println("\n\nDelete 30");
        bst.delete(30);
        System.out.println("InOrder traversal after deletion:");
        bst.inorder();

        System.out.println("\n\nDelete 50");
        bst.delete(50);
        System.out.println("InOrder traversal after deletion:");
        bst.inorder();
    }
}

 ------------------------------------------------------------------------ CODE ---------- CODE ------------- CODE -----------------------------------------------------------------------------


   **Tech Stack and Tools Used:**
- **Programming Language**: Java
- **Documentation**: JavaDoc for generating project documentation.
