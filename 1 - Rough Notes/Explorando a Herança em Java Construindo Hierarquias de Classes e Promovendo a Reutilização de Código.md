Source: https://www.dio.me/articles/explorando-a-heranca-em-java-construindo-hierarquias-de-classes-e-promovendo-a-reutilizacao-de-codigo
# **_Introdução_**

A herança é um dos conceitos fundamentais da Programação Orientada a Objetos (POO), permitindo que as classes compartilhem características e comportamentos comuns enquanto estendem ou modificam esses atributos para atender a requisitos específicos. Em Java, a herança é uma pedra angular da linguagem, possibilitando a criação de hierarquias de classes poderosas e facilitando a reutilização de código. Neste artigo, exploraremos a herança em profundidade, suas aplicações práticas e forneceremos exemplos técnicos em Java.

_Entendendo a Herança em Java:_

A herança em Java permite que uma classe seja baseada em outra classe existente, conhecida como classe base ou superclasse. A classe que herda os atributos e métodos da classe base é chamada de subclasse ou classe derivada. Isso permite que a subclasse reutilize o código da superclasse e adicione novos membros ou modifique o comportamento existente.

_Aplicação Prática da Herança:_

A herança é uma ferramenta valiosa para modelar relações hierárquicas no mundo real. Imagine um sistema de gerenciamento de uma loja de veículos, onde diferentes tipos de veículos compartilham características básicas, mas também têm características específicas. Vamos visualizar isso com um exemplo de herança:

## Superclasse: Veículo
```java
public class Veiculo {
	private String marca;
	private String modelo;
	private int ano;

	public Veiculo(String marca, String modelo, int ano) {
		this.marca = marca;
		this.modelo = modelo;
		this.ano = ano;
	}

	public void exibirDetalhes() {       
		System.out.println("Marca: " + marca);
		System.out.println("Modelo: " + modelo);
		System.out.println("Ano: " + ano);   
	}

}
```

## Subclasse: Carro
```java
public class Carro extends Veiculo {
	private int numeroPortas;

	publoc Carro(String marca, String modelo, int ano, int numeroPortas) {
		super(marca, modelo, ano);
		this.numeroPortas = numeroPortas;
	}

	@Override
	public void exibirDetalhes() {       
		super().exibirDetalhes();
		System.out.println("Número de Portas: " + numeroPortas); 
	}
	
}
```

## Subclasse: Moto
```java
public class Moto extends Veiculo {   
	private boolean temPartidaEletrica;

	public Moto(String marca, String modelo, int ano, 
	boolean temPartidaEletrica) {
		super(marca, modelo, ano);
		this.temPartidaEletrica = temPartidaEletrica
	}

	@Override
	public void exibirDetalhes() {       
		super().exibirDetalhes();
		System.out.println("Partida Elétrica: " + 
		(temPartidaEletrica ? "Sim" : "Não"));
	}
	
}
```

_Navegando pela Hierarquia:_

No exemplo acima, a classe "Veiculo" é a superclasse que contém os atributos e métodos comuns a todos os veículos. As subclasses "Carro" e "Moto" herdam essas características e adicionam atributos específicos e comportamentos de exibição personalizados.

A herança em Java é uma técnica poderosa para criar hierarquias de classes que compartilham características comuns, permitindo a reutilização eficiente de código e a modelagem precisa de objetos do mundo real. Com a herança, é possível criar sistemas mais estruturados, flexíveis e fáceis de manter. Ao entender e aplicar adequadamente a herança, você estará dominando um dos pilares da Programação Orientada a Objetos em Java. Lembre-se de que a herança deve ser usada com moderação e cuidado, a fim de evitar hierarquias excessivamente complexas ou confusas.
