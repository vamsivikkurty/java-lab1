# java-lab1
Question 1: Write a JAVA program to calculate the average value of an array elements.

Code:
import java.util.Scanner;
public class array_avg
{
    public static void main(String[] args)
    {
        System.out.println("\nName:vikkurty vamsi           Reg.no:20BCE1066\n");
        Scanner scan = new Scanner(System.in);
        int[] arr = new int[5];
        System.out.println("Enter " + arr.length + " integer values:");
        for(int i=0; i < arr.length; i++)
        {
            arr[i] = scan.nextInt();
        }
        float sum = 0,avg = 0;
        for (int i=0; i < arr.length; i++)
        {
            sum = sum + arr[i];
        }
        avg = sum / arr.length;
        System.out.println("The average is " + avg);

    }
}

Question 2 : Write a JAVA program to copy an array by iterating the array

 Code : 

import java.util.Scanner;
public class copy_arr
{
    public static void main(String[] args)
    {

        Scanner scan = new Scanner(System.in);
        int[] arr = new int[5];
        System.out.println("Enter " + arr.length + " integer values:");
        for(int i=0; i < arr.length; i++)
        {
            arr[i] = scan.nextInt();
        }

        int[] arr_new = new int[5];

        for(int i=0; i < arr_new.length; i++)
        {
            arr_new[i] = arr[i];
        }
        System.out.println("Array elements tha are:");
        for (int i=0; i < arr.length; i++)
        {
            System.out.print(arr_new[i]+"\t");
        }

    }
}




Question 3 : Write a JAVA program to find the number of even and odd integers in a given array.

 Code :

import java.util.Scanner;
public class even_odd_arr
{
    public static void main(String[] args)
    {

        Scanner scan = new Scanner(System.in);
        int[] arr = new int[5];
        System.out.println("Enter " + arr.length + " integer values:");
        for(int i=0; i < arr.length; i++)
        {
            arr[i] = scan.nextInt();
        }
        int even = 0,odd = 0;
        for (int i=0; i < arr.length; i++)
        {
            if (arr[i] % 2 == 0)
            {
                even = even + 1;
            }
            else
            {
                odd = odd + 1;
            }
        }

        System.out.println("The number of even integers are " + even);
        System.out.println("The number of odd integers are " + odd);

    }
}



Question 4 : Write a JAVA program to print an array after changing the rows and columns of a given two-dimensional array

Code :

import java.util.Scanner;
public class row_col_arr
{
    public static void main(String[] args)
    {
        int[][] twodm = {
                {11, 22, 33},
                {44, 55, 66}
        };
        System.out.print("Original Array:\n");
        print_array(twodm);
        System.out.print("After changing the rows and columns of the said array: \n");
        transpose(twodm);
    }

    private static void transpose(int[][] twodm)
    {

        int[][] newtwodm = new int[twodm[0].length][twodm.length];

        for (int i = 0; i < twodm.length; i++)
        {
            for (int j = 0; j < twodm[0].length; j++)
            {
                newtwodm[j][i] = twodm[i][j];
            }
        }

        print_array(newtwodm);
    }
    private static void print_array(int[][] twodm)
    {
        for (int i = 0; i < twodm.length; i++)
        {
            for (int j = 0; j < twodm[0].length; j++)
            {
                System.out.print(twodm[i][j] + " ");
            }
            System.out.println();
        }

    }
}


Question 5 : Write a JAVA program to compute the average value of an array of integers except the largest and the smallest values. 

Code :
import java.util.Scanner;
public class avg_wo_largest_smallest
{
    public static void main(String[] args)
    {

        Scanner scan = new Scanner(System.in);
        int[] arr = new int[5];
        System.out.println("Enter " + arr.length + " integer values:");
        for(int i=0; i < arr.length; i++)
        {
            arr[i] = scan.nextInt();
        }
        int min = 0,max = 0;
        max = arr[0];
        min = arr[0];
        for (int i=0; i < arr.length; i++)
        {
            if (arr[i]>max)
            {
                max = arr[i];
            }
            if (arr[i]<min)
            {
                min = arr[i];
            }
        }
        float sum = 0,avg_req =0;
        for (int i=0; i < arr.length; i++)
        {
            sum = sum + arr[i];
        }
        avg_req = (sum - max - min) / (arr.length - 2);

        System.out.println("The average excluding the largest and smallest is " + avg_req);

    }
}


