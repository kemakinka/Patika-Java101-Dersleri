```
import java.util.Scanner;

public class UcgenHesapla {

	public static void main(String[] args) {
		/*
		 * Üç kenar uzunluğunu kullanıcıdan aldığınız üçgenin alanını hesaplayan
		 * programı yazınız.
		 * 
		 * Formül Üç𝑔𝑒𝑛𝑖𝑛 ç𝑒𝑣𝑟𝑒𝑠𝑖 = 2𝑢
		 * 
		 * 𝑢 = (a+b+c) / 2
		 * 
		 * Alan * Alan = 𝑢 * (𝑢 − 𝑎)* (𝑢 − 𝑏) * (𝑢 − 𝑐)
		 * 
		 * 
		 */
		
		int aKenari, bKenari, cKenari,ucgen,alan,sonuc;
		
		Scanner scan = new Scanner(System.in);
		
		System.out.println("A Kenarı: ");
		aKenari = scan.nextInt();
		System.out.println("B Kenarı: ");
		bKenari = scan.nextInt();
		System.out.println("C Kenarı: ");
		cKenari = scan.nextInt();
		
		ucgen = (aKenari+bKenari+cKenari)/2;
		alan =  ucgen*(ucgen-aKenari)*(ucgen-bKenari)*(ucgen-cKenari);
		sonuc = alan*alan;
		
		System.out.println("A Kenarı= "+aKenari);
		System.out.println("B Kenarı= "+bKenari);
		System.out.println("A Kenarı= "+cKenari);
		System.out.println("----------------------");
		System.out.println("Üçgen Alanı= "+sonuc);
		
		
	}

}


```
