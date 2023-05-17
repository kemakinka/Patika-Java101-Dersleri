### Java döngüler ile tek bir sayı girilene kadar kullanıcıdan girişleri kabul eden ve girilen değerlerden çift ve 4'ün katları olan sayıları toplayıp ekrana basan programı yazıyoruz.
```
import java.util.Scanner;

public class Application {

	public static void main(String[] args) {
		/*
		 * Java döngüler ile tek bir sayı girilene kadar kullanıcıdan girişleri kabul
		 * eden ve girilen değerlerden çift ve 4'ün katları olan sayıları toplayıp
		 * ekrana basan programı yazıyoruz.
		 */

		Scanner input = new Scanner(System.in);

		int toplam = 0;

		while (true) {
			System.out.print("Sayı Giriniz: ");
			int sayi = input.nextInt();
			if (sayi % 2 != 0) {
				System.out.println("Tekil bir sayı girdiniz.");
				break;
			}
			if (sayi % 2 == 0 && sayi % 4 == 0) {
				toplam += sayi;
				System.out.println(toplam);
			}

		}

	}

}

```
