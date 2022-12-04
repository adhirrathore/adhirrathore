import java.util.*;
public class insertion
{
	public static void main (String[]args)
	{
		Scanner sc=new Scanner(System.in);
		int index,value,size;
		System.out.println("Enter the size of an array");
		size=sc.nextInt();
		System.out.println("Enter the index on which number is need to be inserted");
		index=sc.nextInt();
		System.out.println("Enter the value which is to be inserted in an array at a given index");
		value=sc.nextInt();
		
		int a[]=new int[size];
		int b[]=new int[size+1];
		
		System.out.println("Enter the elements in an array");
		for(int i=0;i<size;i++) {
			a[i]=sc.nextInt();
		}
		System.out.println("Print the array");
		for(int i=0;i<size;i++) {
			System.out.print(" "+a[i]);
		}
		
		System.out.println("Print the updated array");
		for(int i=0;i<size+1;i++) {
			if(i<index) {
				b[i]=a[i];
			}
			else if(i==index) {
				b[i]=value;
			}
			else {
				b[i]=a[i-1];
			}
		}
		System.out.println("Elements after insertion are : ");
		for (int i=0;i<size+1;i++){
			System.out.print(" "+b[i]);
		}
	}
}
	 
