
JavaSE

Plan de cours
1 Syntaxe de base et types de données 
2 Structures de contrôle
3 Fonctions et méthodes
4 Concepts de programmation orientée objet (POO)
5 Héritage et polymorphisme
6 Gestion des exceptions
7 Collections et génériques
8 Entrées/Sorties (I/O) en Java
Bonus - Concurrence et programmation multithread


1 Syntaxe de base et types de données 

## Objectifs
Maîtriser la syntaxe de base de Java et les types de données primitifs.


### 1. Variables et types de données primitifs
**Description :**
Les variables sont des conteneurs pour stocker des données. Java est un langage fortement typé, ce qui signifie que chaque variable doit être déclarée avec un type de données spécifique. Les types de données primitifs en Java incluent :
- `int` : pour les entiers (4 octets)
- `double` : pour les nombres à virgule flottante (8 octets)
- `char` : pour les caractères (2 octets)
- `boolean` : pour les valeurs de vérité (`true` ou `false`)

**Exemples de code :**
```java
int age = 25;
double price = 19.99;
char grade = 'A';
boolean isJavaFun = true;
```

**Exercice de pratique :**
Déclarez des variables pour représenter votre âge, votre taille (en mètres), la première lettre de votre prénom, et si vous aimez programmer en Java ou non. Affichez ces valeurs dans la console.

**Correction :**
```java
public class Main {
    public static void main(String[] args) {
        int age = 30;
        double height = 1.75;
        char firstInitial = 'J';
        boolean likesJava = true;

        System.out.println("Age: " + age);
        System.out.println("Height: " + height);
        System.out.println("First Initial: " + firstInitial);
        System.out.println("Likes Java: " + likesJava);
    }
}
```

### 2. Opérateurs arithmétiques et logiques
**Description :**
Les opérateurs arithmétiques permettent de réaliser des opérations mathématiques :
- `+` : addition
- `-` : soustraction
- `*` : multiplication
- `/` : division
- `%` : modulo (reste de la division entière)

Les opérateurs logiques permettent de réaliser des opérations logiques :
- `&&` : ET logique
- `||` : OU logique
- `!` : NON logique

**Exemples de code :**
```java
int a = 10;
int b = 5;
int sum = a + b;
int difference = a - b;
int product = a * b;
int quotient = a / b;
int remainder = a % b;

boolean result1 = (a > b) && (b < 20);
boolean result2 = (a < b) || (b == 5);
boolean result3 = !(a == b);
```

**Exercice de pratique :**
Calculez la somme, la différence, le produit, le quotient et le reste de la division de deux nombres. Vérifiez ensuite si les deux nombres sont égaux, si le premier est supérieur au second, et si le second est inférieur à 20.

**Correction :**
```java
public class Main {
    public static void main(String[] args) {
        int num1 = 12;
        int num2 = 4;
        
        int sum = num1 + num2;
        int difference = num1 - num2;
        int product = num1 + num2;
        int quotient = num1 / num2;
        int remainder = num1 % num2;
        
        System.out.println("Sum: " + sum);
        System.out.println("Difference: " + difference);
        System.out.println("Product: " + product);
        System.out.println("Quotient: " + quotient);
        System.out.println("Remainder: " + remainder);
        
        boolean isEqual = num1 == num2;
        boolean isNum1Greater = num1 > num2;
        boolean isNum2LessThan20 = num2 < 20;
        
        System.out.println("Numbers are equal: " + isEqual);
        System.out.println("First number is greater than second: " + isNum1Greater);
        System.out.println("Second number is less than 20: " + isNum2LessThan20);
    }
}
```

### 3. Entrées et sorties de base
**Description :**
En Java, la classe `Scanner` est utilisée pour lire les entrées utilisateur. `System.out.println` est utilisé pour afficher des messages à la console.

**Exemples de code :**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter your name: ");
        String name = scanner.nextLine();
        
        System.out.println("Hello, " + name + "!");
    }
}
```

**Exercice de pratique :**
Écrivez un programme qui demande à l'utilisateur de saisir son nom, son âge et sa ville, puis affiche ces informations.

**Correction :**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter your name: ");
        String name = scanner.nextLine();
        
        System.out.print("Enter your age: ");
        int age = scanner.nextInt();
        
        scanner.nextLine(); // Consuming the leftover newline
        
        System.out.print("Enter your city: ");
        String city = scanner.nextLine();
        
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("City: " + city);
    }
}
```



2 Structures de contrôle

### 1. Instructions conditionnelles
**Description :**
Les instructions conditionnelles permettent d'exécuter des blocs de code différents en fonction de certaines conditions. Les principales instructions conditionnelles en Java sont `if`, `else if`, `else`, et `switch`.

**Exemples de code :**
```java
public class Main {
    public static void main(String[] args) {
        int number = 10;

        // Instruction if
        if (number > 0) {
            System.out.println("The number is positive.");
        }

        // Instruction if-else
        if (number % 2 == 0) {
            System.out.println("The number is even.");
        } else {
            System.out.println("The number is odd.");
        }

        // Instruction if-else if-else
        if (number < 0) {
            System.out.println("The number is negative.");
        } else if (number == 0) {
            System.out.println("The number is zero.");
        } else {
            System.out.println("The number is positive.");
        }

        // Instruction switch
        int dayOfWeek = 3;
        switch (dayOfWeek) {
            case 1:
                System.out.println("Monday");
                break;
            case 2:
                System.out.println("Tuesday");
                break;
            case 3:
                System.out.println("Wednesday");
                break;
            case 4:
                System.out.println("Thursday");
                break;
            case 5:
                System.out.println("Friday");
                break;
            case 6:
                System.out.println("Saturday");
                break;
            case 7:
                System.out.println("Sunday");
                break;
            default:
                System.out.println("Invalid day");
        }
    }
}
```

**Exercice de pratique :**
Écrivez un programme qui demande à l'utilisateur de saisir un nombre entier. Si le nombre est positif, affichez "Positif". Si le nombre est négatif, affichez "Négatif". Si le nombre est zéro, affichez "Zéro". Utilisez également une instruction `switch` pour afficher le jour de la semaine correspondant à un nombre entre 1 et 7.

