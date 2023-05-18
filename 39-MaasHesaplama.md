Java'da "Employee" adında fabrika çalışanlarını temsil eden ve metotları ile çalışanların maaşlarını hesaplayan bir sınıf yazmalısınız. Bu sınıf 4 nitelik ve 5 metoda sahip olacaktır.
### Sınıfın Nitelikleri
- name : Çalışanın adı ve soyadı
- salary : Çalışanın maaşı
- workHours : Haftalık çalışma saati
- hireYear : İşe başlangıç yılı
### Sınıfın Metotları
### Employee(name,salary,workHours,hireYear) : Kurucu metot olup 4 parametre alacaktır.
### tax() : Maaşa uygulanan vergiyi hesaplayacaktır.
- Çalışanın maaşı 1000 TL'den az ise vergi uygulanmayacaktır.
- Çalışanın maaşı 1000 TL'den fazla ise maaşının %3'ü kadar vergi uygulanacaktır.
- bonus() : Eğer çalışan haftada 40 saatten fazla çalışmış ise fazladan çalıştığı her saat başına 30 TL olacak şekilde bonus ücretleri hesaplayacaktır.
### raiseSalary() : Çalışanın işe başlangıç yılına göre maaş artışını hesaplayacaktır. Şuan ki yılı 2021 olarak alın.
- Eğer çalışan 10 yıldan az bir süredir çalışıyorsa maaşına %5 zam yapılacaktır.
- Eğer çalışan 9 yıldan fazla ve 20 yıldan az çalışıyorsa maaşına %10 zam yapılacaktır.
- Eğer çalışan 19 yıldan fazla çalışıyorsa %15 zam yapılacaktır.
### toString() : Çalışana ait bilgileri ekrana bastıracaktır.


### Employee Sınıfı
```
class Employee {
	String name; // Adı
	double salary; // Maaş
	int workHours; // Hafatalık Çalışma Saati
	int hireYear; // işe Başlangıç yılı
	int nowYear = 2021;
	
	Employee(String name, double salary, int workHours, int hireYear) {
		this.name = name;
		this.salary = salary;
		this.workHours = workHours;
		this.hireYear = hireYear;
	}


	// Veri Hesaplama formül (para/100)*vergiMiktari
	// Çalışanın maaşı 1000 TL'den fazla ise maaşının %3'ü kadar vergi
	// uygulanacaktır

	double tax() { // vergi
		double vergiHesap;
		if (this.salary > 1000) {
			return vergiHesap = this.salary * 0.03;
		}

		return this.salary;
	}

	/*
	 * bonus() : Eğer çalışan haftada 40 saatten fazla çalışmış ise fazladan
	 * çalıştığı her saat başına 30 TL olacak şekilde bonus ücretleri
	 * hesaplayacaktır.
	 */
	
	double bonus() { //Prim
		if(this.workHours > 40) {
			int fazlaSaat = (this.workHours - 40)*30;
			return fazlaSaat;
		}
		
		return this.workHours;
	}
	
	
	/*
	 raiseSalary() : Çalışanın işe başlangıç yılına göre maaş artışını hesaplayacaktır. Şuan ki yılı 2021 olarak alın.
	 Eğer çalışan 10 yıldan az bir süredir çalışıyorsa maaşına %5 zam yapılacaktır.
	 Eğer çalışan 9 yıldan fazla ve 20 yıldan az çalışıyorsa maaşına %10 zam yapılacaktır.
	 Eğer çalışan 19 yıldan fazla çalışıyorsa %15 zam yapılacaktır.
	 */
	
	
	double raiseSalary() {  //Maaş Artışı
		int calistigiYil = (this.nowYear-this.hireYear);
		double maasArtisi;
		
		if(calistigiYil < 10) {
			return maasArtisi = this.salary*0.05;
		}else if(calistigiYil > 9 && calistigiYil < 20) {
			return maasArtisi = this.salary*0.10;
		}else if(calistigiYil > 19) {
			return maasArtisi = this.salary*0.15;
		}
		
		return 0;
	}
	
	void Hesap() {
		System.out.println("Adı: "+this.name);
		System.out.println("Maaşı: "+this.salary);
		System.out.println("Çalışma Saati: "+this.workHours);
		System.out.println("Başlangıç Yılı: "+this.hireYear);
		System.out.println("Vergi: "+tax());
		System.out.println("Bonus: "+bonus());
		System.out.println("Maaş Artışı: "+raiseSalary());
		System.out.println("Vergi ve Bonuslarla Birlikte Maaş: "+ (bonus()+this.salary-tax()));
		System.out.println("Toplam Maaş: "+ (this.salary+raiseSalary()));
	}
	

}
```

### Main Sınıfı

```

public class Application {

	public static void main(String[] args) {

		Employee kemal = new Employee("kemal",2000.0,45,1985);
		kemal.Hesap();
	}

}


```
