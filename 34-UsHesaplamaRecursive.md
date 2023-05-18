```
import java.util.Scanner;

class Main {
    static Scanner input = new Scanner(System.in);
   static void Power()
   {
       int taban,kuvvet,sonuc=1;
       do
        {
            System.out.print("Taban değerini giriniz");
             taban=input.nextInt();
            System.out.print("Kuvvet değeini giriniz");
             kuvvet=input.nextInt();
            for (int i=1; i<=kuvvet;i++)
            {
                sonuc=sonuc*taban;

            }
            System.out.println("Sonuc: "+ sonuc);


        } while (taban!=0);

   }

    public static void main(String[] args) {
       Power();





    }
}



```