**Correction :**
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int number = scanner.nextInt();

        if (number > 0) {
            System.out.println("Positif");
        } else if (number < 0) {
            System.out.println("Négatif");
        } else {
            System.out.println("Zéro");
        }

        System.out.print("Enter a number for the day of the week (1-7): ");
        int dayOfWeek = scanner.nextInt();

        switch (dayOfWeek) {
            case 1:
                System.out.println("Lundi");
                break;
            case 2:
                System.out.println("Mardi");
                break;
            case 3:
                System.out.println("Mercredi");
                break;
            case 4:
                System.out.println("Jeudi");
                break;
            case 5:
                System.out.println("Vendredi");
                break;
            case 6:
                System.out.println("Samedi");
                break;
            case 7:
                System.out.println("Dimanche");
                break;
            default:
                System.out.println("Jour invalide");
        }
    }
}
```

### 2. Boucles
**Description :**
Les boucles permettent de répéter l'exécution d'un bloc de code. Les principales boucles en Java sont `for`, `while`, et `do-while`.

**Exemples de code :**
```java
public class Main {
    public static void main(String[] args) {
        // Boucle for
        for (int i = 0; i < 5; i++) {
            System.out.println("For loop iteration: " + i);
        }

        // Boucle while
        int j = 0;
        while (j < 5) {
            System.out.println("While loop iteration: " + j);
            j++;
        }

        // Boucle do-while
        int k = 0;
        do {
            System.out.println("Do-While loop iteration: " + k);
            k++;
        } while (k < 5);
    }
}
```

**Exercice de pratique :**
Écrivez un programme qui affiche les nombres de 1 à 10 en utilisant une boucle `for`, puis les mêmes nombres en utilisant une boucle `while`, et enfin en utilisant une boucle `do-while`.

**Correction :**
```java
public class Main {
    public static void main(String[] args) {
        // Boucle for
        for (int i = 1; i <= 10; i++) {
            System.out.println("For loop: " + i);
        }

        // Boucle while
        int j = 1;
        while (j <= 10) {
            System.out.println("While loop: " + j);
            j++;
        }

        // Boucle do-while
        int k = 1;
        do {
            System.out.println("Do-While loop: " + k);
            k++;
        } while (k <= 10);
    }
}
```

### 3. Utilisation de `break` et `continue`
**Description :**
Les instructions `break` et `continue` sont utilisées pour contrôler le flux à l'intérieur des boucles. `break` permet de sortir prématurément d'une boucle, tandis que `continue` permet de sauter à l'itération suivante de la boucle.

**Exemples de code :**
```java
public class Main {
    public static void main(String[] args) {
        // Utilisation de break
        for (int i = 0; i < 10; i++) {
            if (i == 5) {
                break; // Sort de la boucle quand i vaut 5
            }
            System.out.println("Break example, i = " + i);
        }

        // Utilisation de continue
        for (int j = 0; j < 10; j++) {
            if (j % 2 == 0) {
                continue; // Passe à l'itération suivante quand j est pair
            }
            System.out.println("Continue example, j = " + j);
        }
    }
}
```

**Exercice de pratique :**
Écrivez un programme qui affiche les nombres de 1 à 10, mais sort de la boucle lorsque le nombre atteint 7. Ensuite, écrivez un programme qui affiche les nombres impairs de 1 à 10 en sautant les nombres pairs.

**Correction :**
```java
public class Main {
    public static void main(String[] args) {
        // Utilisation de break
        for (int i = 1; i <= 10; i++) {
            if (i == 7) {
                break; // Sort de la boucle quand i vaut 7
            }
            System.out.println("Break example, i = " + i);
        }

        // Utilisation de continue
        for (int j = 1; j <= 10; j++) {
            if (j % 2 == 0) {
                continue; // Passe à l'itération suivante quand j est pair
            }
            System.out.println("Continue example, j = " + j);
        }
    }
}
```



3 Fonctions et méthodes

## Objectifs
Définir et appeler des fonctions en Java.

## Contenu

### 1. Définition de méthodes
**Description :**
Une méthode est un bloc de code qui ne s'exécute que lorsqu'il est appelé. Vous pouvez passer des données, appelées paramètres, à une méthode. Les méthodes sont utilisées pour effectuer certaines actions, et elles sont également connues sous le nom de fonctions.

**Exemples de code :**
```java
public class Main {
    // Définition d'une méthode
    static void myMethod() {
        System.out.println("Hello, this is my method!");
    }

    public static void main(String[] args) {
        // Appel de la méthode
        myMethod();
    }
}
```

**Exercice de pratique :**
Définissez une méthode appelée `greet` qui affiche un message de salutation. Appelez cette méthode depuis la méthode `main`.

**Correction :**
```java
public class Main {
    // Définition de la méthode greet
    static void greet() {
        System.out.println("Hello, welcome to Java programming!");
    }

    public static void main(String[] args) {
        // Appel de la méthode greet
        greet();
    }
}
```

### 2. Appel de méthodes
**Description :**
Les méthodes sont appelées en écrivant leur nom suivi de parenthèses. Vous pouvez appeler une méthode autant de fois que nécessaire.

**Exemples de code :**
```java
public class Main {
    static void myMethod() {
        System.out.println("I just got executed!");
    }

    public static void main(String[] args) {
        myMethod();
        myMethod();
        myMethod();
    }
}
```

**Exercice de pratique :**
Définissez une méthode appelée `displayNumber` qui prend un entier en paramètre et affiche ce nombre. Appelez cette méthode trois fois avec des nombres différents.

**Correction :**
```java
public class Main {
    // Définition de la méthode displayNumber
    static void displayNumber(int num) {
        System.out.println("The number is: " + num);
    }

    public static void main(String[] args) {
        // Appel de la méthode displayNumber avec des nombres différents
        displayNumber(5);
        displayNumber(10);
        displayNumber(15);
    }
}
```

### 3. Passage de paramètres et retour de valeurs
**Description :**
Les méthodes peuvent prendre des paramètres et renvoyer des valeurs. Les paramètres agissent comme des variables à l'intérieur de la méthode. Vous pouvez également retourner une valeur à l'aide du mot-clé `return`.

**Exemples de code :**
```java
public class Main {
    // Méthode avec paramètres et retour de valeur
    static int addNumbers(int a, int b) {
        return a + b;
    }

