```
import java.util.Arrays;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        //Dizi boyutunu alıyoruz ve dizinin index değeri yerine yerleştiriyoruz.
        System.out.print("Dizi Boyutunu Giriniz : ");
        int indexArray = input.nextInt();
        int[] numbers = new int[indexArray];
        //Dizi elemanlarını döngü ile kullanıcıdan alıyoruz.
        System.out.println("Dizinin Elemanlarını Giriniz : ");
        for(int i=0; i < numbers.length; i++){
            System.out.print((i+1) + ". Elemanı Gir : ");
            numbers[i] = input.nextInt();
        }
        //Dizi hafızaya kaydedildiği için döngü dışında istediğimiz gibi diziyi ekrana bastırabiliyoruz.
        System.out.println("Dizi : " + Arrays.toString(numbers));
        Arrays.sort(numbers);
        System.out.println("Sıralı : " + Arrays.toString(numbers));
    }
}
```
