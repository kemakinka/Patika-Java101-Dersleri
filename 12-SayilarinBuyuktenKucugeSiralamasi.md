### Ödev 
Girilen 3 sayıyı "küçükten büyüğe" sıralayan programı yazınız.
```
import java.util.Scanner;

public class SayiSiralama {

	public static void main(String[] args) {
		// Girilen 3 sayıyı "küçükten büyüğe" sıralayan programı yazınız.

		int a, b, c;

		Scanner input = new Scanner(System.in);

		System.out.print("Birinci Sayı: ");
		a = input.nextInt();
		System.out.print("İkinci Sayı: ");
		b = input.nextInt();
		System.out.print("Üçüncü Sayı: ");
		c = input.nextInt();

		if (a > b && a > c) { // a, hem b hemde c den büyükse
			if (b > c) {
				System.out.println("a > b > c");
			} else {
				System.out.println("a > c > b");
			}
		} else if (b > a && b > c) { // b, hem c hemde a dan büyükse
			if (a > c) {
				System.out.println("b > a > c");
			} else {
				System.out.println("b > c > a");
			}
		} else if (c > a && c > b) { // c, hem a dan hemde b den büyüktse
			if (a > b) {
				System.out.println("c > a > b");
			} else {
				System.out.println("c > b > a");
			}
		}
	}

}

```
