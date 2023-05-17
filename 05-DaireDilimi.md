```
import java.util.Scanner;

public class DaireCevresiVeAlani {
	public static void main(String[] args) {
		/*
		 * Yarıçapı r, merkez açısının ölçüsü 𝛼 olan daire diliminin alanı bulan
		 * programı yazınız.
		 * 
		 * 𝜋 sayısını = 3.14 alınız.
		 * 
		 * Formül : (𝜋 * (r*r) * 𝛼) / 360
		 */
		
		
		double pi = 3.14, yariCap,merkezAci,daireDilimi;
		
		Scanner input = new Scanner(System.in);
		
		System.out.print("Yarıçapı Giriniz: ");
		yariCap = input.nextDouble();
		
		System.out.println("Merkez Açısı: ");
		merkezAci = input.nextDouble();
		
		daireDilimi = (pi*(yariCap*yariCap)*merkezAci) /360;
		
		System.out.println("Yapı Çapı: "+yariCap);
		System.out.println("Merkez Açı: "+merkezAci);
		System.out.println("Olan Dairenin Dilimi: "+daireDilimi);
		
	}
}


```
