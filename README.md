# spe-skill-test
software engineer skill test a

// C# program for checking 
// of Narcissistic number 
using System; 
  
class narcissistic 
{ 
  
    // function to count digits 
    int countDigit(int n) 
    { 
        if (n == 0) 
            return 0; 
      
        return 1 + countDigit(n / 10); 
    } 
      
    // Returns true if n is Narcissistic number 
    bool check(int n) 
    { 
        // count the number of digits 
        int l = countDigit(n); 
        int dup = n; 
        int sum = 0; 
      
        // calculates the sum of  
        //digits raised to power 
        while(dup > 0)  
        { 
            sum += (int)Math.Pow(dup % 10, l); 
            dup /= 10; 
        } 
      
        return (n == sum); 
    } 
      
    // Driver code  
    public static void Main() 
    { 
        narcissistic obj = new narcissistic(); 
        int n = 1634; 
        if (obj.check(n)) 
            Console.WriteLine("yes"); 
        else
            Console.WriteLine("no"); 
    } 
} 
  
// This code is contributed by vt_m.
