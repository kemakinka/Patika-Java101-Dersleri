### Ödev
Java ile kullanıcının girdiği değerler ile üslü sayı hesaplayan programı "For Döngüsü" kullanarak yapınız.

```
import java.util.Scanner;

public class Application {

	public static void main(String[] args) {
		
		  int deger=1,sonuc=1;
		
	      Scanner input=new Scanner(System.in);
	      
	      System.out.print("Taban Sayısını Yazınız: ");
	      int taban = input.nextInt();
	      
	      System.out.print("Üs Sayısını Yazınız: ");
	      int us = input.nextInt();
	      
	      for(int i = 1; i<=us; i++) {
	    	  sonuc *=taban;
	      }
	      
	      System.out.println(taban+" ^ "+us+" = "+sonuc);
	      
	      
		
	}

}

```
