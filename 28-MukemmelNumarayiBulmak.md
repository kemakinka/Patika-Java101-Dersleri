### Mükemmel Sayı Nedir ?
Bir sayının kendisi hariç pozitif tam sayı çarpanları (kalansız bölen sayıların) toplamı kendisine eşit olan sayıya mükemmel sayı denir.

```
import java.util.Scanner;

public class Application {

	public static void main(String[] args) {
		   int n,i,counter=0;
	        Scanner input = new Scanner(System.in);
	        System.out.print("Bir Numara Girin: ");
	        n = input.nextInt();

	        for(i=1; i<n; i++){
	            if(n%i == 0){
	                counter+=i;
	            }
	        }
	        if(counter == n){
	            System.out.print("Girdiğin " + n + " sayisi mükemmel sayidir.");
	        }
	        else{
	            System.out.print("Girdiğin  " + n +" sayisi mükemmel sayi Değildir! ");
	        }
	}

}

```
