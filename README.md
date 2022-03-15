# Sum-First-And-Last-Digits

This projects adds both the first and last digits of any given numbers and returns the sum. it returns -1 for negative numbers.

public class FirstLastDigitSum {
    public static int ERROR_MESSAGE = -1;
    
    public static int sumFirstAndLastDigit(int num) {
    
        if(num < 0) {
            return ERROR_MESSAGE;
        }
        
        int addSingleNumbers = num + num;
        if (num < 10) {return addSingleNumbers; }
        
        int sum = 0;
        int lastNum = num % 10;

        while(num > 0) {
            num /= 10;
            if(num <= 9) {
                sum += lastNum;
                sum += num;
                break;
            }
        }
        
        return sum;
    }
    
    public static void main(String[] args) {
        System.out.println(sumFirstAndLastDigit(109836020));
    }
}
