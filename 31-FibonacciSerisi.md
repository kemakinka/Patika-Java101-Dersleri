### Fibonacci Serisi Nedir ?
Fibonacci serisi, her sayının kendinden önceki ile toplanması sonucu oluşan bir sayı dizisidir. Bu şekilde devam eden bu dizide sayılar birbirleriyle oranlandığında altın oran ortaya çıkar, yani bir sayı kendisinden önceki sayıya bölündüğünde altın orana gittikçe yaklaşan bir dizi elde edilir.
Fibonacci dizisi, 0'dan başlar ve sonsuza kadar. Her rakam, bir önceki rakamla toplanır. Elde edilen sonuç rakamın sağ tarafına yazılır. Fibonacci dizisinin ilk on sayısı şu şekildedir:
- 9 Elemanlı Fibonacci Serisi : 0 1 1 2 3 5 8 13 21 34

```
import java.util.Scanner;

public class Application {

	public static void main(String[] args) {
		  int n,i,sum=0;
	        Scanner input = new Scanner(System.in);
	        System.out.print("Fibonacci Adım Sayısı Giriniz: ");
	        n = input.nextInt();
	        int s1=0;
	        int s2=1;
	        for(i=1;i<=n;i++){
	            System.out.print(s1 + " ");
	            sum = s1+s2;
	            s1=s2;
	            s2=sum;
	        }
	}

}

```
