
Source: https://blog.rocketseat.com.br/entendendo-a-abstracao-em-poo-com-java/

---

A Programação Orientada a Objetos (POO) é um paradigma de programação que oferece uma maneira eficiente e poderosa de organizar e estruturar o código de software. Entre os princípios fundamentais da POO, a abstração desempenha um papel crucial ao permitir que os desenvolvedores se concentrem nas características essenciais de um objeto, simplificando assim a complexidade do mundo real em modelos mais gerenciáveis no código. Este artigo destina-se a iniciantes em programação, fornecendo uma explanação clara do conceito de abstração em POO, com ênfase em sua aplicação prática usando a linguagem Java.

## O Conceito de Abstração em POO

A abstração é um princípio fundamental da Programação Orientada a Objetos que envolve a identificação e a modelagem das características e comportamentos essenciais de um objeto, ignorando os detalhes irrelevantes ou secundários para o contexto em questão. Em essência, a abstração permite aos desenvolvedores criar modelos simplificados de entidades complexas do mundo real, focando apenas nos aspectos que são importantes para a aplicação sendo desenvolvida.

### Por Que a Abstração é Importante?

A abstração é importante por várias razões:

- **Simplificação:** Reduz a complexidade do desenvolvimento de software, permitindo que os desenvolvedores se concentrem nos aspectos relevantes.
- **Reusabilidade:** Promove a reusabilidade do código, uma vez que as abstrações podem ser usadas em diferentes partes de um aplicativo ou em diferentes projetos.
- **Manutenibilidade:** Facilita a manutenção do código, pois as modificações em uma abstração (como uma classe) são herdadas por todas as suas subclasses.
- **Extensibilidade:** Permite que novas funcionalidades sejam adicionadas com facilidade, estendendo as classes existentes.

## Aplicando Abstração em Java

Java, sendo uma das linguagens de programação mais populares para a implementação de conceitos de POO, fornece recursos robustos para aplicar a abstração. Vamos ilustrar isso com um exemplo prático, retomando o cenário da clínica veterinária.

### Classe Abstrata `Animal`

Em Java, uma classe abstrata é usada para definir um Template para outras classes. Ela pode conter métodos abstratos (sem corpo) que devem ser implementados pelas classes filhas.

```java
public abstract class Animal { 
	private String nome; 
	private String especie; 
	private String nomeDoDono; 
	
	// Construtor 
	public Animal(String nome, String especie, String nomeDoDono) { 
			this.nome = nome; 
			this.especie = especie; 
			this.nomeDoDono = nomeDoDono; 
	} 
	
	// Métodos abstratos 
	public abstract void mostrarInfo(); 
}
```

### Implementando Classes Concretas

A classe `Cachorro` abaixo é uma implementação específica de `Animal`, onde definimos características e comportamentos específicos de cachorros.

```java
public class Cachorro extends Animal { 

	// Implementação específica para cachorros 
	@Override public void mostrarInfo() { 
		// Detalhes de implementação 
	} 
	
}
```

### Utilizando a Abstração

Ao criar instâncias de classes concretas e utilizar seus métodos, trabalhamos apenas com os aspectos relevantes definidos na abstração, simplificando assim o desenvolvimento de software.

```java
public class Main { public static void main(String[] args) { 
		Cachorro cachorro = new Cachorro("Rex", "Labrador", "João");
		cachorro.mostrarInfo(); 
	} 
}
```

A abstração é um conceito fundamental em POO que facilita o gerenciamento da complexidade nos projetos de software, permitindo aos desenvolvedores modelar entidades do mundo real de forma simplificada e focada. Ao aprender e aplicar a abstração, especialmente em uma linguagem como Java, os iniciantes em programação podem melhorar significativamente a qualidade, a reusabilidade e a manutenibilidade de seu código.

Para aqueles que estão começando, é crucial praticar a criação de abstrações eficazes, entendendo as necessidades específicas de seus projetos e como os princípios de POO podem ajudar a atender a essas necessidades de maneira elegante e eficiente. Com o tempo e a experiência, o uso habilidoso da abstração se tornará uma segunda natureza, enriquecendo seu conjunto de habilidades de desenvolvimento de software e abrindo novas possibilidades para a solução de problemas complexos.