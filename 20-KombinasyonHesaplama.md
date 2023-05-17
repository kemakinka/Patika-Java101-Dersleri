### Ödev
N elemanlı bir kümenin elemanları ile oluşturulacak r elemanlı farklı grupların sayısı n’in r’li kombinasyonu olarak adlandırılır. N’in r’li kombinasyonu C(n,r) şeklinde gösterilir.
### Kombinasyon formülü
C(n,r) = n! / (r! * (n-r)!)
```
import java.util.Scanner;
public class Application {
public static void main(String[] args) {
	      Scanner scanner=new Scanner(System.in);
	        System.out.print("Bir n degeri giriniz:");
	        int n=scanner.nextInt();
	        System.out.print("Bir r degeri giriniz:");
	        int r=scanner.nextInt();
	        
	        int nToplam=1, rToplam=1, nrToplam=1;
	        
	        for (int i=1; i<=n; i++){
	        	nToplam=nToplam*i;
	        }
	        for (int i=1; i<=r; i++){
	        	rToplam=rToplam*i;
	        }
	        for (int i=1; i<=(n-r); i++){
	        	nrToplam=nrToplam*i;
	        }
	        int sonuc=nToplam/(rToplam*nrToplam);
	        
	        System.out.println("Sonuc:"+sonuc);		
	}

}

```
