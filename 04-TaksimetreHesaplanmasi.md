```
import java.util.Scanner;

public class TaksiMetre {

	public static void main(String[] args) {
		/*
		 * Java ile gidilen mesafeye (KM) göre taksimetre tutarını ekrana yazdıran
		 * programı yazın.
		 * 
		 * Taksimetre KM başına 2.20 TL tutmaktadır. Minimum ödenecek tutar 20 TL'dir.
		 * 20 TL altında ki ücretlerde yine 20 TL alınacaktır. Taksimetre açılış ücreti
		 * 10 TL'dir.
		 *  10+(mesafe*2.20)
		 */
		
	  // Verilerin Tanımlanması
		double gidilenMesafe, kmBasi =2.30, minimumTutar = 20, acilisUcreti = 10,toplamTutar;
		
		Scanner input = new Scanner(System.in);
		
    //Kullanıcıdan Km Bilgisi Alınması
		System.out.print("Gidilen Mesafeyi Giriniz (km): ");
		gidilenMesafe = input.nextDouble();
		
    //Tutar Hesaplanması
		toplamTutar =(gidilenMesafe*2.20)+acilisUcreti;
		
    //İşlemler
		if(toplamTutar < minimumTutar) {
			System.out.println("Toplam Tutar: "+minimumTutar);
		}else {
			System.out.println("Toplam Tutar: "+toplamTutar);
		}
		
		
		
	}
}


```
