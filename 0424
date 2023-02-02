#include <iostream>
using namespace std;

//Create Node
struct node{
    int element;
    node *next;
  };	

//Create Linked List Class
class LinkedList {
private:
  node *front, *back;
public:
//Basic Constructor
  LinkedList() {
      front=NULL;
      back=NULL;
  }

//Add to Front
  void PushFront(int key){
    node *temp=new node;
    temp->element=key;
    temp->next=front;
    front=temp;
  }

//Return Front Item
  void TopFront(){
    node *temp=new node;
    temp=front;
    cout<<temp->element<<"\t"<<endl;
  }

//Remove Front Item
  void PopFront(){
    node *temp=new node;
    temp=front;
    front=front->next;
    delete temp;
  }

//Add to Back
  void PushBack(int key){
    node *pre=new node;
    node *cur=new node;
    node *temp=new node;
    cur=front;
    for(int i=1;i<(Size()+1);i++){
      pre=cur;
      cur=cur->next;
    }
    temp->element=key;
    pre->next=temp;	
    temp->next=cur;
  }

//Return Back Item
  void TopBack(){
    node *temp=new node;
    temp=front;
    for(int i=1;i<Size();i++){
      temp=temp->next;
    }
    cout<<temp->element<<"\t"<<endl;
  }

//Remove Back Item
  void PopBack(){
    node *current=new node;
    node *previous=new node;
    current=front;
    while(current->next!=NULL){
      previous=current;
      current=current->next;	
    }
    back=previous;
    previous->next=NULL;
    delete current;
  }

//Is key in list?
  bool FindKey(int key){
    node *temp=new node;
    temp=front;
    for(int i = 0; i < Size(); i++){
      if (temp->element == key) {
        return true;
      }
      temp=temp->next;
    }
    return false;
  }

//Enpty List?
  bool Empty(){
    if (Size() == 0){
      return 1;
    }
    return 0;
  }

//Add Key Before Node
  void AddBefore(int nod, int key){
    node *pre=new node;
    node *cur=new node;
    node *temp=new node;
    cur=front;
    for(int i=0;i<nod;i++){
      pre=cur;
      cur=cur->next;
    }
    temp->element=key;
    pre->next=temp;	
    temp->next=cur;
  }

//Add Key After Node
  void AddAfter(int nod, int key){
    nod++;
    node *pre=new node;
    node *cur=new node;
    node *temp=new node;
    cur=front;
    for(int i=0;i<nod;i++){
      pre=cur;
      cur=cur->next;
    }
    temp->element=key;
    pre->next=temp;	
    temp->next=cur;
  }

//Print all the elements of the list
  void DisplayAll() {
    node *temp=new node;
    temp=front;
    for(int i=0;i<Size();i++){
      cout<<temp->element<<"\t";
      temp=temp->next;
    }
    cout<<endl;
  } 

// Return the number of Elements
  int Size(){
    int sum = 0;
    node *temp=new node;
    temp=front;
    while(temp!=NULL) {
      sum++;
      temp=temp->next;
    }
    return sum;
  }

//Overwrite the key to a given node
  void ReplaceKey(int nod, int key){
    node *current=new node;
    node *previous=new node;
    current=front;
    for(int i=0;i<nod;i++){
      previous=current;
      current=current->next;
    }
    previous->next=current->next;
    AddBefore(nod, key);
  }
};

int main() {
  LinkedList list;
  //Create Initial List
  list.PushFront(25);
  list.PushFront(50);
  list.PushFront(90);
  list.PushFront(40);
  list.PushBack(35);
  //Output
  list.DisplayAll();

  //Determine first and last item
  list.TopFront();
  list.TopBack();
  //Delete First Item
  list.PopFront();
  //Output
  list.DisplayAll();

  //Delete Last Item
  list.PopBack();
  //Output
  list.DisplayAll();

  //Add Items to Back
  list.PushBack(10);
  list.PushBack(12);
  list.PushBack(14);
  //Output
  list.DisplayAll();

  //Check FindKey command and Empty command
  cout<< list.FindKey(25)<<endl;
  cout<< list.FindKey(6)<<endl;
  cout<< list.Empty()<<endl;

  //Add Item
  list.AddBefore(3,94);
  //Output
  list.DisplayAll();

  //Add Item
  list.AddAfter(2,5);
  //Output
  list.DisplayAll();

  //Output Size
  cout<<list.Size()<<endl;
  //Replace and Output
  list.ReplaceKey(6,87);
  list.DisplayAll();

  //Delete All from List
  list.PopFront();
  list.PopFront();
  list.PopFront();
  list.PopFront();
  list.PopFront();
  list.PopFront();
  list.PopFront();
  list.PopFront();

  //Determine if Empty
  cout<< list.Empty()<<endl;
}
