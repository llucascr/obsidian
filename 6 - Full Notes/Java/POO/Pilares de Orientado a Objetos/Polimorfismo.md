2025-03-24

Status:

Tags: [[Orientação a Objetos - POO]]

---

# Enredo

Polimorfismo significa "muitas formas" e ocorre quando temos muitas classes relacionadas entre si por herança.

Como especificamos no capítulo anterior; **Herança** nos permite herdar atributos e métodos de outra classe. **Polimorfismo** usa esses métodos para executar tarefas diferentes. Isso nos permite executar uma única ação de maneiras diferentes.


```java
public class Animal {
	public void animalSound() {
		System.out.println("The animal makes a sound");
	}
}

public class Pig extends Animal {
	@Override
	public void animalSound() {
		System.out.println("The pig says: Oik Oik");
	}
}

public class Dog extends Animal {
	@Override
	public void animalSound() {
		System.out.println("The dog says: Au Au");
	}
}

class Main {
  public static void main(String[] args) {
    Animal myAnimal = new Animal();  // Create a Animal object
    Animal myPig = new Pig();  // Create a Pig object
    Animal myDog = new Dog();  // Create a Dog object
    myAnimal.animalSound();
    myPig.animalSound();
    myDog.animalSound();
  }
}

```


# Introdução

Polimorfismo significa "muitas formas", é o termo definido em linguagens orientadas a objeto, como por exemplo Java, C# e C++, que permite ao desenvolvedor usar o mesmo elemento de formas diferentes. Polimorfismo denota uma situação na qual um objeto pode se comportar de maneiras diferentes ao receber uma mensagem. No Polimorfismo temos dois tipos:

- **Polimorfismo Estático ou Sobrecarga**

<span style="background:#fff88f">O Polimorfismo Estático se dá quando temos a mesma operação implementada várias vezes na mesma classe</span>. A escolha de qual operação será chamada depende da assinatura dos métodos sobrecarregados.

- Polimorfismo Dinâmico ou Sobreposição

<span style="background:#fff88f">O Polimorfismo Dinâmico acontece na herança, quando a subclasse sobrepõe o método original.</span> Agora o método escolhido se dá em tempo de execução e não mais em tempo de compilação. A escolha de qual método será chamado depende do tipo do objeto que recebe a mensagem.

Existem dois tipos principais de polimorfismo:

1. **Polimorfismo de Inclusão (Sobrescrita de Métodos):**  
    Ocorre quando uma classe filha redefine um método herdado de sua classe pai usando a mesma assinatura (mesmo nome, parâmetros e tipo de retorno). Isso permite que a subclasse forneça uma implementação específica para o método, enquanto objetos da superclasse e subclasse podem ser tratados de maneira uniforme.
    
    - Exemplo: Uma classe `Forma` possui um método `calculaArea()`. As subclasses `Triangulo` e `Circulo` sobrescrevem este método para calcular suas áreas específicas.
        
    - Resultado: Ao chamar `calculaArea()` em um objeto `Forma`, o método correto é executado automaticamente com base no tipo real do objeto (ex: Triangulo ou Circulo).
        
2. **Polimorfismo de Sobrecarga (Sobrecarga de Métodos):**  
    Permite que uma classe tenha vários métodos com o mesmo nome, desde que suas assinaturas sejam diferentes (quantidade ou tipos de parâmetros variam). A decisão de qual método usar é feita em tempo de compilação.
    
    - Exemplo: Um método `soma` pode ter várias versões:
        
        - `soma(int a, int b)`
            
        - `soma(double a, double b)`
            
        - `soma(int a, int b, int c)`
            
    - Resultado: Ao chamar `soma`, o compilador escolhe a versão correta com base nos parâmetros passados.

Em resumo, o polimorfismo é uma técnica poderosa que reduz acoplamento, melhora a manutenção e aumenta a flexibilidade, sendo essencial para projetos orientados a objetos bem estruturados.

---
# Referências
[[Orientação a Objetos - POO]]