    public static void main(String[] args) {
        int sum = addNumbers(5, 10);
        System.out.println("Sum: " + sum);
    }
}
```

**Exercice de pratique :**
Définissez une méthode appelée `multiply` qui prend deux nombres en paramètres et renvoie leur produit. Appelez cette méthode et affichez le résultat.

**Correction :**
```java
public class Main {
    // Définition de la méthode multiply
    static int multiply(int a, int b) {
        return a * b;
    }

    public static void main(String[] args) {
        int product = multiply(4, 5);
        System.out.println("Product: " + product);
    }
}
```

### 4. Surcharge de méthodes
**Description :**
Java permet de définir plusieurs méthodes avec le même nom, à condition que leurs paramètres soient différents. Cette fonctionnalité est appelée surcharge de méthodes.

**Exemples de code :**
```java
public class Main {
    // Méthode sans paramètres
    static void display() {
        System.out.println("No parameters");
    }

    // Méthode avec un paramètre entier
    static void display(int a) {
        System.out.println("Parameter: " + a);
    }

    public static void main(String[] args) {
        display();
        display(5);
    }
}
```

**Exercice de pratique :**
Définissez une méthode `print` qui affiche un message. Surchargez cette méthode pour qu'elle puisse également afficher un entier et une chaîne de caractères. Appelez chaque version de la méthode `print`.

**Correction :**
```java
public class Main {
    // Méthode print sans paramètres
    static void print() {
        System.out.println("Printing a message");
    }

    // Surcharge de la méthode print avec un paramètre entier
    static void print(int a) {
        System.out.println("Printing an integer: " + a);
    }

    // Surcharge de la méthode print avec une chaîne de caractères
    static void print(String message) {
        System.out.println("Printing a string: " + message);
    }

    public static void main(String[] args) {
        print();
        print(10);
        print("Hello, World!");
    }
}
```



4 Concepts de programmation orientée objet (POO)




### 1. Classes et objets
**Description :**
Une classe est un plan pour créer des objets. Un objet est une instance d'une classe. Les classes contiennent des attributs (variables) et des méthodes (fonctions) qui définissent le comportement des objets.

**Exemples de code :**
```java
// Définition de la classe
public class Car {
    // Attributs
    String color;
    int year;

    // Méthode
    void displayDetails() {
        System.out.println("Car color: " + color);
        System.out.println("Car year: " + year);
    }
}

// Utilisation de la classe dans la méthode main
public class Main {
    public static void main(String[] args) {
        Car myCar = new Car(); // Création d'un objet
        myCar.color = "Red"; // Initialisation des attributs
        myCar.year = 2021;
        myCar.displayDetails(); // Appel de la méthode
    }
}
```

**Exercice de pratique :**
Définissez une classe `Person` avec des attributs `name` et `age`, et une méthode `displayInfo` qui affiche ces attributs. Créez un objet de cette classe dans la méthode `main` et initialisez les attributs avant d'appeler `displayInfo`.

**Correction :**
```java
public class Person {
    String name;
    int age;

    void displayInfo() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

public class Main {
    public static void main(String[] args) {
        Person person = new Person();
        person.name = "Alice";
        person.age = 30;
        person.displayInfo();
    }
}
```

### 2. Attributs et méthodes
**Description :**
Les attributs sont des variables définies dans une classe. Les méthodes sont des fonctions définies dans une classe. Les attributs et les méthodes définissent le comportement des objets créés à partir de la classe.

**Exemples de code :**
```java
public class Dog {
    String breed;
    int age;

    void bark() {
        System.out.println("Woof!");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog();
        myDog.breed = "Labrador";
        myDog.age = 3;
        System.out.println("Breed: " + myDog.breed);
        System.out.println("Age: " + myDog.age);
        myDog.bark();
    }
}
```

**Exercice de pratique :**
Définissez une classe `Book` avec des attributs `title` et `author`, et une méthode `displayDetails` qui affiche ces attributs. Créez un objet de cette classe dans la méthode `main`, initialisez les attributs et appelez `displayDetails`.

**Correction :**
```java
public class Book {
    String title;
    String author;

    void displayDetails() {
        System.out.println("Title: " + title);
        System.out.println("Author: " + author);
    }
}

public class Main {
    public static void main(String[] args) {
        Book myBook = new Book();
        myBook.title = "1984";
        myBook.author = "George Orwell";
        myBook.displayDetails();
    }
}
```

### 3. Constructeurs
**Description :**
Les constructeurs sont des méthodes spéciales appelées lors de la création d'un objet. Ils sont utilisés pour initialiser les objets.

**Exemples de code :**
```java
public class Student {
    String name;
    int age;

    // Constructeur
    public Student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    void displayInfo() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

public class Main {
    public static void main(String[] args) {
        Student student = new Student("Bob", 22);
        student.displayInfo();
    }
}
```

**Exercice de pratique :**
Définissez une classe `Movie` avec des attributs `title` et `year`, et un constructeur pour initialiser ces attributs. Ajoutez une méthode `displayDetails` et créez un objet de la classe `Movie` dans la méthode `main`, en appelant `displayDetails`.

**Correction :**
```java
public class Movie {
    String title;
    int year;

    // Constructeur
    public Movie(String title, int year) {
        this.title = title;
        this.year = year;
    }

