### Java ile klavyeden girilen N tane sayma sayısından en büyük ve en küçük sayıları bulan ve bu sayıları ekrana yazan programı yazın.

```
import java.util.Scanner;

public class Application {

	public static void main(String[] args) {
		  Scanner input = new Scanner(System.in);

	        int numCount = 1;
	        do {
	            if(numCount <= 0) System.out.println("Hatalı Veri Giriniz!");

	            System.out.print("Kaç adet sayı girmek istersiniz: ");
	            numCount = input.nextInt();
	        }while(numCount < 0);

	        int maxNum = Integer.MIN_VALUE;
	        int minNum = Integer.MAX_VALUE;
	        for(int i = 0; i < numCount; i++)
	        {
	            System.out.print("Bir Numara Girin: ");
	            int currentNum = input.nextInt();
	            if(currentNum > maxNum) maxNum = currentNum;
	            if(currentNum < minNum) minNum = currentNum;
	        }
	        
	        System.out.println("en Büyük Numara: " + maxNum + "\nEn Küçük Numara: " + minNum);
	}

}

```
