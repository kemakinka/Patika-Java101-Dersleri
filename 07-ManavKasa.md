## Manav Kasa Programı
#### Java ile kullanıcıların manavdan almış oldukları ürünlerin kilogram değerlerine göre toplam tutarını ekrana yazdıran programı yazın.
##### Meyveler ve KG Fiyatları
- Armut : 2,14 TL
- Elma : 3,67 TL
- Domates : 1,11 TL
- Muz: 0,95 TL
- Patlıcan : 5,00 TL     
```
import java.util.Scanner;

public class ManavKasa {

	public static void main(String[] args) {
	

		double armutFiyat = 2.14, elmaFiyat = 3.67, domatesFiyat = 1.11, muzFiyat = 0.95, patlicanFiyat = 5.00;

		Scanner input = new Scanner(System.in);

		System.out.print("Armut Kaç Kilo? ");
		double armut = input.nextDouble();
		System.out.print("Elma Kaç Kilo? ");
		double elma = input.nextDouble();
		System.out.print("Domates Kaç Kilo? ");
		double domates = input.nextDouble();
		System.out.print("Muz Kaç Kilo? ");
		double muz = input.nextDouble();
		System.out.print("Patlican Kaç Kilo? ");
		double patlican = input.nextDouble();

		double hesap = (armut * armutFiyat) + (elma * elmaFiyat) + (domates * domatesFiyat) + (muz * muzFiyat)
				+ (patlican * patlicanFiyat);

		System.out.println("Toplam: " + hesap +" TL");

	}

}

```