    void displayDetails() {
        System.out.println("Title: " + title);
        System.out.println("Year: " + year);
    }
}

public class Main {
    public static void main(String[] args) {
        Movie myMovie = new Movie("Inception", 2010);
        myMovie.displayDetails();
    }
}

### 4. Encapsulation
**Description :**
L'encapsulation est une technique qui consiste à restreindre l'accès à certains composants d'un objet et à les protéger contre les modifications non autorisées. Les modificateurs d'accès (`private`, `public`, `protected`) sont utilisés pour contrôler l'accès aux membres d'une classe.

**Exemples de code :**
```java
public class Account {
    private double balance;

    // Méthode pour déposer de l'argent
    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
        }
    }

    // Méthode pour retirer de l'argent
    public void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
        }
    }

    // Méthode pour obtenir le solde
    public double getBalance() {
        return balance;
    }
}

public class Main {
    public static void main(String[] args) {
        Account myAccount = new Account();
        myAccount.deposit(100);
        myAccount.withdraw(30);
        System.out.println("Balance: " + myAccount.getBalance());
    }
}
```

**Exercice de pratique :**
Définissez une classe `BankAccount` avec un attribut `balance` privé, et des méthodes `deposit`, `withdraw` et `getBalance` pour gérer l'accès à cet attribut. Créez un objet de cette classe dans la méthode `main`, effectuez quelques opérations de dépôt et de retrait, et affichez le solde.

**Correction :**
```java
public class BankAccount {
    private double balance;

    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
        }
    }

    public void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
        }
    }

    public double getBalance() {
        return balance;
    }
}

public class Main {
    public static void main(String[] args) {
        BankAccount myAccount = new BankAccount();
        myAccount.deposit(500);
        myAccount.withdraw(200);
        System.out.println("Balance: " + myAccount.getBalance());
    }
}
```

### 5. Getters et Setters
**Description :**
Les getters et setters sont des méthodes utilisées pour accéder et modifier les valeurs des attributs privés d'une classe.

**Exemples de code :**
```java
public class Employee {
    private String name;
    private int id;

    // Getter pour le nom
    public String getName() {
        return name;
    }

    // Setter pour le nom
    public void setName(String name) {
        this.name = name;
    }

    // Getter pour l'ID
    public int getId() {
        return id;
    }

    // Setter pour l'ID
    public void setId(int id) {
        this.id = id;
    }
}

public class Main {
    public static void main(String[] args) {
        Employee emp = new Employee();
        emp.setName("John Doe");
        emp.setId(12345);
        System.out.println("Employee Name: " + emp.getName());
        System.out.println("Employee ID: " + emp.getId());
    }
}
```

**Exercice de pratique :**
Définissez une classe `Product` avec des attributs privés `name` et `price`. Ajoutez des getters et setters pour ces

