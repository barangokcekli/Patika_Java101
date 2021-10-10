
# Patika Java 101

-------------------


## Pratik 1 - Not Ortalaması Hesaplayan Program

---


```java
import java.util.Scanner;

public class NotOrtalama {
    public static void main(String[] args) {

        double matematik, fizik, kimya, turkce, tarih, muzik;
        Scanner scanner = new Scanner(System.in);

        System.out.print("Matematik notunuzu giriniz : ");
        matematik = scanner.nextInt();
        
        System.out.print("Fizik notunuzu giriniz : ");
        fizik = scanner.nextInt();

        System.out.print("Kimya notunuzu giriniz : ");
        kimya = scanner.nextInt();

        System.out.print("Türkçe notunuzu giriniz : ");
        turkce = scanner.nextInt();

        System.out.print("Tarih notunuzu giriniz : ");
        tarih = scanner.nextInt();

        System.out.print("Müzik notunuzu giriniz : ");
        muzik = scanner.nextInt();


        double toplam = matematik + fizik + kimya + turkce + tarih + muzik;
        double ortalama = toplam / 6;

        System.out.println("Ortamanız = " + ortalama);
        System.out.println("Durum = " + (ortalama >= 60 ? "Geçti" : "Kaldı"));

    }
}
```

---


## Pratik 2 - KDV Tutarı Hesaplayan Program

---

```java
import java.util.Scanner;

public class KdvHesaplama {
    public static void main(String[] args) {

        double kdvOran, tutar, kdvTutar, toplam;
        Scanner scanner = new Scanner(System.in);

        System.out.print("Tutarı girin: ");
        tutar = scanner.nextDouble();
        kdvOran = tutar <= 1000 ? 0.18 : 0.08;
        kdvTutar = tutar * kdvOran;
        toplam = tutar + kdvTutar;


        System.out.println("KDV hariç tutar: " + tutar);
        System.out.println("KDV oranı: " + kdvOran);
        System.out.println("KDV dahil tutar: " + toplam);


    }
}
```
## Pratik 3 - Dik Üçgende Hipotenüs Bulan Program

---



```java
import java.util.Scanner;

public class Hipotenus {
    public static void main(String[] args) {
        int dikkenarA, dikkenarB;
        double hipotenus, cevre, alan;
        Scanner scanner = new Scanner(System.in);

        System.out.print("1. Dik Kenarı Giriniz: ");
        dikkenarA = scanner.nextInt();

        System.out.print("2.Dik Kenarı Giriniz: ");
        dikkenarB = scanner.nextInt();


        hipotenus = Math.sqrt((dikkenarA * dikkenarA) + (dikkenarB * dikkenarB));
        cevre = dikkenarA + dikkenarB + hipotenus;
        alan = (dikkenarA * dikkenarB) / 2;

        System.out.println("Hipotenüs: " + hipotenus);
        System.out.println("Çevre: " + cevre);
        System.out.println("Alan: " + alan);
        
    }
}
```

---

## Pratik 4 - Taksimetre Hesaplayan Program

---



```java
import java.util.Scanner;

public class Taksimetre {
    public static void main(String[] args) {
        double mesafe, taksimetre, toplam;
        int acilis = 10;

        Scanner scanner = new Scanner(System.in);

        System.out.print("Gidilecek mesafeyi giriniz: ");
        mesafe = scanner.nextDouble();

        taksimetre = mesafe * 2.20;
        toplam = (acilis + taksimetre) < 20 ? 20 : acilis + taksimetre;
        System.out.println("Toplam tutar: " + toplam);
    }
}
```

---





