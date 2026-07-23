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





