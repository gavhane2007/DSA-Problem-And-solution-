#include <iostream>
#include <string>
using namespace std;

// Node of Linked List
struct Node
{
    int orderID;
    string customerName;
    string foodName;
    Node* next;
};

// Head pointer
Node* head = NULL;

// Function to add a new order
void addOrder()
{
    Node* newNode = new Node;

    cout << "\nEnter Order ID: ";
    cin >> newNode->orderID;

    cout << "Enter Customer Name: ";
    cin >> newNode->customerName;

    cout << "Enter Food Name: ";
    cin >> newNode->foodName;

    newNode->next = NULL;

    // If list is empty
    if (head == NULL)
    {
        head = newNode;
    }
    else
    {
        Node* temp = head;

        // Move to last node
        while (temp->next != NULL)
        {
            temp = temp->next;
        }

        // Connect new node
        temp->next = newNode;
    }

    cout << "\nOrder added successfully!\n";
}


// Function to display all orders
void displayOrders()
{
    if (head == NULL)
    {
        cout << "\nNo pending orders.\n";
        return;
    }

    Node* temp = head;

    cout << "\n========== FOOD ORDER LIST ==========\n";

    while (temp != NULL)
    {
        cout << "\n+---------------------------+\n";
        cout << "| Order ID  : " << temp->orderID << endl;
        cout << "| Customer  : " << temp->customerName << endl;
        cout << "| Food      : " << temp->foodName << endl;
        cout << "+---------------------------+\n";

        if (temp->next != NULL)
        {
            cout << "             |\n";
            cout << "             v\n";
        }

        temp = temp->next;
    }

    cout << "             |\n";
    cout << "            NULL\n";
}


// Function to place/complete first order
void placeOrder()
{
    if (head == NULL)
    {
        cout << "\nNo orders available.\n";
        return;
    }

    Node* temp = head;

    cout << "\n========== ORDER COMPLETED ==========\n";
    cout << "Order ID : " << temp->orderID << endl;
    cout << "Customer : " << temp->customerName << endl;
    cout << "Food     : " << temp->foodName << endl;

    // Move head to next node
    head = head->next;

    // Delete old first node
    delete temp;

    cout << "\nOrder placed successfully!\n";
}


// Main function
int main()
{
    int choice;

    do
    {
        cout << "\n\n====================================\n";
        cout << "     FOOD ORDER MANAGEMENT SYSTEM\n";
        cout << "       USING LINKED LIST\n";
        cout << "====================================\n";

        cout << "\n1. Add New Order";
        cout << "\n2. Display Orders";
        cout << "\n3. Place / Complete Order";
        cout << "\n4. Exit";

        cout << "\n\nEnter your choice: ";
        cin >> choice;

        switch (choice)
        {
            case 1:
                addOrder();
                break;

            case 2:
                displayOrders();
                break;

            case 3:
                placeOrder();
                break;

            case 4:
                cout << "\nThank you for using Food Order Management System!\n";
                break;

            default:
                cout << "\nInvalid choice! Please try again.\n";
        }

    } while (choice != 4);

    return 0;
}
