### SINIF GEÇME DURUMU
Dersler : Matematik, Fizik, Türkçe, Kimya, Müzik
Geçme Notu : 55
### Ödev
Eğer girilen ders notları 0 veya 100 arasında değil ise ortalamaya katılmasın.
```
import java.util.Scanner;

public class NotOrtalamasi {

	public static void main(String[] args) {

		int matematik, fizik, kimya, turkce, tarih, muzik;
		Scanner not = new Scanner(System.in);

		System.out.println("Matematik Notunuz: ");
		matematik = not.nextInt();

		System.out.println("Fizik Notunuz: ");
		fizik = not.nextInt();
		
		System.out.println("Türkçe Notunuz: ");
		turkce = not.nextInt();
		
		System.out.println("Kimya Notunuz: ");
		kimya = not.nextInt();

		System.out.println("Müzik Notunuz: ");
		muzik = not.nextInt();

		double ortalama = (matematik + fizik + kimya + turkce + muzik) / 5;
		
		if(ortalama <0 || ortalama > 100) {
			System.out.println("Notunuz, 0 ile 100 arasında olmadığından ortalamaya katılamadınız.");
		}else {
			System.out.println("Not Ortalamanız: "+ortalama);
		}

	}

}

```
