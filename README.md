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

[Test 3.1](#Test-3_1)
[Test 3.2](#Test-3_2)
[Test 3.3](#Test-3_3)

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
    private int contactHours;
    public Module(String _code, String _name){
        code=_code;
        name=_name;
    }
    public void setName(String _name){
        name = _name;
    }
    public String getName(){
        return name;
    }
    public String getCode(){
        return code;
    }
    public int getContactHours () {
        return contactHours;
    }
    public void setContactHours (int stunden) {
        contactHours = stunden;
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
    
   public boolean isHungry() {
        return hunger > hungerThreshhold;
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
    
    public void play() {
        if (!isHungry()) {
            hunger += 2;
            mood += 2;
            fatigue += 3;
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

## Test 3_1

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

## Test 3_2

### Frage 1
```java
public class Month {
    private final int month;
    private int[] hourCounts;
    public Month(int m){
        month = m;
    }
  
    
    public boolean isRMonth(){
        if (((month % 12) >= 0 && (month % 12) < 5) || (((month % 12) >= 9 && (month % 12) < 12))) {
        return true;
    }
    else if (((month % 12) > -4 && (month % 12) <= 0) || ((month % 12) < -7 && (month % 12) > -12) ){
        return true;
    }
    else return false;
}
    
}


```
### Frage 2
```java
public int crossTotal(int n){
    int summe = 0;
    while (n > 0) {
        summe += n % 10;
        n = n / 10;
    }
    return summe;
    }
```
### Frage 3
```java
public int crossTotal(int n){ //bestanden
    int summe = 0;
    while (n > 0) {
        summe += n % 10;
        n = n / 10;
    }
    return summe;
    }
    
    public int repeatedCrossTotal(int n) {
        int summe2 = 0;
        while (n > 9) {
            n = crossTotal (n);
        }
        return n;
    }
```
### Frage 4
```java
public class PrimeTester{
    private int why = 10;
    public void divisors(int n){
        System.out.print("Teiler von " + n + " sind ");
        for (int i = 1; i < n; i++) {
            if (n % i == 0) {
                System.out.print(i + ", ");
            }
            
        }
        while (why == 10) {
        why -= 1;
        }
        System.out.print(n);
    }
    
    public void properDivisors(int n) {
    System.out.print("Echte Teiler von " + n + " sind ");
    boolean first = true;  // To handle comma placement
    for (int i = 2; i < n; i++) {  // Start from 2 to exclude 1
        if (n % i == 0) {  // If 'i' is a divisor of 'n'
            if (!first) {
                System.out.print(", ");
            }
            System.out.print(i);
            first = false;  // Set false after the first divisor is printed
        }
    }
    System.out.println();  // New line at the end of the output
}

    
    public boolean isPrime(int n) {
        if (n == 1) return false;
        for (int i = 2; i < n; i++) {
            if (n % i == 0) {
                return false;
            }
        }
        return true;
    }
    
    
    public void teilerSpeichern (int n) {
        boolean [] teiler = new boolean[n];
        for (int i = 0; i < n; i++) {
            teiler [i] = n % (i + 1) == 0;
        }
        
        for (int i = 0; i < n; i++) {
            if (teiler[i]) {
                System.out.println((i+2) + " ist ein Teiler von " + n);
            }
        }
    }
    
}
```

## Test 3_3

### Frage 1

<img width="1197" alt="Bildschirmfoto 2024-08-26 um 21 21 06" src="https://github.com/user-attachments/assets/ed00b962-a0b8-4af0-aa95-eef68ab018c7">


### Frage 2
```java

        String[] spruch = {"Ich", "finde", "Java", "Spitze"};

        System.out.println(spruch[0]);
        System.out.println(spruch[1]);
        System.out.println(spruch[2]);
        System.out.println(spruch[3]);
```

### Frage 3
```java
public void printNumbers(int [] numbers){

        for (int i = 0; i < numbers.length; i++) {
            System.out.println(numbers[i]);
        }
    
}
```

### Frage 4
```java
public int totalLength(String[] words){
        int incr = 0;
        	

        for (int i = 0; i < words.length; i++) {
            if (words[i] != null) incr += words[i].length();
        }
        return incr;
    }
```

### Frage 5
```java
public int luhn(int [] digits){
        x2every2nd(digits);
        int sum = crossTotalArray(digits);
        sum = sum % 10;
        sum = 10 - sum;
        sum = sum % 10;
        digits = appendCheckdigit (digits, sum);
        return sum;
    }
    
    public int [] appendCheckdigit (int [] digits, int checkDigit) {
        int [] fullDigits = new int [digits.length + 1];
        for (int i = 0; i < digits.length; i++) {
            fullDigits [i] = digits [i];
        }
        fullDigits [digits.length] = checkDigit;
        return fullDigits;
    }
    
    public int [] x2every2nd (int [] digits) {
        for (int i = 0; i < digits.length; i++) {
            if (i % 2 == 0) {
                digits [i] = 2 * digits[i]; 
            }
        }
        return digits;
    }
    
    public int crossTotalArray (int [] digits) {
        for (int i = 0; i < digits.length; i++) {
            digits [i] = crossTotal (digits [i]);
        }
        int sum = 0;
        for (int i = 0; i < digits.length; i++) {
            sum += digits [i];
        }
        return sum;
    }
    
    public int crossTotal (int zahl) {
        int summe = 0;
        while (zahl != 0) {
            summe += zahl % 10;
            zahl = zahl / 10;
        }
        return summe;
    }
```

### Frage 6
```java
private boolean [] lon; //list of numbers

    
    
    public boolean [] sieve (int n) {
        lon = new boolean [n - 1];
        lon = falsify(lon);
        for (int i = 0; i < lon.length; i++) {
            lon = mark(lon, (i + 2));
        }
        return lon;
    }
    
    private boolean [] falsify (boolean [] lon) {
        for (int i = 0; i < lon.length; i++) {
            lon [i] = false;
        }
        return lon;
    }
    
    private boolean [] mark (boolean [] lon, int k) {
        for (int i = 0; i < lon.length; i++) {
            if ((i + 2) != k && (i + 2) % k == 0) {
                lon [i] = true;
            }
        }
        return lon;
    }
```
### Frage 7
```java
private int [][] chessBoard;
public int[][] chessBoard(){
        chessBoard = new int [8][8];
        for (int i = 0; i < chessBoard.length; i++) {
            for (int j = 0; j < chessBoard[i].length; j++) {
                if (i % 2 == 0) { //gerade Zeilen, Restklasse 0
                    if (j % 2 == 0) { //gerade Elemente in Zeile gez. ab 0
                        chessBoard[i][j] = 0;
                    } else {
                        chessBoard [i][j] = 1;
                    }
                } else if (i % 2 == 1) { //ungerade Zeile RK = 1
                   if (j % 2 == 0) {
                       chessBoard[i][j] = 1;
                   } else {
                       chessBoard [i][j] = 0;
                   }
                }
            }
        }
        return chessBoard;
    }
```

### Frage 8
```java
public int[][] bino(int rows){
        int[][] pascalTriangle = new int[rows][];
     
        for (int i = 0; i < rows; i++) {
            pascalTriangle[i] = new int[i+1];
            
            for (int j = 0; j <= i; j++) {
                if (j == 0 || i == j) {
                    pascalTriangle [i][j] = 1;
                } else {
                    pascalTriangle [i][j] = pascalTriangle[i - 1][j - 1] + pascalTriangle [i -1][j];
                }
            }
        }
        return pascalTriangle;
    }
```



