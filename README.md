# Patika Java 101

-------------------

## İçindekiler

| **PRATİKLER**                                                |                       **ÖDEVLER**                        |
| :----------------------------------------------------------- | :------------------------------------------------------: |
| [Pratik 1 - Not  Ortalaması Hesaplayan Program](#pratik1)    | [ÖDEV 1 - Uçak Bileti Fiyatı Hesaplayan Program](#ödev1) |
| [Pratik 2 - KDV  Tutarı Hesaplayan Program](#pratik2)        |    [ÖDEV 2 - Çin Zodyağı Hesaplayan Program](#ödev2)     |
| [Pratik 3 - Dik Üçgende Hipotenüs Bulan Program](#pratik3)   |     [ÖDEV 3 - Artık Yıl Hesaplayan Program](#ödev3)      |
| [Pratik 4 - Taksimetre Hesaplayan Program](#pratik4)         |                                                          |
| [Pratik 5 - Dairenin Alanını ve Çevresini Bulan Program](#pratik5) |                                                          |
| [Pratik 6 - Vücut Kitle İndeksini Hesaplayan Program](#pratik6) |                                                          |
| [Pratik 7 - Manav Kasa Programı](#pratik7)                   |                                                          |
| [Pratik 8 - Basit Hesap Makinesi](#pratik8)                  |                                                          |
| [Pratik 9 - Kullanıcı Girişi](#pratik9)                      |                                                          |
| [Pratik 10 - Sınıfı Geçme Durumu](#pratik10)                 |                                                          |
| [Pratik 11 - Hava Sıcaklığına Göre Etkinlik Önerme](#pratik11) |                                                          |
| [Pratik 12 - Sayıları Küçükten Büyüğüe Sıralayan Program](#pratik12) |                                                          |
| [Pratik 13 - Burç Bulan Program](#pratik13)                  |                                                          |
|                                                              |                                                          |





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



---

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

## Pratik 10 - Sınıfı Geçme Durumu <a name = "pratik10"></a>

---



```java
import java.util.Scanner;

public class Sinif {
    public static void main(String[] args) {
        int math, physics, turkish, chemistry, music;
        double average;
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter your math grade: ");
        math = scanner.nextInt();

        System.out.print("Enter your physics grade: ");
        physics = scanner.nextInt();

        System.out.print("Enter your turkish grade: ");
        turkish = scanner.nextInt();

        System.out.print("Enter your chemistry grade: ");
        chemistry = scanner.nextInt();

        System.out.print("Enter your music grade: ");
        music = scanner.nextInt();

        average = (math + physics + turkish + chemistry + music) / 5;

        if ((0 <= average) && (average < 55)){
            System.out.println("You failed");
        }
        else if ((average >= 55) && (average <= 100)){
            System.out.println("Congratulations! You passed the class.");

        }else {
            System.out.println("Error! Check the values that you entered.");
        }
    }
}
```

---

## Pratik 11 - Hava Sıcaklığına Göre Etkinlik Önerme<a name = "pratik11"></a>

---

```java
import java.util.Scanner;

public class Sicaklik {
    public static void main(String[] args) {
        int temperature;
        Scanner scanner = new Scanner(System.in);

        System.out.print("Hava sıcaklığını giriniz: ");
        temperature = scanner.nextInt();

        if (temperature < 5) {
            System.out.println("Kayak yapabilirsiniz.");
        } else if (temperature >= 5 && temperature <= 25) {
            if (temperature <= 15) {
                System.out.println("Sinemaya gidebilirsiniz.");
            }
            if (temperature >= 10) {
                System.out.println("Pikniğe gidebilirsiniz.");
            }
        } else {
            System.out.println("Yüzmeye gidebilirsiniz.");
        }
    }
}
```



---

## Pratik 12 - Sayıları Küçükten Büyüğüe Sıralayan Program <a name = "pratik12"></a>

---

```java
import java.util.Scanner;

public class SayiSirala {
    public static void main(String[] args) {
        int a, b, c;
        Scanner scanner = new Scanner(System.in);

        System.out.print("1.sayıyı giriniz : ");
        a = scanner.nextInt();

        System.out.print("2.sayıyı giriniz : ");
        b = scanner.nextInt();

        System.out.print("3.sayıyı giriniz : ");
        c = scanner.nextInt();

        if ((a < b) && (a < c)) {
            if (b < c) {
                System.out.println("a: "+a+" < "+" b: "+b+" < "+"c: "+c);
            } else if (c < b) {
                System.out.println("a: "+a+" < "+" c: "+c+" < "+"b: "+b);
            } else {
                System.out.println("a: "+a+" < "+" c: "+c+" = "+"b: "+b);
            }
        } else if ((b < a) && (b < c)) {
            if (a < c) {
                System.out.println("b: "+b+" < "+" a: "+a+" < "+"c: "+c);
            } else if (c < a) {
                System.out.println("b: "+b+" < "+" c: "+c+" < "+"a: "+a);
            } else {
                System.out.println("b: "+a+" < "+" c: "+c+" = "+"a: "+a);
            }
        } else if ((c < a) && (c < b)) {
            if (a < b) {
                System.out.println("c: "+c+" < "+" a: "+a+" < "+"b: "+b);
            } else if (b < a) {
                System.out.println("c: "+c+" < "+" b: "+b+" < "+"a: "+a);
            } else {
                System.out.println("c: "+c+" < "+" b: "+b+" = "+"a: "+a);
            }
        } else {
            System.out.println("a: "+a+" = "+" c: "+c+" = "+"b: "+b);
        }
    }
}
```

---

## Pratik 13 - Burç Bulan Program <a name = "pratik13"></a>

---

```java
import java.util.Scanner;

public class Burc {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("gun: ");
        int gun = scanner.nextInt();
        System.out.print("ay: ");
        int ay = scanner.nextInt();

        if (ay == 12 && gun >= 22 || ay == 1 && gun <= 21)
            System.out.println("oglak");
        else if (ay == 1 || ay == 2 && gun <= 19)
            System.out.println("kova");
        else if (ay == 2 || ay == 3 && gun <= 20)
            System.out.println("balik");
        else if (ay == 3 || ay == 4 && gun <= 20)
            System.out.println("koc");
        else if (ay == 4 || ay == 5 && gun <= 21)
            System.out.println("boga");
        else if (ay == 5 || ay == 6 && gun <= 22)
            System.out.println("ikizler");
        else if (ay == 6 || ay == 7 && gun <= 22)
            System.out.println("yengec");
        else if (ay == 7 || ay == 8 && gun <= 22)
            System.out.println("aslan");
        else if (ay == 8 || ay == 9 && gun <= 22)
            System.out.println("basak");
        else if (ay == 9 || ay == 10 && gun <= 22)
            System.out.println("terazi");
        else if (ay == 10 || ay == 11 && gun <= 21)
            System.out.println("akrep");
        else if (ay == 11 || ay == 12)
            System.out.println("yay");
    }
}

```

---

## ÖDEV 1 - Uçak Bileti Fiyatı Hesaplayan Program <a name = "ödev1" ></a>

---

```java
import java.util.Scanner;

public class UcakBilet {
    public static void main(String[] args) {
        int yas, yolculukTipi;
        double perKM = 0.10;
        double mesafe;
        double biletFiyati;
        boolean valueCheck;
        double tutar;
        Scanner scanner = new Scanner(System.in);

        System.out.print("Mesafe giriniz.(km cinsinden) : ");
        mesafe = scanner.nextDouble();

        System.out.print("Yaşınızı giriniz : ");
        yas = scanner.nextInt();

        System.out.println("Yolculuk Tipini Seçiniz:\n1- Tek Yön\n2-Gidiş Dönüş");
        yolculukTipi = scanner.nextInt();

        valueCheck = (mesafe > 0) && (yas > 0) && (yolculukTipi == 1 || yolculukTipi == 2);
        biletFiyati = mesafe * perKM;

        if (valueCheck) {
            if (yolculukTipi == 2) {
                biletFiyati -= mesafe * perKM * 0.2;
                if (yas < 12) {
                    biletFiyati *= 0.5;
                    tutar = biletFiyati * 2;
                    System.out.println("Toplam fiyat: " + tutar);
                } else if (12 <= yas && yas <= 24) {
                    biletFiyati -= biletFiyati * 0.1;
                    tutar = biletFiyati * 2;
                    System.out.println("Toplam fiyat: " + tutar);
                } else if (yas > 65) {
                    biletFiyati -= biletFiyati * 0.3;
                    tutar = biletFiyati * 2;
                    System.out.println("Toplam fiyat: " + tutar);
                } else {
                    biletFiyati = biletFiyati;
                    tutar = biletFiyati * 2;
                    System.out.println("Toplam fiyat: " + tutar);
                }
            } else {
                if (yas < 12) {
                    biletFiyati *= 0.5;
                    System.out.println("Toplam fiyat: " + biletFiyati);
                } else if (12 <= yas && yas <= 24) {
                    biletFiyati -= biletFiyati * 0.1;
                    System.out.println("Toplam fiyat: " + biletFiyati);
                } else if (yas > 65) {
                    biletFiyati -= biletFiyati * 0.3;
                    System.out.println("Toplam fiyat: " + biletFiyati);
                } else {
                    biletFiyati = biletFiyati;
                    System.out.println("Toplam fiyat: " + biletFiyati);
                }
            }
        } else {
            System.out.println("HATA: Mesafe ve yaş değerleri pozitif sayı, yolculuk tipi ise 1 veya 2 olmalıdır");
        }
    }
}
```

---

## ÖDEV 2 - Çin Zodyağı Hesaplayan Program <a name = "ödev2"></a>

---

```java
import java.util.Scanner;

public class Zodiac {
    public static void main(String[] args) {
        int  yearOfBirth, zodiac;

        Scanner scanner = new Scanner(System.in);

        System.out.print("Doğum yılınızı giriniz: ");
        yearOfBirth = scanner.nextInt();

        zodiac = yearOfBirth % 12;

        switch (zodiac) {
            case 0:
                System.out.println("Maymun");
                break;
            case 1:
                System.out.println("Horoz");
                break;
            case 2:
                System.out.println("Köpek");
                break;
            case 3:
                System.out.println("Domuz");
                break;
            case 4:
                System.out.println("Fare");
                break;
            case 5:
                System.out.println("Öküz");
                break;
            case 6:
                System.out.println("Kaplan");
                break;
            case 7:
                System.out.println("Tavşan");
                break;
            case 8:
                System.out.println("Ejderha");
                break;
            case 9:
                System.out.println("Yılan");
                break;
            case 10:
                System.out.println("At");
                break;
            case 11:
                System.out.println("Koyun");
                break;
            default:
                System.out.println("ERROR!!");
        }
    }
}
```

---

## ÖDEV 3 - Artık Yıl Hesaplayan Program <a name = "ödev3"></a>

---

```java
import java.util.Scanner;

public class ArtikYil {
    public static void main(String[] args) {
        int year;
        Scanner scanner = new Scanner(System.in);

        System.out.print("Yıl giriniz: ");
        year = scanner.nextInt();

        if (year % 10 == 0) {
            if (year % 400 == 0) {
                System.out.println(year + " artık yıldır.");
            } else if ((year % 400) % 4 == 0) {
                System.out.println(year + " artık yıldır.");
            } else {
                System.out.println(year + " artık yıl değildir.");
            }
        } else if (year % 4 == 0) {
            System.out.println(year + " artık yıldır.");
        } else {
            System.out.println(year + " artık yıl değildir.");
        }
    }
}
```

---

