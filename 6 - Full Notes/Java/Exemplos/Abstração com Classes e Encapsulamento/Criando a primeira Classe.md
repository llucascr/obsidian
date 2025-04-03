
2025-04-02

Status: #JavaDIO

Tags: [[ExemplosPOO]] |

---

# Criando a primeira Classe

## Person
```java
package Aula01_CriandoPrimeiraClasse;  
  
import java.time.OffsetDateTime;  
  
public class Person {  
  
    private final String name;  
  
    private int age;  
  
    private int lastYearAgeInc = OffsetDateTime.now().getYear();  
  
  
    public Person(String name) {  
        this.name = name;  
        this.age = 1;  
    }  
  
    public void incAge() {  
        if (this.lastYearAgeInc >= OffsetDateTime.now().getYear()) 
        return;  
  
        this.age += 1;  
    }  
  
    // metodo estatico acessado pela classe e não pela sua instancia  
    public static void test() {  
        System.out.println("Static");  
    }  
  
    // Atibutos e metodos get e set estaticos  
    private static String test;  
  
    public static String getTest() {  
        return test;  
    }  
  
    public static void setTest(String test) {  
//        this // metodos staticos nao tem acesso ao this e nem atributos que nao sao staticos  
        Person.test = test;  
    }  
    // ----------------------------------------------  
  
    public String getName() {  
        return name;  
    }  
  
    // Como declarei name como final não podemos criar um setName  
//    public void setName(String name) {  
//        this.name = name;  
//    }  
  
    public int getAge() {  
        return age;  
    }  
  
//    public void setAge(int age) {  
//        this.age = age;  
//    }  
}
```

## Main
```java
package Aula01_CriandoPrimeiraClasse;  
  
public class Main {  
  
    public static void main(String[] args) {  
        Person male = new Person("Lucas");  
//        male.name = "Lucas"; // ERRO: Encapsulamento dos atributos  
//        male.setName("Lucas");  
//        male.age = 19;  
//        male.setAge(19);  
        male.incAge();  
        Person female = new Person("Iris");  
//        female.name = "Iris";  
//        female.setName("Iris");  
//        female.age = 19;  
//        female.setAge(19);  
        female.incAge();  
  
        System.out.println(male.getName() + " " + male.getAge() + " ");  
        System.out.println(female.getName() + " " + female.getAge());  
  
        // metodo estatico acessamos pela classe e não pela sua instancia  
//        Person.test();  
    }  
}
```

---
# Referências
[[ExemplosPOO]]