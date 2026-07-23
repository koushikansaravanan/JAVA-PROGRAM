# JAVA-PROGRAM

binary search 

import java.io.*;
import java.util.Scanner;
public class binary
{
public static void main (String args[])
{
int size,i,search,first,last,middle;
int arr[]=new int[20];
Scanner s=new Scanner(System.in);
System.out.print("enter the number of elements:");
size=s.nextInt();
System.out.print("enter"+size+"elements(asceding):");
for(i=0;i<size;i++)
  arr[i]=s.nextInt();
System.out.print("enter the number of elements to search:");
 search=s.nextInt();
first=0;
last=size-1;
middle=(first+last)/2;
while (first<last)
{
if (arr[middle]<search)
{
first=middle+1;
}
else if(arr[middle]==search)
{
 System.out.print("the element is available at index no."+(middle+1));
break;
}
else
{
last=middle-1;
}
middle=(first+last)/2;
}
if(first>last)
{
 System.out.print("the element is not found!");
}
}
}

**bubble search**

import java.io.*;
import java.util.*;
public class bubble
{
public static void main (String args[])
{
Scanner s=new Scanner(System.in);
int size,i,j;
System.out.print("enter the limits :");
size=s.nextInt();
int arr[]=new int[size];
System.out.print("enter"+size+"elements :");
for(i=0;i<size;i++)
{
arr[i]=s.nextInt();
}
for(i=0;i<(size-1);i++)
{
for(j=0;j<(size-1);j++)
{
if(arr[j]>arr[j+1])
{
int x;
x=arr[j];
arr[j]=arr[j+1];
arr[j+1]=x;
}
}
}
System.out.print("the new sorted array:");
for(i=0;i<size;i++)
System.out.print(""+arr[i]);
}
}

**binary tree**
class Node

{ int data;
 Node left, right;
 Node(int d)

{

data=d;

left=right=null;

}

}

class BinaryTree

{

Node tree,root;

public static void main(String args[])

{

BinaryTree tree=new BinaryTree();

tree.root=new Node(1);

tree.root.left=new Node(2);

tree.root.right=new Node(3);

tree.root.left.left=new Node(4);

tree.root.left.right=new Node(5);

tree.root=null;

System.out.print("\n\ntree deleted!\n\n\n");

}

void deleteTree(Node node)

{

root=null;

} void deleteTreeRef(Node nodeRef)

{

nodeRef=null; 
}
}

**insectionsort**

import java.util.*;
class insertionsort
{
public static void main(String args[])
{
Scanner scan=new Scanner(System.in);
System.out.print("\n\t\t INSERTION SORT");
System.out.print("\n\n enter the size of array:");
int n,element;
n=scan.nextInt();
int arr[]=new int[n];
int j;
System.out.print("enter the elements :");
for(int i=0;i<n;i++)
{
arr[i]=scan.nextInt();
}
for(int i=0;i<n;i++)
{
element=arr[i];
for(j=(i-1);j>=0 && (arr[j]>element);j--)
{
arr[j+1]=arr[j];

arr[j+1]=element;
}
}
System.out.print("the new sorted array is ");
for(int i=0;i<n;i++)
System.out.print(arr[i]+"");
System.out.print("\n");
}
}

**linear search**
import java.io.*;
import java.util.Scanner;
public class linear
{
public static void main (String args[])
{
Scanner s=new Scanner(System.in);
int size,i,pos=0;
System.out.print("Enter the limit of elements:");
size=s.nextInt();
int arr[]=new int [size];
System.out.print("Enter the elements:");
for(i=0;i<size;i++)
arr[i]=s.nextInt();
System.out.print("Enter the elements to search:");
int num=s.nextInt();
for(i=0;i<size;i++)
{
if(arr[i]==num)
{
pos=i+1;
break;
}
}if(pos==0)
{
System.out.print("The elements not found:");
}
else
{
System.out.print("The elements found at position:"+pos);
}
}
}

**linkedlist**

import java.io.*;
import java.util.*;
public class linkedlist
{
public static void main(String args[])
{
LinkedList<Integer>list=new LinkedList<Integer>();
Scanner s=new Scanner(System.in);
int size,i,n;
System.out.print("enter the size of linkedlist:");
size=s.nextInt();
System.out.print("enter"+size+"elements:");
for(i=0;i<size;i++)
{
n=s.nextInt();
list.add(n);
}
System.out.print("\n the elements in the list:"+list);
if(!list.isEmpty())
{
System.out.println("\n the elements in the 1st index (0-based):"+list.get(1));
System.out.println("\n the first elements :"+list.getFirst());
System.out.println("\n the last elements :"+list.getLast());
}else{
System.out.println("the list is empty.");
}
s.close();
}
}

**priorityqueue**

import java.io.*;
import java.util.*;
public class priorityqueue
{
public static void main(String args[])
{
PriorityQueue<Integer> pq =new PriorityQueue<Integer>();
Scanner s=new Scanner(System.in);
int size,i,n;

System.out.print("enter the size of priority queue:");
size= s.nextInt();

System.out.print("enter "+size+"elements:");
for(i=0;i<size;i++)
{
n=s.nextInt();
pq.add(n);
}
System.out.println("\n the element with top priority:"+pq.peek());
System.out.println("\n the top element is romoved :"+pq.poll());
System.out.println("\n the new top priority element:"+pq.peek());

s.close();
}
}

**queue**

import java.io.*;
import java.util.*;
class queue
{
public static void main (String args[])
{
Queue<Integer>queue=new LinkedList<>();
Scanner s=new Scanner (System.in);
int[] arr=new int[30];
System.out.print("\n enter the element limit to add in queue :");
int n;
n=s.nextInt();
System.out.print("\n enter the elements :");
for(int i=0;i<n;i++)
{
arr[i]=s.nextInt();
queue.add(arr[i]);
}
System.out.print("\n the queue contents :"+queue);
System.out.print("\n peek(): head of the queue:"+queue.peek());
System.out.print("\n poll(): returnedhead of the queue:"+queue.poll());
System.out.print("\n the queue contents :"+queue);
}
}

**selection**

import java.util.Scanner;
public class selection
{
public static void main(String[] args)
{
 int tot,i,j,count,small,index=0,x;
Scanner scan=new Scanner(System.in);
System.out.print("enter the size of arrays :");
tot=scan.nextInt();
int[]arr=new int[tot];
System.out.print("enter "+tot+"elements for the arrays :");
for (i=0;i<tot;i++)
{
arr[i]=scan.nextInt();
}
for(i=0;i<(tot-1);i++)
{
count=0;
small=arr[i];
for(j=(i+1);j<tot;j++)
{
if(small>arr[j])
{
small=arr[j];
count++;
index=j;
}
}
if(count!=0)
{
x=arr[i];
arr[i]=small;
arr[index]=x;
}
}
System.out.println("\n the new sorted array is:");
for(i=0;i<tot;i++)
 
System.out.print(arr[i]+" ");
System.out.print("\n");
}
}







