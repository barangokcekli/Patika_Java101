# Patika Java 101

-------------------

## İçindekiler

1. [Pratik 1 - Not  Ortalaması Hesaplayan Program](#pratik1)

2. [Pratik 2 - KDV  Tutarı Hesaplayan Program](#pratik2)

3. [Pratik 3 - Dik Üçgende Hipotenüs Bulan Program](#pratik3)

4. [Pratik 4 - Taksimetre Hesaplayan Program](#pratik4)

5. [Pratik 5 - Dairenin Alanını ve Çevresini Bulan Program](#pratik5)

6. [Pratik 6 - Vücut Kitle İndeksini Hesaplayan Program](#pratik6)

7. [Pratik 7 - Manav Kasa Programı](#pratik7)

8. [Pratik 8 - Basit Hesap Makinesi](#pratik8)

9. [Pratik 9 - Kullanıcı Girişi](#pratik9)

   



## Pratik 1 - Not  Ortalaması Hesaplayan Program <a name ="pratik1"></a>

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

## Pratik 2 - KDV  Tutarı Hesaplayan Program <a name ="pratik2"></a>

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

---



## Pratik 3 - Dik Üçgende Hipotenüs Bulan Program <a name ="pratik3"></a>

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



## Pratik 4 - Taksimetre Hesaplayan Program <a name ="pratik4"></a>

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



## Pratik 5 - Dairenin Alanını ve Çevresini Bulan Program <a name ="pratik5"></a>

---



```java
import java.util.Scanner;
public class Circle {
    public static void main(String[] args) {
        double pi = 3.14, perimeter, area, circleSegmentArea;
        int radius, centralAngle;

        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter radius value: ");
        radius = scanner.nextInt();

        System.out.println("Enter central angle value: ");
        centralAngle = scanner.nextInt();

        perimeter = 2 * pi * radius;
        area = pi * Math.pow(radius, 2);
        circleSegmentArea = (pi * Math.pow(radius, 2) * centralAngle) / 360;

        System.out.println("Perimeter: " + perimeter);
        System.out.println("Area: " + area);
        System.out.println("Circle segment area: " + circleSegmentArea);
    }
}
```

---

 ## Pratik 6 - Vücut Kitle İndeksini Hesaplayan Program <a name ="pratik6"></a>

---



```java
import java.util.Scanner;

public class BodyMassIndex {
    public static void main(String[] args) {
        double height, weight, bodyMassIndex;
        Scanner scanner = new Scanner(System.in);

        System.out.print("Boyunuzu (metre cinsinden) giriniz: ");
        height = scanner.nextDouble();

        System.out.print("Kilonuzu (kg cinsinden) giriniz: ");
        weight = scanner.nextDouble();

        bodyMassIndex = weight / Math.pow(height, 2);

        System.out.println("Vücut Kitle İndeksiniz: " + bodyMassIndex);
    }
}
```

---



## Pratik 7 - Manav Kasa Programı <a name ="pratik7"></a>

---



```java
import java.util.Scanner;

public class Manav {
    public static void main(String[] args) {
        double armut = 2.14, elma = 3.67, domates = 1.11, muz = 0.95, patlican = 5.00;
        double miktarArmut, miktarElma, miktarDomates, miktarMuz, miktarPatlican;
        double total;
        Scanner scanner = new Scanner(System.in);
        System.out.println("""
                Meyveler ve KG Fiyatları
                ------------------------
                Armut : 2,14 TL
                Elma : 3,67 TL
                Domates : 1,11 TL
                Muz: 0,95 TL
                Patlıcan : 5,00 TL""");

        System.out.print("Alınan Armut Miktarını Kg Cinsinden Giriniz: ");
        miktarArmut = scanner.nextDouble();

        System.out.print("Alınan Elma Miktarını Kg Cinsinden Giriniz: ");
        miktarElma = scanner.nextDouble();

        System.out.print("Alınan Domates Miktarını Kg Cinsinden Giriniz: ");
        miktarDomates = scanner.nextDouble();

        System.out.print("Alınan Muz Miktarını Kg Cinsinden Giriniz: ");
        miktarMuz = scanner.nextDouble();

        System.out.print("Alınan Patlıcan Miktarını Kg Cinsinden Giriniz: ");
        miktarPatlican = scanner.nextDouble();

        total = (miktarArmut * armut) + (miktarElma * elma) + (miktarDomates * domates) + (miktarMuz * muz) + (miktarPatlican * patlican);
        System.out.println("Toplam tutar: " + total);
    }
}

```

---

## Pratik 8 - Basit Hesap Makinesi<a name ="pratik8"></a>

---



```java
import java.util.Scanner;

public class BasitHesapMakinesi {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        double number1, number2, result;
        int selection;
        
        System.out.print("Number 1: ");
        number1 = scanner.nextDouble();
        System.out.print("Number 2: ");
        number2 = scanner.nextDouble();

        System.out.println("1-Toplama\n2-Çıkarma\n3-Çarpma\n4-Bölme");
        System.out.print("Select : ");
        selection = scanner.nextInt();

        switch (selection) {
            case 1:
                result = number1 + number2;
                System.out.println(result);
                break;
            case 2:
                result = number1 - number2;
                System.out.println(result);
                break;
            case 3:
                result = number1 * number2;
                System.out.println(result);
                break;
            case 4:
                if (number2 == 0){
                    System.out.println("Zero Division Error!");
                    break;
                }else{
                    result = number1 / number2;
                    System.out.println(result);
                }
                break;
            default:
                System.out.println("ERROR");
        }
    }
}
```


## Pratik 9 - Kullanıcı Girişi <a name = "pratik9" ></a>

---



```java
import java.util.Scanner;

public class KullaniciGiris {
    public static void main(String[] args) {
        String userName = "patika", password = "java123";
        String inptUserName, inptPassword;
        int resetSelection;

        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter your username: ");
        inptUserName = scanner.nextLine();

        System.out.print("Enter your password: ");
        inptPassword = scanner.nextLine();

        if (inptUserName.equals(userName)){
            if (inptPassword.equals(password)){
                System.out.println("You've successfully logged in.");
            }else{
                System.out.print("Error! Invalid password.If you want to change your password enter 1 if not enter 0 : ");
                resetSelection = scanner.nextInt();
                if (resetSelection == 1){
                    System.out.print("Enter your new password: ");
                    String newPassword = scanner.next();
                    if(newPassword.equals(inptPassword) || (newPassword.equals(password))){
                        System.out.println("New password cannot be the same as your old password.");
                    }else{
                        System.out.println("You've successfully changed your password");
                        newPassword = inptPassword;
                    }
                }else {
                    System.out.println("Exiting....");
                }
            }
        }else{
            System.out.println("Error! : Invalid username");
        }
    }
}
```
---














