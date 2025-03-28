2025-03-26

Status:

Tags: [[Orientação a Objetos - POO]]

---

# Enredo

Abstração em Java é o conceito de ocultar detalhes de implementação e expor apenas as funcionalidades essenciais de um objeto, utilizando classes abstratas e interfaces para definir comportamentos sem especificar como eles são implementados.

# Conceito de Abstração em POO

A Abstração envolve a identificação e a modelagem das características e comportamentos essenciais de um objeto, ignorando os detalhes irrelevantes ou secundários para o contexto em questão. Em essência, a abstração permite aos desenvolvedores criar modelos simplificados de entidades complexas do mundo real, focando apenas nos aspectos que são importantes para a aplicação sendo desenvolvida.

### Por Que a Abstração é Importante?

- Simplificação
- Reusabilidade
- Manutenibilidade
- Extensibilidade

## Aplicando Abstração em Java

### Classe Abstrata `Animal`

Uma classe abstrata em Java é uma classe que não pode ser instanciada e serve como modelo para outras classes, podendo conter métodos abstratos (sem implementação) e métodos concretos (com implementação).

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
		cachorro.mostrarInfo(); // class abstract
	} 
}
```

A abstração é um conceito fundamental em POO que facilita o gerenciamento da complexidade nos projetos de software, permitindo aos desenvolvedores modelar entidades do mundo real de forma simplificada e focada. Ao aprender e aplicar a abstração, especialmente em uma linguagem como Java, os iniciantes em programação podem melhorar significativamente a qualidade, a reusabilidade e a manutenibilidade de seu código.

---
# Referências
[[Orientação a Objetos - POO]]