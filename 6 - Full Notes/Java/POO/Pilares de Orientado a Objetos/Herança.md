2025-03-19

Status: 

Tags: [[Orientação a Objetos - POO]] | 

---

# _**Introdução**_

### Definição

A Herança em Java permite que os atributos e métodos de uma classe sejam baseados / herdados de uma classe "modelo" (classe pai) mais chamada de **Superclasse**, a classe que herda esses atributos e métodos (classe filho) é chamada de **Subclasse**, aonde podemos reescrever os métodos herdados e adicionar atributos e métodos específicos dessa classe. 

### Explicação DIO

Características e comportamentos comuns podem ser elevados e compartilhados através de uma hierarquia de objetos.
**Exemplo:** Um Cachorro e um Gato possuem propriedades e métodos equivalente mas cada um tem suas características próprias e diferentes um de outro. Mas podemos concordar que os dois são Animais (uma classe **Animal é criada**) nela as propriedade e métodos em comum aos dois animais são colocadas. As duas classes **Cachorro** e **Gato** (Subclasses) Herdam da classe **Animal**(Superclasse). 

## Exemplo
### Superclasse: Veículo
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

### Subclasse: Carro
```java
public class Carro extends Veiculo {
	private int numeroPortas;

	public Carro(String marca, String modelo, int ano, int numeroPortas) {
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

### Subclasse: Moto
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


_Navegando pela Hierarquia_:
No exemplo acima, a classe "Veiculo" é a superclasse que contém os atributos e métodos comuns a todos os veículos. As subclasses "Carro" e "Moto" herdam essas características e adicionam atributos específicos e comportamentos de exibição personalizados.

A herança em Java é uma técnica poderosa para criar hierarquias de classes que compartilham características comuns, permitindo a reutilização eficiente de código e a modelagem precisa de objetos do mundo real. Com a herança, é possível criar sistemas mais estruturados, flexíveis e fáceis de manter.

---
# Referências
[[Orientação a Objetos - POO]]