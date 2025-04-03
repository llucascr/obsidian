
2025-03-27 

Status:

Tags: [[Orientação a Objetos - POO]]

---

# Enredo

Uma interface assemelha-se a um contrato, através dela podemos definir métodos que as classes que implementam esta interface serão obrigados a implementar.

Resolve o problema de herança múltipla em Java, pois enquanto a herança via extends aceita apenas uma classe, é possível fazer a implementação de mais de uma interface em minha classe.

## 1. O que é uma Interface em Java?

- Uma interface é um contrato que define um conjunto de métodos sem implementação.
    
- Classes que implementam uma interface são obrigadas a fornecer a implementação dos métodos declarados.

```java
public interface Veiculo {
    void acelerar();
    void frear();
}

public class Carro implements Veiculo {
    @Override
    public void acelerar() {
        System.out.println("Carro acelerando");
    }

    @Override
    public void frear() {
        System.out.println("Carro freando");
    }
}
```

## 2. Características das Interfaces

- Todos os métodos são públicos e abstratos por padrão (desde o Java 8, métodos default e static podem ter corpo).
    
- As variáveis são públicas, estáticas e finais por padrão.
    
- Não podem ter construtores (não podem ser instanciadas).

## 3. Interfaces x Classes Abstratas

|Aspecto|Interface|Classe Abstrata|
|---|---|---|
|Herança Múltipla|Suporta (implementação de múltiplas interfaces)|Não suporta|
|Métodos Com Corpo|Apenas métodos default e static (Java 8+)|Métodos concretos permitidos|
|Modificadores de Acesso|Sempre públicos e abstratos|Métodos e atributos podem ter qualquer visibilidade|
## Diferença entre Classe Abstrata x Interface
[[Diferença entre Classe Abstrata x Interface]]

A Classe abstrata está relacionada a contratos que precisam ser definidos, como por exemplo classe Carro, Moto. Interface é a capacidade de um mesmo objeto ter propriedades e papeis diferentes em uma aplicação

## 4. Polimorfismo e Herança Múltipla

- Uma classe pode implementar várias interfaces ao mesmo tempo, permitindo herança múltipla.

```java
public interface Eletronico {
    void ligar();
}

public interface Conectavel {
    void conectar();
}

public class Smartphone implements Eletronico, Conectavel {
    @Override
    public void ligar() {
        System.out.println("Smartphone ligado");
    }

    @Override
    public void conectar() {
        System.out.println("Smartphone conectado");
    }
}
```

## 5. Métodos Default e Static (Java 8+)

- Métodos default: Permitem fornecer uma implementação padrão para métodos.
    
- Métodos static: Pertencem à interface e não à instância.

```java
public interface Calculadora {
    int somar(int a, int b);

    default int subtrair(int a, int b) {
        return a - b;
    }

    static int multiplicar(int a, int b) {
        return a * b;
    }
}
```

---
# Referências
[[Orientação a Objetos - POO]]