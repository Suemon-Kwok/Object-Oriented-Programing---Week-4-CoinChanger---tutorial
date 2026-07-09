/*
Object oriented programming Lab 4 question 3

Complete the CoinChanger class by:
1.	Declaring five private instance variables int ten, int twenty, int fifty, int oneDollar, int twoDollar that store the number of each kind of coin
2.	Writing the constructor method with input parameters for each instance variable, in the order written in item 1.
3.	Writing a get method for each of the instance variables
4.	Writing the int coinAsCents() method to calculate and return cent value of all coins according to the formula: ten*10 + twenty*20 + fifty*50 + oneDollar*100 + twoDollar*200 
5.	Writing the int dollars() method to return the value this.coinAsCents()/100
6.	Writing the int cents() method to return the integer remainder coinAsCents() % 100
Complete the main method by
1.	Using new to create a CoinChanger instance new CoinChanger(3,4,5,6,10)
2.	Printing the return value of the dollars() and cents() method in standard output formatting 
3.	Using new to create a CoinChanger instance new CoinChanger(12,54,1,2,40)
4.	Printing the return value of the dollars() and cents() method in standard output formatting
 
For example:
Test	Result
CoinChanger cc = new CoinChanger(3,4,5,6,10);
System.out.println(cc.getTen());
System.out.println(cc.getTwenty());
System.out.println(cc.getFifty());
System.out.println(cc.getOneDollar());
System.out.println(cc.getTwoDollar());	3
4
5
6
10

//Testing get methods

CoinChanger coinChanger = new CoinChanger(10, 20, 30, 40, 50);
System.out.println(coinChanger.getTen());
System.out.println(coinChanger.getTwenty());
System.out.println(coinChanger.getFifty());
System.out.println(coinChanger.getOneDollar());
System.out.println(coinChanger.getTwoDollar());	10
20
30
40
50

//Testing coinAsCents()

CoinChanger coinChanger = new CoinChanger(22, 1, 2, 40, 15);
System.out.println(coinChanger.coinAsCents());	7340
//Testing dollars()

CoinChanger coinChanger = new CoinChanger(6, 34, 9, 1, 0);
System.out.println(coinChanger.dollars());	12

//Testing cents()

CoinChanger coinChanger = new CoinChanger(90, 21, 4, 2, 55);
System.out.println(coinChanger.cents());	20

CoinChanger.main(new String[]{});	dollars = 29
cents = 60
dollars = 94
cents = 50


For example:
Test	Input	Result
ComputeSum.main(new String[]{});	2
3
5
6
-1	Please Enter a Number
Please Enter a Number
Please Enter a Number
Please Enter a Number
Please Enter a Number
16

ComputeSum.main(new String[]{});	-1	Please Enter a Number
0

ComputeSum.main(new String[]{});	2
3
4
-1	Please Enter a Number
Please Enter a Number
Please Enter a Number
Please Enter a Number
9

ComputeSum.main(new String[]{});	0
6
2
3
4
-9	Please Enter a Number
Please Enter a Number
Please Enter a Number
Please Enter a Number
Please Enter a Number
Please Enter a Number
15

//This import is necessary for your program to run in code validator
import java.lang.reflect.Field;

public class CoinChanger 
{
	//declare private instance variables
	
	//write constructor here
	
	//write get methods here
	
	//write int coinAsCents() method here
	
	//write int dollars() method here
	
	//write int cents() method here

	public static void main(String[] args)
	{
		//instantiate CoinChanger objects here
	}
}
*/





//This import is necessary for your program to run in code validator
import java.lang.reflect.Field;
public class CoinChanger 
{
    //declare private instance variables
    private int ten;
    private int twenty;
    private int fifty;
    private int oneDollar;
    private int twoDollar;
    
    //write constructor here
    public CoinChanger(int ten, int twenty, int fifty, int oneDollar, int twoDollar) {
        this.ten = ten;
        this.twenty = twenty;
        this.fifty = fifty;
        this.oneDollar = oneDollar;
        this.twoDollar = twoDollar;
    }
    
    //write get methods here
    public int getTen() {
        return ten;
    }
    
    public int getTwenty() {
        return twenty;
    }
    
    public int getFifty() {
        return fifty;
    }
    
    public int getOneDollar() {
        return oneDollar;
    }
    
    public int getTwoDollar() {
        return twoDollar;
    }
    
    //write int coinAsCents() method here
    public int coinAsCents() {
        return ten * 10 + twenty * 20 + fifty * 50 + oneDollar * 100 + twoDollar * 200;
    }
    
    //write int dollars() method here
    public int dollars() {
        return this.coinAsCents() / 100;
    }
    
    //write int cents() method here
    public int cents() {
        return coinAsCents() % 100;
    }
    
    public static void main(String[] args)
    {
        //instantiate CoinChanger objects here
        CoinChanger cc1 = new CoinChanger(3, 4, 5, 6, 10);
        System.out.println("dollars = " + cc1.dollars());
        System.out.println("cents = " + cc1.cents());
        
        CoinChanger cc2 = new CoinChanger(12, 54, 1, 2, 40);
        System.out.println("dollars = " + cc2.dollars());
        System.out.println("cents = " + cc2.cents());
    }
}
