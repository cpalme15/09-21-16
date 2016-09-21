# 09-21-16
/* Programmer:Collin Palmer
 * Date:09/21/16
 * COSC 111
 */

   package classwork2;
   import java.util.*;
   import java.io.FileInputStream;
   import java.io.FileNotFoundException;
   public class Classwork2 {

   public static void main(String[] args) {
	Scanner k =null;
	//variables here
	int num = 0;
	int box=0;
	int gondola=0;
	int passenger=0;
	int totaltrain=0;
	final int N=1000;
	final int boxlimit=60;
	try
	{
	k = new Scanner(new FileInputStream("myinput.txt"));
	}
	catch (FileNotFoundException e)
	{
    e.printStackTrace();
    }
	//input section
	num = k.nextInt();
    box=k.nextInt();
	gondola=k.nextInt();
	passenger=k.nextInt();
		 
    //process section(calculations)
	totaltrain=box+gondola+passenger;
	if (totaltrain > N)
	{
		System.out.println("The train is very long");
	}
	else
	{
	System.out.println("The train is short");	
	}
	if (box>=boxlimit)
		System.out.println("you passed the test");
	else 
		System.out.println("You failed the test");
    System.out.println("The number is "+num);//output section
    System.out.println("\t Box cars number is "+box);
    System.out.println("\t gondola cars number is "+gondola);
	System.out.println("\t passenger cars number is "+passenger);
	System.out.println("The total is "+totaltrain);
	k.close();
	}
	 
}
