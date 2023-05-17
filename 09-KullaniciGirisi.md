### Kullanici Girişi
Eğer şifre yanlış ise kullanıcıya şifresini sıfırlayıp sıfırlamayacağını sorun, eğer kullanıcı sıfırlamak isterse yeni girdiği şifrenin hatalı girdiği ve unuttuğu şifre ile aynı olmaması gerektiğini kontrol edip , şifreler aynı ise ekrana "Şifre oluşturulamadı, lütfen başka şifre giriniz." sorun yoksa "Şifre oluşturuldu" yazan programı yazınız.

```
import java.util.Scanner;

public class KullaniciGirisi {

	public static void main(String[] args) {
		String username, password, dbUser, dbPassword;

		dbUser = "kemal";
		dbPassword = "12345";

		Scanner input = new Scanner(System.in);

		System.out.print("Kullanıcı Adı: ");
		username = input.nextLine();

		System.out.print("Şifreniz: ");
		password = input.nextLine();

		if (!dbUser.equals(username)) { // Kullanıcı Adı karşılaştırıldı
			System.out.println("Kullanıcı Adı Hatalı!");
		} else if (!dbPassword.equals(password)) { // Şifre Karşılaştırıldı
			System.out.println("Şifreniz Hatalı!");
			System.out.print("Şifreyi Sıfırlamak İster misiniz? Evet(e) - Hayır(h)"); //Şifre Değiştirmek istendiğinde
			String cevap = input.nextLine();
			if (cevap.equals("e") || cevap.equals("E")) {
				System.out.println("Yeni Şifrenizi Giriniz: ");
				String newPassword = input.nextLine(); 
				if(dbPassword.equals(newPassword)) {
					System.out.println("Şifre oluşturulamadı, lütfen başka şifre giriniz");
				}else {
					System.out.println("Şifre Oluşturuldu.");
				}
			} else {
				System.out.println("Lütfen bilgilerinizi kontrol edin ve tekrar giriş yapınız.");
			}
		} else {
			System.out.println("Hoşgeldin," + dbUser);
		}

	}

}

```
