Java döngüler ile girilen sayıya kadar olan 4 ve 5'in kuvvetlerini ekrana yazdıran programı yazıyoruz.
 ```
 Scanner input = new Scanner(System.in);
		System.out.print("Sayı Giriniz: ");
		int sayi = input.nextInt();

		
		System.out.println("Girilen Sayıya Kadar Olan Sayıların 4'ün Kuvvetleri");
		for(int i = 1; i<sayi; i*=4) {
			System.out.println(i+" x "+i+" = "+(i*i));
	
		}
		System.out.println("\n");
		System.out.println("Girilen Sayıya Kadar Olan Sayıların 5'ün Kuvvetleri");
		for(int j = 1; j<sayi; j*=5) {
				System.out.println(j+" x "+j+" = "+(j*j));
		}
 ```
