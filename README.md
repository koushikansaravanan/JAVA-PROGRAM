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
