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

[Test 4](#Test-4)

[Test 5](#Test-5)

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

```java
//oder eleganter:

public int[][] chessBoard() {
    int[][] schachBrett = new int[8][8];
    for (int i = 0; i < 8; i++) {
        for (int j = 0; j < 8; j++) {
            schachBrett[i][j] = (i + j) % 2; // 1 für Weiß, 0 für Schwarz
        }
    }
    return schachBrett;
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

## Test 4

### Frage 1

![image](https://github.com/user-attachments/assets/789c3cba-a00d-4bd9-b2e2-945f4bd5a3b0)

### Frage 2

![image](https://github.com/user-attachments/assets/8c4d2854-8162-42fe-a03e-40b1235b956a)


### Frage 3

![image](https://github.com/user-attachments/assets/cc0567d7-344c-4423-96c1-4f7bc2fe7cb4)

### Frage 4

![image](https://github.com/user-attachments/assets/a287e7bc-d0d1-4a4b-9de2-d2dd4e369be7)


### Frage 5
```java
public class ClockDisplay {
    private NumberDisplay hours;
    private NumberDisplay minutes;
    private String displayString;    
    
    public ClockDisplay(){
        hours = new NumberDisplay(24);
        minutes = new NumberDisplay(60, hours);
        updateDisplay();
    }
    public ClockDisplay(int hour, int minute){
        hours = new NumberDisplay(24);
        minutes = new NumberDisplay(60, hours);
        setTime(hour, minute);
    }
    public void timeTick(){
        minutes.increment();
        // if(minutes.getValue() == 0) {  
            // hours.increment();
        // }
        updateDisplay();
    }
    public void setTime(int hour, int minute) {
        hours.setValue(hour);
        minutes.setValue(minute);
        updateDisplay();
    }

    public String getTime() {
        return displayString;
    }
    
    private void updateDisplay() {
        displayString = hours.getDisplayValue() + ":" + 
                        minutes.getDisplayValue();
    }
}


public class NumberDisplay
{
    private int limit;
    private int value;
    private NumberDisplay parent;
    
    public NumberDisplay(int rollOverLimit, NumberDisplay parent)    {
        limit = rollOverLimit;
        value = 0;
        this.parent = parent;
    }
    
    public NumberDisplay(int rollOverLimit)    {
        limit = rollOverLimit;
        value = 0;
    }

    public int getValue()    {
        return value;
    }

    public String getDisplayValue()    {
        if(value < 10) {
            return "0" + value;
        }
        else {
            return "" + value;
        }
    }

    public void setValue(int replacementValue)    {
        if((replacementValue >= 0) && (replacementValue < limit)) {
            value = replacementValue;
        }
    }

    public void increment() {
        if ((value + 1) == limit && parent != null) parent.increment();
        value = (value + 1) % limit;
    }
}
```

## Test 5

### Frage 1
![image](https://github.com/user-attachments/assets/0b7cd51c-9cab-422d-9b7c-fd9db4ae00f2)

### Frage 2
![image](https://github.com/user-attachments/assets/b677f88f-b1ff-467c-9e3e-6bc1ee6c0c46)


### Frage 3
![image](https://github.com/user-attachments/assets/f19d6717-70f0-4a6e-a44e-5a2c3bcab5f2)


### Frage 4
![image](https://github.com/user-attachments/assets/72be54b2-a299-452a-8f29-aa0c395f2664)

### Frage 5
```java
public ArrayList<String> unify(ArrayList<String> input){
        ArrayList <String> result = new ArrayList<>();
        for (String s: input) {
            if (!result.contains(s)) {
                if (s != null) {
                    result.add(s);
                }
            }
        }
        return result;
    }
```
### Frage 6
```java
public ArrayList<String> unify(ArrayList<String> input){
        ArrayList <String> result = new ArrayList<>();
        int n = 0;
        while (n < input.size()) {
            if (!result.contains(input.get(n))) {
                if (input.get(n) != null) {
                    result.add(input.get(n));
                }
            }
            n++;
        }
        return result;
    }
```
### Frage 7
```java
// später...
```
### Frage 8
```java
public void deleteTabu(ArrayList<String> posts, String tabu){
    Iterator<String> i = posts.iterator();
    while (i.hasNext()){
        String hs = i.next();
        if (hs != null && hs.contains(tabu)) {
            i.remove();
             }
        }
    }
```
### Frage 9
```java
// shoppingBasket
import java.util.*;
import java.util.Iterator;

public class ShoppingBasket
{
    // Instanzvariablen - ersetzen Sie das folgende Beispiel mit Ihren Variablen
    private Catalog catalog;
    private ArrayList<String> basket = new ArrayList<> ();

    public ShoppingBasket(Catalog catalog)
    {
        this.catalog = catalog;

    }

    public void addItem(String name) {
        if (catalog.hasProduct(name)) {
            basket.add(name);
        }
    }

    private int fullPrice() {
        int akku = 0;
        for (String s : basket) {
            akku += catalog.getProductPrice(s);
        }
        return akku;
    }

    public void print() {
        System.out.println("+-----------------------------------+-------+");
        System.out.println("|Pos|Produkt                        |Preis  |");
        System.out.println("+---+-------------------------------+-------+");
        for (int i = 0; i < basket.size(); i++) {
            String prod = basket.get(i);
            System.out.print("|");
            printSpaces(3 - Integer.toString(i + 1).length());
            System.out.print((i + 1) + "|");
            if (prod.length() < 31) {
                System.out.print(prod);
                printSpaces(31-prod.length());
            } else {
                System.out.print(prod.substring( 0, 31));
            }
            String preisAlsString = priceToString(catalog.getProductPrice(prod));
            System.out.print("|");
            printSpaces(6 - preisAlsString.length());
            System.out.print(preisAlsString + "€");
            System.out.println("|");
            // System.out.print("|  0,90|");
        }
        System.out.println("+---+-------------------------------+-------+");
        System.out.print("|                             Summe: ");
        String fullPriceString = priceToString(fullPrice());
        printSpaces(6 - fullPriceString.length());
        System.out.print(fullPriceString);
        System.out.println(" |");
        System.out.print("+---+-------------------------------+-------+");
    }

    private void printSpaces (int n) {
        int x = 0;
        while (x < n) {
            System.out.print(" ");
            x++;
        }
    }

    private String priceToString(int price) {   
        float pricex = price;
        float stringPrice = pricex / 100;
        String formatted = String.format("%.2f", stringPrice);
        String result = formatted.replace('.', ',');
        return formatted;
    }

    public void deleteItem (int n) {
        if (basket.get(n - 1) != null) {
            basket.remove(n - 1);
        } else {
            System.out.print("There is no item at the position number given!");
        }
    }

    public void deleteItems (String item) {
        for (int i = 0; i < basket.size(); i++) {
            if (basket.get(i).equals(item)) {
                basket.remove(i);
            }
        }
    }

    public void sortByName () {
        Collections.sort(basket);
    }

    public void printPackList () {
        sortByName();
        Iterator<String> iterator = basket.iterator();
        printSeparator ();
        System.out.println("|Produkt                        |Anzahl |");
        printSeparator ();
        String lastItem = null;
        int runningCount = 1;
        while (iterator.hasNext()) {
            String currentItem = iterator.next();
            if (lastItem == null) {
                lastItem = currentItem;
                currentItem = iterator.next();
            }
            if (lastItem.equals(currentItem)) {
                runningCount++;
            } else {
                printToPackList(lastItem, runningCount);
                runningCount = 1;
                lastItem = currentItem;
            }
            if (!iterator.hasNext()) {
                printToPackList(currentItem, runningCount);
            }
        }
        printSeparator ();
    }

    private void printToPackList (String item, int count) {
        System.out.print("|");
        if ((item.length() < 31)) {
            System.out.print(item);
            printSpaces(31- item.length());    
        } else {
            System.out.print(item.substring( 0, 31));
        }
        System.out.print("|");
        printSpaces(7 - Integer.toString(count).length());
        System.out.print(count);
        System.out.println("|");
    }

    private void printSeparator () {
        System.out.println("+-------------------------------+-------+");
    }
}


```

