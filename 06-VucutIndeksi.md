```
import java.util.Scanner;

public class VucutKitliIndeksi {

	public static void main(String[] args) {
		/*
		 * Vücut Kitle İndeksi Hesaplama Java ile kullanıcıdan boy ve kilo değerlerini
		 * alıp bir değişkene atayın. Aşağıdaki formüle göre kullanıcının
		 * "Vücut Kitle İndeks" değerini hesaplayıp ekrana yazdırın.
		 * 
		 * Formül Kilo (kg) / Boy(m) * Boy(m)
		 */
		
		double kilo,boy,sonuc;
		
		Scanner scan = new Scanner(System.in);
		
		System.out.print("Lütfen boyunuzu (metre cinsinde) giriniz: ");
		kilo = scan.nextDouble();

		System.out.print("Lütfen kilonuzu giriniz:  ");
		boy = scan.nextDouble();
		
		sonuc = kilo/(boy*boy);
		
		System.out.println("Vücut Kitle İndeksiniz:"+ sonuc);
		
	}

}


```
