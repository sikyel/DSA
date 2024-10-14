import java.io.*;

class Node {
    int data;
    Node prev;
    Node next;

    public Node(int data) {
        this.data = data;
        this.prev = null;
        this.next = null;
    }
}

class DoubleLinkedList {
    private Node first;
    private Node last;

    public DoubleLinkedList() {
        first = null;
        last = null;
    }

    public void insertAtFront(int data) {
        Node newNode = new Node(data);
        if (first == null) {
            first = last = newNode;
        } else {
            newNode.next = first;
            first.prev = newNode;
            first = newNode;
        }
        System.out.println("Inserted to Front: " + data);
    }

    public void insertAtRear(int data) {
        Node newNode = new Node(data);
        if (last == null) {
            first = last = newNode;
        } else {
            newNode.prev = last;
            last.next = newNode;
            last = newNode;
        }
        System.out.println("Inserted to Rear: " + data);
    }

    public void deleteFromFront() {
        if (first == null) {
            System.out.println("Deque is empty!");
        } else {
            System.out.println("Deleted from Front: " + first.data);
            first = first.next;
            if (first != null) {
                first.prev = null;
            } else {
                last = null; // List becomes empty
            }
        }
    }

    public void deleteFromRear() {
        if (last == null) {
            System.out.println("Deque is empty!");
        } else {
            System.out.println("Deleted from Rear: " + last.data);
            last = last.prev;
            if (last != null) {
                last.next = null;
            } else {
                first = null; // List becomes empty
            }
        }
    }

    public void displayFromFront() {
        if (first == null) {
            System.out.println("Deque is empty!");
        } else {
            System.out.print("Deque from Front: ");
            Node current = first;
            while (current != null) {
                System.out.print(current.data + " ");
                current = current.next;
            }
            System.out.println();
        }
    }

    public void displayFromRear() {
        if (last == null) {
            System.out.println("Deque is empty!");
        } else {
            System.out.print("Deque from Rear: ");
            Node current = last;
            while (current != null) {
                System.out.print(current.data + " ");
                current = current.prev;
            }
            System.out.println();
        }
    }
}

class Deque {
    private DoubleLinkedList deque = new DoubleLinkedList();

    public void insertFront(int data) {
        deque.insertAtFront(data);
    }

    public void insertRear(int data) {
        deque.insertAtRear(data);
    }

    public void deleteFront() {
        deque.deleteFromFront();
    }

    public void deleteRear() {
        deque.deleteFromRear();
    }

    public void displayFront() {
        deque.displayFromFront();
    }

    public void displayRear() {
        deque.displayFromRear();
    }
}

public class DequeApp {
    public static void main(String[] args) throws IOException {
        BufferedReader inp = new BufferedReader(new InputStreamReader(System.in));
        Deque q = new Deque();
        String ch = "y";

        while (ch.equalsIgnoreCase("y")) {
            System.out.println("\n1. Insert at Front");
            System.out.println("2. Insert at Rear");
            System.out.println("3. Delete at Front");
            System.out.println("4. Delete at Rear");
            System.out.println("5. Display From Front");
            System.out.println("6. Display From Rear");
            System.out.print("Enter your choice: ");
            int choice = Integer.parseInt(inp.readLine());

            switch (choice) {
                case 1:
                    System.out.print("Enter the data: ");
                    int frontData = Integer.parseInt(inp.readLine());
                    q.insertFront(frontData);
                    break;
                case 2:
                    System.out.print("Enter the data: ");
                    int rearData = Integer.parseInt(inp.readLine());
                    q.insertRear(rearData);
                    break;
                case 3:
                    q.deleteFront();
                    break;
                case 4:
                    q.deleteRear();
                    break;
                case 5:
                    q.displayFront();
                    break;
                case 6:
                    q.displayRear();
                    break;
                default:
                    System.out.println("Invalid choice!");
            }

            System.out.print("Enter y to continue: ");
            ch = inp.readLine();
        }
    }
}
