### Fighter Sınıfı
```
public class Fighter {
    String name;
    int damage;
    int health;
    int weight;
    int dodge;

    Fighter(String name, int damage, int health, int weight, int dodge){
        this.name = name;
        this.damage = damage;
        this.health = health;
        this.weight = weight;
        if (dodge >= 0 && dodge <= 100) {
            this.dodge = dodge;
        }
        else {
            this.dodge = 0;
        }
    }
    public int hit (Fighter foe) {
        System.out.println(this.name + " => " + foe.name + " hit " + this.damage + " damage !");

        if (isDodge()) {
            System.out.println(foe.name + " blocked incoming damage !");
            return foe.health;
        }

        if (foe.health - this.damage < 0) {
            return 0;
        }
        return foe.health - this.damage;
    }
    public boolean isDodge () {
         double randomNumber = (Math.random() * 100);
         return randomNumber <= this.dodge;
    }
}
```
### Ring Sınıfı

```
import java.util.Random;
public class Ring {
    Fighter f1;
    Fighter f2;
    int minWeight;
    int maxWeight;


    Ring(Fighter f1, Fighter f2, int minWeight, int maxWeight) {
        this.f1 = f1;
        this.f2 = f2;
        this.minWeight = minWeight;
        this.maxWeight = maxWeight;
    }

    public void run() {
        if(isCheck()) {
            while (this.f1.health > 0 && this.f2.health > 0 ){
                System.out.println(">>>>NEW ROUND<<<<");

                if (firstToAttack() == true) {
                    this.f2.health = this.f1.hit(this.f2);
                    System.out.println(this.f2.name + "'s Health = " + this.f2.health);
                    System.out.println(this.f1.name + "'s Health =  " + this.f1.health);
                    if (isWin()) {
                        break;
                    }
                }
                else {
                    this.f1.health = this.f2.hit(this.f1);
                    System.out.println(this.f1.name + "'s Health =  " + this.f1.health);
                    System.out.println(this.f2.name + "'s Health = " + this.f2.health);
                    if (isWin()) {
                        break;
                    }

                }
            }

        }
        else {
            System.out.println("Athletes' weights don't match !");
        }
    }
    public boolean isWin() {
        if (this.f1.health == 0) {
            System.out.println(this.f2.name + " won !");
            return true;
        }
        if (this.f2.health == 0) {
            System.out.println(this.f1.name + " won !");
            return true;
        }
        return false;
    }
    public boolean isCheck(){
        return (this.f1.weight >= minWeight && this.f1.weight <= maxWeight)
                && (this.f2.weight >= minWeight && this.f2.weight <= maxWeight);
    }
    public boolean firstToAttack () {
        int number = (int)(Math.random()*10);
        if (number <= 5) {
            return true; // if it is true, then f1 will start.
        }
        return false;
    }
}
```
### Main sınıfı

```
public class Main {
    public static void main(String[] args) {
        Fighter f1 = new Fighter("A", 10,120,100,30);
        Fighter f2 = new Fighter("B", 20, 85, 85,40);

        Ring match = new Ring(f1, f2, 85,100);
        match.run();

    }
}

```
