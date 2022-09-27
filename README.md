# count-1-using-binary-search
 import java.util.*;
import java.lang.*;
import java.io.*;

public class Main
{
	public static void main (String[] args) throws java.lang.Exception
	{
                Scanner sc=new Scanner(System.in);
                int n=sc.nextInt();
                int arr[]=new int[n];
                for(int i=0;i<n;i++){
                        arr[i]=sc.nextInt();
                }
                System.out.println(check(arr,n));
                // int count=0;
                // for(int i=0;i<n;i++){
                //         if(arr[i]==1){
                //                 count++;
                //         }
                // }
                // System.out.println(count);
	}
        public static int check(int []arr ,int n){
                n=arr.length;
                int l=0;
                int r=n-1;
                int mid;
                while(l<=r){
                        mid=(l+r)/2;
                        if(arr[mid]<1){
                                r=mid-1;
                        }
                        //else if(arr[mid]>1){
                            //            l=mid+1;
                                //}
                        
                           else{
                                if(mid==n-1 || arr[mid+1]!=1){
                                        return mid+1;
                                }
                                else{
                                        l=mid+1;
                                }
                        }
                }
                
           return 0;     
        }
}
