2025-03-25

Status:

Tags: [[Encapsulamento]]

---

# *__Introdução__*

O **Encapsulamento** refere-se à ideia de que cada Objeto deve manter a integridade de seus dados, garantindo que estes sejam acessados apenas por meio de métodos específicos da classe.

## **O que é Encapsulamento ?**

Em Java, encapsulamento é a prática de esconder os detalhes de implementação de uma classe, e expor apenas uma interface pública para interagir com ela. Isso significa que os atributos de uma classe devem ser privados e o acesso a eles deve ser feito somente por meio de métodos públicos.

Por Exemplo:
```java
public class Pessoa {
	private String nome;
	private int idade;

	public String getNome() {
		return nome;
	}

	public void setNome(String nome) {
		this.nome = nome;
	}

	public int getIdade() {
		return idade;
	}

	public void setIdade() {
		this.idade = idade;
	}
}
```

Nesse exemplo, os atributos "nome" e "idade" são privados, o que significa que eles não podem ser acessados diretamente por outras classes. Em vez disso, a classe Pessoa oferece métodos públicos de acesso ("getNome()" e "getIdade()") e métodos públicos de alteração ("setNome()" e "setIdade()") para manipular esses atributos.

### O que isso gera ?

Isso garante que outras classes não possam alterar diretamente os dados da classe Pessoa sem passar pelos métodos de acesso e alteração definidos na própria classe. Isso ajuda a manter a integridade dos objetos e a prevenir erros de programação.

## **Vantagens do encapsulamento**

- Maior segurança: dificulta erros de outros programadores 
- Maior organização do código: encapsulamento, interface publica, facilitando a compreensão e a manutenção do código.
- Maior flexibilidade: mudanças na implementação interna de uma classe sem afetar o restante do código.

---
# Referências
[[Encapsulamento]]