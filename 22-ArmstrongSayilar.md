### Armstrong Sayı Nedir ?
N haneli bir sayının basamaklarının n’inci üstlerinin toplamı, sayının kendisine eşitse, böyle sayılara Armstrong sayı denir.

### Ödev
Bir sayının basamak sayılarının toplamını hesaplayan program yazınız.
```
import java.util.Scanner;

public class Application {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Bir sayi giriniz : ");
        int number = input.nextInt();
        int basamakSayac = 0;
        int tempNumber = number;
        int basamakDegeri;
        int sonuc = 0;
        int basamakUssu;

        while (tempNumber != 0) {
            tempNumber /= 10;
            basamakSayac++;
        }

        tempNumber = number;

        while (tempNumber != 0) {
            basamakDegeri = tempNumber % 10;
            basamakUssu = 1;
            for (int i = 1; i <= basamakSayac; i++) {
                basamakUssu *= basamakDegeri;
            }
            sonuc += basamakUssu;
            tempNumber /= 10;
        }
        if (sonuc == number) {
            System.out.println(number + " Armstrong Sayıdır");
        } else {
            System.out.println(number + " Armstrong Sayı değildir");
        }
    }
}
```
