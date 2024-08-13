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

## Test 1

### Frage 1
![Aufgabe 1](https://github.com/user-attachments/assets/84d4cdb2-c1bc-4bef-9ac1-ce74ddfacefd)

### Frage 2

![Aufgabe 2](https://github.com/user-attachments/assets/9dc5c8b4-b73f-4337-b6f8-e6f03eee4a33)

### Frage 3

![Aufgabe 3](https://github.com/user-attachments/assets/c8d1d3ed-dafa-4ed4-a1f7-8be8e560773d)

### Frage 4

![Aufgabe 4](https://github.com/user-attachments/assets/9b10463d-b464-4f19-9519-3256752dd806)

### Frage 5 

![Aufgabe 5](https://github.com/user-attachments/assets/8e99bbc2-02ab-40c7-a864-829dcfd0455d)

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

<img width="1332" alt="Aufgabe 1" src="https://github.com/user-attachments/assets/c194e88a-37d8-4ac2-9c74-508814cd3d3c">

### Frage 2

<img width="1351" alt="Aufgabe 2" src="https://github.com/user-attachments/assets/52ba407f-3271-450f-8adc-ba3ccf2a59a3">

### Frage 3

<img width="1338" alt="Aufgabe 3" src="https://github.com/user-attachments/assets/fd275121-f89f-46ec-9909-1cc89688af39">
<img width="1201" alt="Aufgabe 4" src="https://github.com/user-attachments/assets/4c303dc9-604a-48e3-9d98-416d5f594b37">

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

<img width="1348" alt="Aufgabe 5" src="https://github.com/user-attachments/assets/b4480fc7-82c4-4a7c-ae0b-7b26d259923c">

### Frage 6

<img width="1347" alt="Aufgabe 6" src="https://github.com/user-attachments/assets/8ece72fe-b173-49ba-bb11-96874ee68957">

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
    // Instanzvariablen - ersetzen Sie das folgende Beispiel mit Ihren Variablen
    private int x;
    private int hunger;
    private int mood;
    private int fatigue;
    private int hungerThreshhold;
    private int moodThreshhold;
    private int fatigueTreshhold;


    public Tamagotchi(int hungerInit, int moodInit, int fatigueInit)
    {
        // Instanzvariable initialisieren
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

