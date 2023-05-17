### Koşullar :
- Sıcaklık 5'dan küçük ise "Kayak" yapmayı öner.
- Sıcaklık 5 ve 15 arasında ise "Sinema" etkinliğini öner.
- Sıcaklık 15 ve 25 arasında ise "Piknik" etkinliğini öner.
- Sıcaklık 25'ten büyük ise "Yüzme" etkinliğini öner.
### Ödev
Aynı örnek üzerinden if koşulları başka hangi şekilde oluşturulabilirdi farklı çözüm yolları bulunuz.
```
import java.util.Scanner;

public class HavaSicakligi {
	public static void main(String[] args) {

		Scanner input = new Scanner(System.in);
		int hava;

		System.out.print("Hava sıcaklığını dahil ediniz: ");
		heat = input.nextInt();

		if (hava < 5) {
			System.out.print("Kayak yapabilirsiniz");
		} else if (hava >= 5 && hava < 10) {
			System.out.print("Sinemaya gidebilirsiniz");
		} else if (hava >= 10 && hava <= 15) {
			System.out.print("Hem sinemaya hem de pikniğe gidebilirsiniz");
		} else if (hava > 15 && hava <= 25) {
			System.out.print("Pikniğe gidebilirsiniz");
		} else {
			System.out.print("Yüzmeye gidebilirsiniz");
		}
	}
}
```
