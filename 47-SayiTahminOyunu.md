### Java ile Sayı Tahmin Oyunu
```
import java.util.Random;
import java.util.Scanner;

public class SayiTahminOyunu {

	public static void main(String[] args) {

		Random rand = new Random();
		int randomSayisi = rand.nextInt(1);
		Scanner input = new Scanner(System.in);

		int tahminHakki = 1;
		while (tahminHakki <= 3) {
			System.out.print("Lütfen (0-100) arasında bir tahmin giriniz: ");
			int tahminSayisi = input.nextInt();

			if (tahminSayisi < 0 || tahminSayisi > 101) {
				continue;
			}

			if (tahminSayisi == randomSayisi) {
				System.out.println("Tebrikler, Doğru Tahmin");
				break;
			} else {
				System.out.println("Malesef, Yanlış Tahmin");
				System.out.println("Tahmin Hakkınız: (" + tahminHakki + "/3)\n");
				if (tahminHakki == 3) {
					System.out.println("Tahmin Hakkınız Bitti (3/3)");
					break;
				}

				tahminHakki++;
			}
		}

	}

}


```
