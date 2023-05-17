### Java ile iki sayının EBOB ve EKOK değerlerini "While Döngüsü" kullanarak yazınız.

```
package Pratik;

import java.util.Scanner;

public class EbobEkok {
    public static void main(String[] args) {
        Scanner scanner=new Scanner(System.in);
        System.out.print("n1 sayisini giriniz:");
        int n1=scanner.nextInt();
        System.out.print("n2 sayisini giriniz:");
        int n2=scanner.nextInt();
        int ebob=1, ekok, i=1;
        while(i<=n1){
            if((n1%i==0)&&(n2%i==0)){
                ebob=i;
            }
            i++;
        }
        System.out.println("Ebob:"+ebob);
        ekok=(n1*n2)/ebob;
        System.out.println("Ekok:"+ekok);
    }
}
```
