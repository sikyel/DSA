import java.util.Scanner;

class BSTNode {
    int data;
    BSTNode left, right;


    public BSTNode() {
        left = null;
        right = null;
        data = 0;
    }

    public BSTNode(int data) {
        this.data = data;
        left = null;
        right = null;
    }

    public void setLeft(BSTNode n) {
        left = n;
    }

    public void setRight(BSTNode n) {
        right = n;
    }

    public BSTNode getLeft() {
        return left;
    }

    public BSTNode getRight() {
        return right;
    }

    public void setData(int data) {
        this.data = data;
    }

    public int getData() {
        return data;
    }
}

class BST {
    private BSTNode root;

    public BST() {
        root = null;
    }

    public boolean isEmpty() {
        return root == null;
    }

    public void insert(int data) {
        root = insertRecursively(root, data);
    }

    private BSTNode insertRecursively(BSTNode node, int data) {
        if (node == null) {
            node = new BSTNode(data);
        } else {
            if (data < node.getData()) {
                node.setLeft(insertRecursively(node.getLeft(), data));
            } else if (data > node.getData()) {
                node.setRight(insertRecursively(node.getRight(), data));
            }
        }
        return node;
    }

    public void delete(int data) {
        root = deleteRecursively(root, data);
    }

    private BSTNode deleteRecursively(BSTNode node, int data) {
        if (node == null) {
            System.out.println(data + " is not present");
            return null;
        }
        if (data < node.getData()) {
            node.setLeft(deleteRecursively(node.getLeft(), data));
        } else if (data > node.getData()) {
            node.setRight(deleteRecursively(node.getRight(), data));
        } else {
            if (node.getLeft() == null)
                return node.getRight();
            if (node.getRight() == null)
                return node.getLeft();

            node.setData(minValue(node.getRight()));
            node.setRight(deleteRecursively(node.getRight(), node.getData()));
        }
        return node;
    }

    private int minValue(BSTNode node) {
        int minValue = node.getData();
        while (node.getLeft() != null) {
            minValue = node.getLeft().getData();
            node = node.getLeft();
        }
        return minValue;
    }

    public int countNodes() {
        return countNodesRecursively(root);
    }

    private int countNodesRecursively(BSTNode node) {
        if (node == null)
            return 0;
        return 1 + countNodesRecursively(node.getLeft()) + countNodesRecursively(node.getRight());
    }

    public boolean search(int data) {
        return searchRecursively(root, data);
    }

    private boolean searchRecursively(BSTNode node, int data) {
        if (node == null) {
            return false;
        }
        if (data < node.getData()) {
            return searchRecursively(node.getLeft(), data);
        } else if (data > node.getData()) {
            return searchRecursively(node.getRight(), data);
        } else {
            return true;
        }
    }

    public void inorderTraversal() {
        inorderRecursively(root);
        System.out.println();
    }

    private void inorderRecursively(BSTNode node) {
        if (node != null) {
            inorderRecursively(node.getLeft());
            System.out.print(node.getData() + " ");
            inorderRecursively(node.getRight());
        }
    }

    public void preorderTraversal() {
        preorderRecursively(root);
        System.out.println();
    }

    private void preorderRecursively(BSTNode node) {
        if (node != null) {
            System.out.print(node.getData() + " ");
            preorderRecursively(node.getLeft());
            preorderRecursively(node.getRight());
        }
    }

    public void postorderTraversal() {
        postorderRecursively(root);
        System.out.println();
    }

    private void postorderRecursively(BSTNode node) {
        if (node != null) {
            postorderRecursively(node.getLeft());
            postorderRecursively(node.getRight());
            System.out.print(node.getData() + " ");
        }
    }
}

public class BinarySearchTree {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        BST bst = new BST(); // Step 27: Creating object of BST
        char ch;
        
        do {
            System.out.println("Binary Search Tree Operations");
            System.out.println("1. insert");
            System.out.println("2. delete");
            System.out.println("3. search");
            System.out.println("4. count nodes");
            System.out.println("5. check empty");
            int choice = scanner.nextInt();

            switch (choice) {
                case 1:
                    System.out.print("Enter integer element to insert: ");
                    bst.insert(scanner.nextInt());
                    break;
                case 2:
                    System.out.print("Enter integer element to delete: ");
                    bst.delete(scanner.nextInt());
                    break;
                case 3:
                    System.out.print("Enter integer element to search: ");
                    System.out.println("Search result: " + bst.search(scanner.nextInt()));
                    break;
                case 4:
                    System.out.println("Nodes = " + bst.countNodes());
                    break;
                case 5:
                    System.out.println("Empty status = " + bst.isEmpty());
                    break;
                default:
                    System.out.println("Wrong entry \n");
                    break;
            }
            
            System.out.print("Post order: ");
            bst.postorderTraversal();
            System.out.print("Pre order: ");
            bst.preorderTraversal();
            System.out.print("In order: ");
            bst.inorderTraversal();

            System.out.print("\nDo you want to continue (Type y or n): ");
            ch = scanner.next().charAt(0);
        } while (ch == 'Y' || ch == 'y');

        scanner.close();
    }
}
