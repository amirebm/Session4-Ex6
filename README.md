//برنامه ایی بنویسید که صف را بصورت داینامیک پیاده سازی کند

# Session4-Ex6
package com.personal.Ex6;

import java.util.Scanner;

public class Ex6 {

	static Scanner sc;

	public static void main(String[] args) {

		
		System.out.println("Enter a the size of Enqueue");
		sc= new Scanner(System.in);
		int arrayLength=sc.nextInt();
		int temp;
		int[] ar= new int[arrayLength];
		
		System.out.println("Please enter "+ arrayLength+ " numbers for Enqueue:");
		
		
		ar[0]=sc.nextInt();
		for (int i = 1; i < ar.length; i++) {
			
			ar[i]=sc.nextInt();
		}
		temp=ar[ar.length-1];
		printArray(ar);

		while(temp!=0) {
			System.out.println("add new num to the Enqueue or press 0 to exit");
			temp=sc.nextInt();
			addToEnqueue(ar, temp);
			printArray(ar);

		}
		System.exit(0);	
		}
	
	static public void addToEnqueue(int[] ar,int temp) {
	
    for (int i = 0; i < ar.length-1; i++) {
    	       	
    	ar[i]=ar[i+1];
		
  	}
    ar[ar.length-1]=temp;
	} 
		
	
	static void printArray(int arr[])
	{
	    int n = arr.length;
	    for (int i=0; i<n; ++i)
	        System.out.print(String.format("a[%d]=%d\t", i,arr[i]));
	    System.out.println();
	}


}
