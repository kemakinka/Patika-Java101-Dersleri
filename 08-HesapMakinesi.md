```
import java.util.Scanner;

public class HesapMakinesi {

	public static void main(String[] args) {
		int sayi1, sayi2, islem;

		Scanner input = new Scanner(System.in);

		System.out.println("[1]-Topla\n[2]-Çıkar\n[3]-Çarp\n[4]-Böl");
		System.out.print("İşlem Seçiniz:");
		islem = input.nextInt();

		System.out.print("Birinci Sayı: ");
		sayi1 = input.nextInt();
		System.out.print("İkinci Sayı: ");
		sayi2 = input.nextInt();

		switch (islem) {
		case 1:
			System.out.println("Sonuç: "+sayi1 + " + " + sayi2 + " = " + (sayi1 + sayi2));
			break;

		case 2:
			System.out.println("Sonuç: "+sayi1 + " - " + sayi2 + " = " + (sayi1 - sayi2));
			break;

		case 3:
			System.out.println("Sonuç: "+sayi1 + " x " + sayi2 + " = " + (sayi1 * sayi2));
			break;

		case 4:
			System.out.println("Sonuç: "+sayi1 + " / " + sayi2 + " = " + (sayi1 / sayi2));
			break;

		default:
			System.out.println("Lütfen İşlem Seçiniz.");
			break;
		}

	}

}


```
