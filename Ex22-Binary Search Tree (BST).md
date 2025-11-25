# Ex22 Searching for a Book ID in a Binary Search Tree (BST)
## DATE: 22/11/25
## AIM:
To design and implement java program that constructs a Binary Search Tree (BST) using given Book IDs and checks whether a specific Book ID exists in the BST.
## Algorithm
1.Start the program.
2.Read integer.
3.Initialize root equals to null.
4.Repeat n times.
5.Insert(root, key).
6.Searching Book ID.
7.Search(root, key).
8.Stop the program.   

## Program:
```
/*
Program to constructs a Binary Search Tree (BST) using given Book IDs 
Developed by: SARISH VARSHAN V
RegisterNumber: 212223230196
import java.util.*;

public class BookIDSearch {
    static class Node {
        int data;
        Node left, right;
        Node(int data) {
            this.data = data;
        }
    }

    public static Node insert(Node root, int key) {
        if (root == null) return new Node(key);
        if (key < root.data) root.left = insert(root.left, key);
        else root.right = insert(root.right, key);
        return root;
    }

    public static boolean search(Node root, int key) {
        if (root == null) return false;
        if (root.data == key) return true;
        if (key < root.data) return search(root.left, key);
        else return search(root.right, key);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        Node root = null;
        for (int i = 0; i < n; i++) {
            root = insert(root, sc.nextInt());
        }
        int q = sc.nextInt();
        while (q-- > 0) {
            int key = sc.nextInt();
            System.out.println(search(root, key) ? "Found" : "Not Found");
        }
    }
}

*/
```

## Output:
<img width="738" height="305" alt="image" src="https://github.com/user-attachments/assets/ee1289c2-2bc5-4c0e-bac2-0adbfbb5ee22" />

## Result:
The program has been successfully implemented and executed.
It constructs a Binary Search Tree from the given Book IDs and accurately determines whether a queried Book ID exists in the library system.