 attributs. Créez un objet de cette classe dans la méthode `main`, initialisez les attributs en utilisant les setters et affichez les valeurs en utilisant les getters.

**Correction :**
```java
public class Product {
    private String name;
    private double price;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public double getPrice() {
        return price;
    }

    public void setPrice(double price) {
        this.price = price;
    }
}

public class Main {
    public static void main(String[] args) {
        Product product = new Product();
        product.setName("Laptop");
        product.setPrice(799.99);
        System.out.println("Product Name: " + product.getName());
        System.out.println("Product Price: $" + product.getPrice());
    }
}
```

5 Héritage et polymorphisme


### 1. Héritage
**Description :**
L'héritage permet de créer une nouvelle classe à partir d'une classe existante. La nouvelle classe (classe dérivée ou sous-classe) hérite des attributs et méthodes de la classe existante (classe de base ou super-classe).

**Exemples de code :**
```java
// Classe de base
public class Animal {
    String name;

    void eat() {
        System.out.println("This animal is eating.");
    }
}

// Classe dérivée
public class Dog extends Animal {
    void bark() {
        System.out.println("Woof!");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog();
        myDog.name = "Buddy";
        myDog.eat(); // Appel de la méthode héritée
        myDog.bark(); // Appel de la méthode de la sous-classe
    }
}
```

**Exercice de pratique :**
Définissez une classe `Person` avec un attribut `name` et une méthode `displayInfo`. Créez une sous-classe `Employee` qui ajoute un attribut `employeeId` et une méthode `displayEmployeeInfo`. Créez un objet de la classe `Employee` dans la méthode `main`, initialisez les attributs et appelez les deux méthodes.

**Correction :**
```java
public class Person {
    String name;

    void displayInfo() {
        System.out.println("Name: " + name);
    }
}

public class Employee extends Person {
    int employeeId;

    void displayEmployeeInfo() {
        System.out.println("Employee ID: " + employeeId);
    }
}

public class Main {
    public static void main(String[] args) {
        Employee emp = new Employee();
        emp.name = "Alice";
        emp.employeeId = 12345;
        emp.displayInfo();
        emp.displayEmployeeInfo();
    }
}
```

### 2. Polymorphisme
**Description :**
Le polymorphisme permet à une méthode d'avoir plusieurs implémentations. Il peut être réalisé via la substitution et l'extension des méthodes héritées.

**Exemples de code :**
```java
// Classe de base
public class Animal {
    void makeSound() {
        System.out.println("Some generic animal sound");
    }
}

// Sous-classe
public class Dog extends Animal {
    @Override
    void makeSound() {
        System.out.println("Woof!");
    }
}

// Sous-classe
public class Cat extends Animal {
    @Override
    void makeSound() {
        System.out.println("Meow!");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Animal();
        Animal myDog = new Dog();
        Animal myCat = new Cat();

        myAnimal.makeSound();
        myDog.makeSound();
        myCat.makeSound();
    }
}
```

**Exercice de pratique :**
Créez une classe `Shape` avec une méthode `draw`. Créez deux sous-classes `Circle` et `Rectangle` qui redéfinissent la méthode `draw`. Dans la méthode `main`, créez des objets de `Circle` et `Rectangle`, et appelez la méthode `draw` sur chacun d'eux.

**Correction :**
```java
public class Shape {
    void draw() {
        System.out.println("Drawing a shape");
    }
}

public class Circle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing a circle");
    }
}

public class Rectangle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing a rectangle");
    }
}

public class Main {
    public static void main(String[] args) {
        Shape myShape = new Shape();
        Shape myCircle = new Circle();
        Shape myRectangle = new Rectangle();

        myShape.draw();
        myCircle.draw();
        myRectangle.draw();
    }
}
```

### 3. Méthodes abstraites et interfaces
**Description :**
Les méthodes abstraites sont déclarées sans implémentation dans une classe abstraite. Une interface est une collection de méthodes abstraites et de constantes. Les classes qui implémentent des interfaces doivent fournir des implémentations pour toutes les méthodes de l'interface.

**Exemples de code :**
```java
// Classe abstraite
abstract class Animal {
    abstract void makeSound();

    void sleep() {
        System.out.println("This animal is sleeping.");
    }
}

// Sous-classe concrète
public class Dog extends Animal {
    @Override
    void makeSound() {
        System.out.println("Woof!");
    }
}

// Interface
interface AnimalInterface {
    void eat();
    void makeSound();
}

// Classe qui implémente l'interface
public class Cat implements AnimalInterface {
    @Override
    public void eat() {
        System.out.println("The cat is eating.");
    }

    @Override
    public void makeSound() {
        System.out.println("Meow!");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog myDog = new Dog();
        myDog.makeSound();
        myDog.sleep();

        Cat myCat = new Cat();
        myCat.eat();
        myCat.makeSound();
    }
}
```

**Exercice de pratique :**
Définissez une classe abstraite `Vehicle` avec une méthode abstraite `move`. Créez deux sous-classes `Car` et `Bicycle` qui redéfinissent la méthode `move`. Créez une interface `Horn` avec une méthode `honk`. Faites en sorte que `Car` et `Bicycle` implémentent l'interface `Horn` et définissez la méthode `honk`. Dans la méthode `main`, créez des objets de `Car` et `Bicycle`, et appelez les méthodes `move` et `honk` sur chacun d'eux.

**Correction :**
```java
// Classe abstraite
abstract class Vehicle {
    abstract void move();
}

// Sous-classe
public class Car extends Vehicle implements Horn {
    @Override
    void move() {
        System.out.println("The car is moving");
    }

    @Override
    public void honk() {
        System.out.println("Car honk: Beep beep!");
    }
}

// Sous-classe
public class Bicycle extends Vehicle implements Horn {
    @Override
    void move() {
        System.out.println("The bicycle is moving");
    }

    @Override
    public void honk() {
        System.out.println("Bicycle honk: Ring ring!");
    }
}

// Interface
interface Horn {
    void honk();
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car();
        Bicycle myBicycle = new Bicycle();

        myCar.move();
        myCar.honk();

        myBicycle.move();
        myBicycle.honk();
    }
}
```


6 Gestion des exceptions



### 1. Types d'exceptions
**Description :**
Java possède deux types d'exceptions : les exceptions vérifiées (checked exceptions) et les exceptions non vérifiées (unchecked exceptions). Les exceptions vérifiées doivent être déclarées dans la signature de la méthode ou capturées dans un bloc `try-catch`, tandis que les exceptions non vérifiées sont des sous-classes de `RuntimeException` et n'ont pas besoin d'être déclarées ou capturées explicitement.

**Exemples de code :**
```java
// Exception vérifiée
import java.io.File;
import java.io.FileReader;
import java.io.IOException;

public class CheckedExceptionExample {
    public static void main(String[] args) {
        try {
            File file = new File("test.txt");
            FileReader fr = new FileReader(file);
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}

// Exception non vérifiée
public class UncheckedExceptionExample {
    public static void main(String[] args) {
        int[] numbers = {1, 2, 3};
        System.out.println(numbers[3]); // Provoque une ArrayIndexOutOfBoundsException
    }
}
```

**Exercice de pratique :**
Écrivez un programme qui lit un fichier texte et affiche son contenu. Si le fichier n'existe pas, capturez l'exception et affichez un message d'erreur. Ajoutez également un exemple d'exception non vérifiée.

**Correction :**
```java
import java.io.File;
import java.io.FileReader;
import java.io.BufferedReader;
import java.io.IOException;

public class ExceptionHandlingExample {
    public static void main(String[] args) {
        try {
            File file = new File("example.txt");
            FileReader fr = new FileReader(file);
            BufferedReader br = new BufferedReader(fr);
            String line;
            while ((line = br.readLine()) != null) {
                System.out.println(line);
            }
            br.close();
            fr.close();
        } catch (IOException e) {
            System.out.println("File not found: " + e.getMessage());
        }

        // Exception non vérifiée
        try {
            int[] numbers = {1, 2, 3};
            System.out.println(numbers[3]);
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Array index out of bounds: " + e.getMessage());
        }
    }
}
```

### 2. Bloc `try-catch`
**Description :**
Le bloc `try-catch` est utilisé pour capturer et gérer les exceptions en Java. Le code susceptible de lancer une exception est placé dans le bloc `try`, et le bloc `catch` capture l'exception et permet de la gérer.

**Exemples de code :**
```java
public class TryCatchExample {
    public static void main(String[] args) {
        try {
            int result = 10 / 0; // Provoque une ArithmeticException
        } catch (ArithmeticException e) {
            System.out.println("Cannot divide by zero: " + e.getMessage());
        }
    }
}
```

**Exercice de pratique :**
Écrivez un programme qui demande à l'utilisateur de saisir deux nombres et affiche le résultat de la division du premier nombre par le second. Utilisez un bloc `try-catch` pour gérer l'exception si l'utilisateur saisit zéro comme deuxième nombre.

**Correction :**
```java
import java.util.Scanner;

public class DivisionExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the first number: ");
        int num1 = scanner.nextInt();

        System.out.print("Enter the second number: ");
        int num2 = scanner.nextInt();

        try {
            int result = num1 / num2;
            System.out.println("Result: " + result);
        } catch (ArithmeticException e) {
            System.out.println("Cannot divide by zero: " + e.getMessage());
        }
    }
}
```

### 3. Bloc `finally`
**Description :**
Le bloc `finally` est utilisé pour exécuter du code après le bloc `try-catch`, que l'exception soit levée ou non. Il est souvent utilisé pour libérer des ressources comme des fichiers ou des connexions réseau.

**Exemples de code :**
```java
import java.io.File;
import java.io.FileReader;
import java.io.IOException;

public class FinallyExample {
    public static void main(String[] args) {
        FileReader fr = null;
        try {
            File file = new File("test.txt");
            fr = new FileReader(file);
            // Lire le fichier
        } catch (IOException e) {
            System.out.println("File not found: " + e.getMessage());
        } finally {
            try {
                if (fr != null) {
                    fr.close();
                }
            } catch (IOException e) {
                System.out.println("Error closing the file: " + e.getMessage());
            }
        }
    }
}
```

**Exercice de pratique :**
Écrivez un programme qui ouvre un fichier et lit son contenu. Utilisez un bloc `finally` pour fermer le fichier, qu'une exception soit levée ou non.

**Correction :**
```java
import java.io.File;
import java.io.FileReader;
import java.io.BufferedReader;
import java.io.IOException;

public class FinallyExamplePractice {
    public static void main(String[] args) {
        FileReader fr = null;
        try {
            File file = new File("example.txt");
            fr = new FileReader(file);
            BufferedReader br = new BufferedReader(fr);
            String line;
            while ((line = br.readLine()) != null) {
                System.out.println(line);
            }
            br.close();
        } catch (IOException e) {
            System.out.println("File not found: " + e.getMessage());
        } finally {
            try {
                if (fr != null) {
                    fr.close();
                }
            } catch (IOException e) {
                System.out.println("Error closing the file: " + e.getMessage());
            }
        }
    }
}
```




7 Collections et génériques


### 1. Collections
**Description :**
Les collections sont des structures de données qui permettent de regrouper des objets. Java fournit plusieurs classes de collection, notamment `ArrayList`, `LinkedList`, `HashSet`, et `HashMap`.

**Exemples de code :**
```java
import java.util.ArrayList;
import java.util.HashSet;
import java.util.HashMap;

public class CollectionsExample {
    public static void main(String[] args) {
        // Utilisation de ArrayList
        ArrayList<String> list = new ArrayList<>();
        list.add("Apple");
        list.add("Banana");
        list.add("Orange");
        System.out.println("ArrayList: " + list);

        // Utilisation de HashSet
        HashSet<String> set = new HashSet<>();
        set.add("Apple");
        set.add("Banana");
        set.add("Apple"); // Duplicate entry, will be ignored
        System.out.println("HashSet: " + set);

        // Utilisation de HashMap
        HashMap<Integer, String> map = new HashMap<>();
        map.put(1, "One");
        map.put(2, "Two");
        map.put(3, "Three");
        System.out.println("HashMap: " + map);
    }
}
```

**Exercice de pratique :**
Écrivez un programme qui utilise `ArrayList` pour stocker une liste de noms d'animaux, `HashSet` pour stocker une liste de couleurs sans doublons, et `HashMap` pour stocker des paires clé-valeur représentant des numéros d'étudiants et leurs noms. Affichez les éléments de chaque collection.

**Correction :**
```java
import java.util.ArrayList;
import java.util.HashSet;
import java.util.HashMap;

public class CollectionsPractice {
    public static void main(String[] args) {
        // Utilisation de ArrayList
        ArrayList<String> animals = new ArrayList<>();
        animals.add("Dog");
        animals.add("Cat");
        animals.add("Horse");
        System.out.println("ArrayList of animals: " + animals);

        // Utilisation de HashSet
        HashSet<String> colors = new HashSet<>();
        colors.add("Red");
        colors.add("Blue");
        colors.add("Red"); // Duplicate entry, will be ignored
        System.out.println("HashSet of colors: " + colors);

        // Utilisation de HashMap
        HashMap<Integer, String> studentMap = new HashMap<>();
        studentMap.put(101, "Alice");
        studentMap.put(102, "Bob");
        studentMap.put(103, "Charlie");
        System.out.println("HashMap of students: " + studentMap);
    }
}
```

### 2. Génériques
**Description :**
Les génériques permettent de créer des classes, des interfaces et des méthodes paramétrées par des types. Ils fournissent une vérification de type au moment de la compilation et éliminent le besoin de castings explicites.

**Exemples de code :**
```java
// Classe générique
public class Box<T> {
    private T content;

    public void setContent(T content) {
        this.content = content;
    }

    public T getContent() {
        return content;
    }

    public static void main(String[] args) {
        Box<String> stringBox = new Box<>();
        stringBox.setContent("Hello");
        System.out.println("String content: " + stringBox.getContent());

        Box<Integer> intBox = new Box<>();
        intBox.setContent(123);
        System.out.println("Integer content: " + intBox.getContent());
    }
}
```

**Exercice de pratique :**
Créez une classe générique `Pair` qui stocke deux objets de types différents. Ajoutez des méthodes pour définir et obtenir les valeurs des objets. Testez la classe en créant des instances de `Pair` avec différents types.

**Correction :**
```java
// Classe générique
public class Pair<U, V> {
    private U first;
    private V second;

    public void setFirst(U first) {
        this.first = first;
    }

    public U getFirst() {
        return first;
    }

    public void setSecond(V second) {
        this.second = second;
    }

    public V getSecond() {
        return second;
    }

    public static void main(String[] args) {
        Pair<String, Integer> pair = new Pair<>();
        pair.setFirst("Age");
        pair.setSecond(30);
        System.out.println("First: " + pair.getFirst() + ", Second: " + pair.getSecond());

        Pair<Double, Character> anotherPair = new Pair<>();
        anotherPair.setFirst(3.14);
        anotherPair.setSecond('π');
        System.out.println("First: " + anotherPair.getFirst() + ", Second: " + anotherPair.getSecond());
    }
}
```

### 3. Utilisation avancée des génériques
**Description :**
Les génériques peuvent être utilisés avec des méthodes, des interfaces et des bornes de type (type bounds) pour créer des structures de données réutilisables et sûres.

**Exemples de code :**
```java
// Méthode générique
public class GenericMethodExample {
    public static <T> void printArray(T[] array) {
        for (T element : array) {
            System.out.print(element + " ");
        }
        System.out.println();
    }

    public static void main(String[] args) {
        Integer[] intArray = {1, 2, 3, 4, 5};
        String[] stringArray = {"A", "B", "C", "D"};

        printArray(intArray);
        printArray(stringArray);
    }
}
```

**Exercice de pratique :**
Créez une méthode générique `swap` qui échange deux éléments dans un tableau. Testez cette méthode avec des tableaux de différents types.

**Correction :**
```java
public class GenericSwapExample {
    public static <T> void swap(T[] array, int index1, int index2) {
        T temp = array[index1];
        array[index1] = array[index2];
        array[index2] = temp;
    }

    public static void main(String[] args) {
        Integer[] intArray = {1, 2, 3, 4, 5};
        String[] stringArray = {"A", "B", "C", "D"};

        System.out.println("Before swap:");
        for (int i : intArray) {
            System.out.print(i + " ");
        }
        System.out.println();
        
        swap(intArray, 0, 4);
        
        System.out.println("After swap:");
        for (int i : intArray) {
            System.out.print(i + " ");
        }
        System.out.println();
    }
}
```

### 4. Définition et lancement des exceptions personnalisées
**Description :**
Vous pouvez définir vos propres exceptions en étendant la classe `Exception` ou `RuntimeException`. Cela vous permet de lancer des exceptions spécifiques à votre application.

**Exemples de code :**
```java
// Définition de l'exception personnalisée
class CustomException extends Exception {
    public CustomException(String message) {
        super(message);
    }
}

public class CustomExceptionExample {
    public static void main(String[] args) {
        try {
            validateAge(15);
        } catch (CustomException e) {
            System.out.println("Caught custom exception: " + e.getMessage());
        }
    }

    // Méthode qui lance l'exception personnalisée
    static void validateAge(int age) throws CustomException {
        if (age < 18) {
            throw new CustomException("Age must be 18 or older");
        }
    }
}
```

**Exercice de pratique :**
Définissez une exception personnalisée `InsufficientBalanceException` et une méthode `withdraw` dans une classe `BankAccount`. La méthode `withdraw` doit lancer l'exception personnalisée si le solde est insuffisant. Testez cette méthode dans la méthode `main`.

**Correction :**
```java
// Définition de l'exception personnalisée
class InsufficientBalanceException extends Exception {
    public InsufficientBalanceException(String message) {
        super(message);
    }
}

public class BankAccount {
    private double balance;

    public BankAccount(double balance) {
        this.balance = balance;
    }

    public void withdraw(double amount) throws InsufficientBalanceException {
        if (amount > balance) {
            throw new InsufficientBalanceException("Insufficient balance");
        }
        balance -= amount;
    }

    public double getBalance() {
        return balance;
    }

    public static void main(String[] args) {
        BankAccount account = new BankAccount(100);

        try {
            account.withdraw(150);
        } catch (InsufficientBalanceException e) {
            System.out.println("Caught custom exception: " + e.getMessage());
        }

        System.out.println("Current balance: " + account.getBalance());
    }
}
```




8 Entrées/Sorties (I/O) en Java



### 1. Lecture et écriture de fichiers
**Description :**
Java fournit plusieurs classes pour lire et écrire des fichiers, notamment `FileReader`, `BufferedReader`, `FileWriter`, et `BufferedWriter`.

**Exemples de code :**
```java
import java.io.*;

public class FileIOExample {
    public static void main(String[] args) {
        // Écriture dans un fichier
        try (BufferedWriter writer = new BufferedWriter(new FileWriter("example.txt"))) {
            writer.write("Hello, World!");
            writer.newLine();
            writer.write("Java File I/O is simple.");
        } catch (IOException e) {
            e.printStackTrace();
        }

        // Lecture depuis un fichier
        try (BufferedReader reader = new BufferedReader(new FileReader("example.txt"))) {
            String line;
            while ((line = reader.readLine()) != null) {
                System.out.println(line);
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

**Exercice de pratique :**
Écrivez un programme qui lit un fichier texte ligne par ligne et affiche son contenu. Écrivez également du texte dans un fichier en utilisant `BufferedWriter`.

**Correction :**
```java
import java.io.*;

public class FileIOPractice {
    public static void main(String[] args) {
        // Écriture dans un fichier
        try (BufferedWriter writer = new BufferedWriter(new FileWriter("practice.txt"))) {
            writer.write("This is a practice file.");
            writer.newLine();
            writer.write("We are learning Java I/O.");
        } catch (IOException e) {
            e.printStackTrace();
        }

        // Lecture depuis un fichier
        try (BufferedReader reader = new BufferedReader(new FileReader("practice.txt"))) {
            String line;
            while ((line = reader.readLine()) != null) {
                System.out.println(line);
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

### 2. Sérialisation
**Description :**
La sérialisation est le processus de conversion d'un objet en un flux de bytes afin qu'il puisse être facilement sauvegardé dans un fichier ou transmis sur un réseau. La désérialisation est l'opération inverse. Pour sérialiser un objet, il doit implémenter l'interface `Serializable`.

**Exemples de code :**
```java
import java.io.*;

class Person implements Serializable {
    private static final long serialVersionUID = 1L;
    String name;
    int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

public class SerializationExample {
    public static void main(String[] args) {
        // Sérialisation
        try (ObjectOutputStream out = new ObjectOutputStream(new FileOutputStream("person.ser"))) {
            Person person = new Person("Alice", 30);
            out.writeObject(person);
        } catch (IOException e) {
            e.printStackTrace();
        }

        // Désérialisation
        try (ObjectInputStream in = new ObjectInputStream(new FileInputStream("person.ser"))) {
            Person person = (Person) in.readObject();
            System.out.println("Name: " + person.name);
            System.out.println("Age: " + person.age);
        } catch (IOException | ClassNotFoundException e) {
            e.printStackTrace();
        }
    }
}
```

**Exercice de pratique :**
Créez une classe `Employee` qui implémente `Serializable` avec des attributs `name` et `salary`. Sérialisez un objet de `Employee` dans un fichier et désérialisez-le pour afficher ses attributs.

**Correction :**
```java
import java.io.*;

class Employee implements Serializable {
    private static final long serialVersionUID = 1L;
    String name;
    double salary;

    public Employee(String name, double salary) {
        this.name = name;
        this.salary = salary;
    }
}

public class EmployeeSerialization {
    public static void main(String[] args) {
        // Sérialisation
        try (ObjectOutputStream out = new ObjectOutputStream(new FileOutputStream("employee.ser"))) {
            Employee emp = new Employee("John Doe", 50000);
            out.writeObject(emp);
        } catch (IOException e) {
            e.printStackTrace();
        }

        // Désérialisation
        try (ObjectInputStream in = new ObjectInputStream(new FileInputStream("employee.ser"))) {
            Employee emp = (Employee) in.readObject();
            System.out.println("Name: " + emp.name);
            System.out.println("Salary: " + emp.salary);
        } catch (IOException | ClassNotFoundException e) {
            e.printStackTrace();
        }
    }
}
```

### 3. Gestion des flux de données
**Description :**
Java permet de travailler avec différents types de flux de données (InputStream, OutputStream, Reader, Writer) pour gérer les opérations d'entrée/sortie.

**Exemples de code :**
```java
import java.io.*;

public class DataStreamExample {
    public static void main(String[] args) {
        // Écriture de données primitives dans un fichier
        try (DataOutputStream out = new DataOutputStream(new FileOutputStream("data.bin"))) {
            out.writeInt(123);
            out.writeDouble(45.67);
            out.writeBoolean(true);
        } catch (IOException e) {
            e.printStackTrace();
        }

        // Lecture de données primitives depuis un fichier
        try (DataInputStream in = new DataInputStream(new FileInputStream("data.bin"))) {
            int intValue = in.readInt();
            double doubleValue = in.readDouble();
            boolean booleanValue = in.readBoolean();

            System.out.println("Integer: " + intValue);
            System.out.println("Double: " + doubleValue);
            System.out.println("Boolean: " + booleanValue);
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

**Exercice de pratique :**
Écrivez un programme qui utilise `DataOutputStream` pour écrire des valeurs primitives dans un fichier et `DataInputStream` pour les lire et les afficher.

**Correction :**
```java
import java.io.*;

public class DataStreamPractice {
    public static void main(String[] args) {
        // Écriture de données primitives dans un fichier
        try (DataOutputStream out = new DataOutputStream(new FileOutputStream("practiceData.bin"))) {
            out.writeLong(9876543210L);
            out.writeFloat(3.14F);
            out.writeChar('A');
        } catch (IOException e) {
            e.printStackTrace();
        }

        // Lecture de données primitives depuis un fichier
        try (DataInputStream in = new DataInputStream(new FileInputStream("practiceData.bin"))) {
            long longValue = in.readLong();
            float floatValue = in.readFloat();
            char charValue = in.readChar();

            System.out.println("Long: " + longValue);
            System.out.println("Float: " + floatValue);
            System.out.println("Char: " + charValue);
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```


Bonus - Concurrence et programmation multithread


### 1. Création et gestion des threads
**Description :**
Un thread est une unité d'exécution distincte dans un programme. Java fournit plusieurs façons de créer et de gérer des threads, notamment en étendant la classe `Thread` et en implémentant l'interface `Runnable`.

**Exemples de code :**
```java
// En étendant la classe Thread
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running...");
    }
}

public class ThreadExample {
    public static void main(String[] args) {
        MyThread thread = new MyThread();
        thread.start(); // Démarre le thread
    }
}

// En implémentant l'interface Runnable
class MyRunnable implements Runnable {
    public void run() {
        System.out.println("Runnable is running...");
    }
}

public class RunnableExample {
    public static void main(String[] args) {
        Thread thread = new Thread(new MyRunnable());
        thread.start(); // Démarre le thread
    }
}
```

**Exercice de pratique :**
Créez une classe qui étend `Thread` et une classe qui implémente `Runnable`. Dans chacune, affichez un message indiquant que le thread est en cours d'exécution. Testez les deux approches dans la méthode `main`.

**Correction :**
```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running...");
    }
}

class MyRunnable implements Runnable {
    public void run() {
        System.out.println("Runnable is running...");
    }
}

public class ConcurrencyPractice {
    public static void main(String[] args) {
        // Utilisation de Thread
        MyThread thread1 = new MyThread();
        thread1.start();

        // Utilisation de Runnable
        Thread thread2 = new Thread(new MyRunnable());
        thread2.start();
    }
}
```

### 2. Synchronisation des threads
**Description :**
La synchronisation est utilisée pour contrôler l'accès des threads aux ressources partagées. Java fournit des blocs synchronisés et des méthodes synchronisées pour gérer la synchronisation.

**Exemples de code :**
```java
class Counter {
    private int count = 0;

    public synchronized void increment() {
        count++;
    }

    public int getCount() {
        return count;
    }
}

public class SynchronizationExample {
    public static void main(String[] args) throws InterruptedException {
        Counter counter = new Counter();

        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        t1.start();
        t2.start();

        t1.join();
        t2.join();

        System.out.println("Count: " + counter.getCount());
    }
}
```

**Exercice de pratique :**
Créez une classe `Counter` avec une méthode `increment` synchronisée. Créez deux threads qui appellent la méthode `increment` plusieurs fois. Affichez la valeur finale du compteur après l'exécution des threads.

**Correction :**
```java
class Counter {
    private int count = 0;

    public synchronized void increment() {
        count++;
    }

    public int getCount() {
        return count;
    }
}

public class SynchronizationPractice {
    public static void main(String[] args) throws InterruptedException {
        Counter counter = new Counter();

        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        t1.start();
        t2.start();

        t1.join();
        t2.join();

        System.out.println("Count: " + counter.getCount());
    }
}
```

### 3. Gestion avancée des threads
**Description :**
Java fournit des classes et des interfaces pour la gestion avancée des threads, telles que `ExecutorService`, `Callable`, et `Future`.

**Exemples de code :**
```java
import java.util.concurrent.*;

public class AdvancedThreadExample {
    public static void main(String[] args) throws ExecutionException, InterruptedException {
        ExecutorService executor = Executors.newFixedThreadPool(2);

        Callable<Integer> task1 = () -> {
            int sum = 0;
            for (int i = 1; i <= 10; i++) {
                sum += i;
            }
            return sum;
        };

        Callable<Integer> task2 = () -> {
            int product = 1;
            for (int i = 1; i <= 5; i++) {
                product *= i;
            }
            return product;
        };

        Future<Integer> future1 = executor.submit(task1);
        Future<Integer> future2 = executor.submit(task2);

        System.out.println("Sum: " + future1.get());
        System.out.println("Product: " + future2.get());

        executor.shutdown();
    }
}
```

**Exercice de pratique :**
Utilisez `ExecutorService` pour exécuter deux tâches `Callable` qui calculent respectivement la somme des nombres de 1 à 10 et le produit des nombres de 1 à 5. Utilisez `Future` pour obtenir et afficher les résultats.

**Correction :**
```java
import java.util.concurrent.*;

public class AdvancedThreadPractice {
    public static void main(String[] args) throws ExecutionException, InterruptedException {
        ExecutorService executor = Executors.newFixedThreadPool(2);

        Callable<Integer> task1 = () -> {
            int sum = 0;
            for (int i = 1; i <= 10; i++) {
                sum += i;
            }
            return sum;
        };

        Callable<Integer> task2 = () -> {
            int product = 1;
            for (int i = 1; i <= 5; i++) {
                product *= i;
            }
            return product;
        };

        Future<Integer> future1 = executor.submit(task1);
        Future<Integer> future2 = executor.submit(task2);

        System.out.println("Sum: " + future1.get());
        System.out.println("Product: " + future2.get());

        executor.shutdown();
    }
}
```
