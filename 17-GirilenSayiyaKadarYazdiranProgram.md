### Java döngüler ile 0'dan girilen sayıya kadar olan sayılardan 3 ve 4'e tam bölünen sayıların ortalamasını hesaplayan programı yazınız.

```
import java.util.Scanner;

public class Application {

	public static void main(String[] args) {
		/*
		 * Ödev Java döngüler ile 0'dan girilen sayıya kadar olan sayılardan 3 ve 4'e
		 * tam bölünen sayıların ortalamasını hesaplayan programı yazınız.
		 */

		Scanner input = new Scanner(System.in);
		System.out.print("Bir Sayı Giriniz: ");

		int girilenSayi = input.nextInt();
		int count = 0;
		double ortalama;
		int toplam = 0;

		for (int i = 0; i < girilenSayi; i++) {
			if (i % 3 == 0 && i % 4 == 0) {
				count++;
				toplam += i;
			}
		}

		ortalama = toplam / count;
		System.out.println(ortalama);

	}

}

```
