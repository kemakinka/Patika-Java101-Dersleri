package application;

import java.util.Scanner;

public class Application {

    public static void main(String[] args) {
        int matematik, fizik, kimya, turkce, tarih, muzik;
        Scanner not = new Scanner(System.in);

        System.out.println("Matematik Notunuz: ");
        matematik = not.nextInt();

        System.out.println("Fizik Notunuz: ");
        fizik = not.nextInt();

        System.out.println("Kimya Notunuz: ");
        kimya = not.nextInt();

        System.out.println("Türkçe Notunuz: ");
        turkce = not.nextInt();

        System.out.println("Tarih Notunuz: ");
        tarih = not.nextInt();

        System.out.println("Müzik Notunuz: ");
        muzik = not.nextInt();

        double ortalama = (matematik + fizik + kimya + turkce + tarih + muzik) / 6;
        System.out.println("Not Ortalaması:" + ortalama);
        System.out.println((ortalama > 60)? "Geçti":"Kaldı");


    }

}
