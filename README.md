# Musterlösungen
>[!IMPORTANT]
>
> Die Lösungen sind alle geprüft richtig für den Jahrgang I23.
> Je länger dieses Repo vor den falschen Augen geschützt wird, desto länger haben Studierende etwas davon. 
> Das Durchführen der Tests ist eine gute Übung. Nutzt diese Musterlösung zum Vergleichen, nicht zum Abschreiben.
> Bei den Multiple-Choice Aufgaben wird die Reihenfolge bei jedem Versuch getauscht, also seid da vorsichtig.
> Der Code kann 1:1 so ins Antwortfeld kopiert werden, wie er hier angegeben ist.





# Inhalt
[Test 1](#Test-1)

[Test 2](#Test-2)

[Test 3-1](#Test-3.1)

## Test 1

### Frage 1

![Bild](https://github.com/user-attachments/assets/0e624cb6-5ecd-4d80-b62a-64210e63f9cd)


### Frage 2

![x](https://github.com/user-attachments/assets/16a3f3e5-8ec0-42e5-96ed-d251474d3611)


### Frage 3

![x](https://github.com/user-attachments/assets/a35a2cb9-4dda-4960-b706-0b4a8a6e5616)

### Frage 4

![x](https://github.com/user-attachments/assets/6d5f1a29-ec19-4c64-aa88-d40106240d78)


### Frage 5 

![x](https://github.com/user-attachments/assets/28e823d7-3f5c-49be-b00a-674d6dee4be1)


### Frage 6
```java
public boolean isOnXAxis(){
    return y == 0;
    }
```
### Frage 7
```java
public void langsamBewegen(int schritte, int xRichtung, int yRichtung) {
        for (int i = 0; i < schritte; i++) {
            if (xPosition + xRichtung <= 0 || xPosition + durchmesser + xRichtung >= 500 ) {
                xRichtung = -xRichtung;
            }
            if (yPosition + yRichtung <= 0 || yPosition + durchmesser + yRichtung >= 300 ) {
                yRichtung = -yRichtung;
            }            
            xPosition += xRichtung;
            yPosition += yRichtung;
            zeichnen();
        }
}
```

<br> 

## Test 2

### Frage 1

<img width="1332" alt="v" src="https://github.com/user-attachments/assets/34adecaf-738e-4031-8683-14674eed8807">

### Frage 2

<img width="1351" alt="a" src="https://github.com/user-attachments/assets/d82a671d-d1d0-4231-ac2b-8f37c84fb993">


### Frage 3

<img width="1338" alt="Frage 6" src="https://github.com/user-attachments/assets/0359730e-9feb-4576-a1ca-259db9891b86">
<img width="1201" alt="Frage 6" src="https://github.com/user-attachments/assets/44f78845-1363-4c62-994a-14dce582f54c">


### Frage 4
```java
public class Module {
    private String code;
    private String name;
    private int kontaktStunden;
    public Module(String _code, String _name){
        code=_code;
        name=_name;
    }
    public void setName(String _name){
        name=_name;
    }
    public String getName(){
        return name;
    }
    public String getCode(){
        return code;
    }
    public int getContactHours () {
        return kontaktStunden;
    }
    public void setContactHours (int stunden) {
        kontaktStunden = stunden;
    }
}
```

### Frage 5


<img width="1348" alt="Frage 6" src="https://github.com/user-attachments/assets/3e1e4167-d970-4532-9423-4632fe92b676">

### Frage 6

<img width="1347" alt="Frage 6" src="https://github.com/user-attachments/assets/27914fd8-f8e1-404f-b68c-f4add199622b">


### Frage 7 
```java
//Vervollständigen Sie folgende Methode
public int relativeXPositionTo(Point p) {
     if (p.x == x){
            return 0;
        }
    else if (p.x > x){
        return -1;
    }
    else {
        return 1;
    }
}
```
### Frage 8
```java
public class Tamagotchi
{

    private int x;
    private int hunger;
    private int mood;
    private int fatigue;
    private int hungerThreshhold;
    private int moodThreshhold;
    private int fatigueTreshhold;


    public Tamagotchi(int hungerInit, int moodInit, int fatigueInit)
    {

        hunger = 0;
        mood = 0;
        fatigue = 0;
        hungerThreshhold = hungerInit;
        moodThreshhold = moodInit;
        fatigueTreshhold = fatigueInit;
    }
    
    private boolean isHungry(){
        if (hunger > hungerThreshhold){
            return true;
        } else {
            return false;
        }
    }
    
    private boolean isHappy(){
        if (mood > moodThreshhold){
            return true;
        } else {
            return false;
        }
    }
    
    private boolean isTired(){
        if (fatigue > fatigueTreshhold){
            return true;
        } else {
            return false;
        }
    }
    
    public void play (){
        if (isHungry() == false){
            hunger = hunger + 2;
            mood = mood + 2;
            fatigue = fatigue + 3;
        }
    }
    
    public void eat (){
        if (isTired() == false){
            hunger -= 3;
            fatigue +=2;
        }
    }
    
    public void sleep (){
        if (isHungry()){
            hunger += 1;
            mood -= 1;
            fatigue = 0;
        } else {
            hunger += 1;
            mood += 1;
            fatigue = 0;
        }
    }
    
    public void pet () {
        hunger += 1;
        mood += 2;
    }
    
    public String getGeneralCondition (){
        if (isTired()){
            return "tired";
        } else if (isHungry()){
            return "hungry";
        } else if(isHappy()) {
            return "happy";
        } else {
            return "indifferent";
        }
    }
    
    public void makeHappy () {
        eat ();
        sleep ();
    }
}
```

## Test 3.1

### Frage 1

<img width="1306" alt="Bildschirmfoto 2024-08-20 um 14 50 25" src="https://github.com/user-attachments/assets/7c072d4a-f0e9-4993-9dc5-cbc2ad8dfe92">

### Frage 2

<img width="1297" alt="Bildschirmfoto 2024-08-20 um 14 50 37" src="https://github.com/user-attachments/assets/5b55b2b5-956b-4a65-b6d3-e7fc911c87d5">

### Frage 3
```java
for (int i = 12; i <= 99; i+= 3) {
        System.out.println(i);
        }
```

### Frage 4
```java
public void printStars(int number){
    for (int i = 0; i < number; i++) {
            System.out.print("*");
        }
}

public void printTriangle(int number){
        for (int i = 1; i <= number; i++) {
            printStars(i);
            System.out.println("");
        }
    
    }

public void printDiamond(int number){
        int breite = 2 * number + 1;
        for (int i = 1; i <= breite; i+= 2){
            printLeerzeichen((breite - i) / 2);
            printStars(i);
            System.out.println(" ");
        }
        for (int i = breite - 2; i > 0; i-= 2){
            printLeerzeichen((breite - i) / 2);
            printStars(i);
            System.out.println(" ");
        }
    }

    public void printLeerzeichen (int number) {
        for (int i = 0; i < number; i++) {
            System.out.print(" ");
        }
    }
```
