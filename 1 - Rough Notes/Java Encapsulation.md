Source: https://www.datacamp.com/pt/doc/java/encapsulation

# Java Encapsulation

O encapsulamento é um princípio fundamental da programação orientada a objetos (OOP) em Java que envolve o agrupamento dos dados (variáveis) e dos métodos (funções) que operam nos dados em uma única unidade, conhecida como classe. Ele restringe o acesso direto a alguns dos componentes de um objeto e pode impedir a modificação acidental de dados.

## Objetivo do encapsulamento

- **Ocultação de dados**: O encapsulamento permite que a representação interna de um objeto fique oculta do lado de fora. Somente os detalhes necessários são expostos por meio de uma interface pública.
- **Maior flexibilidade**: Ao controlar o acesso aos campos de uma classe, você pode alterar a implementação interna sem afetar o código externo que usa a classe.
- **Melhoria da capacidade de manutenção**: O encapsulamento ajuda a manter o código, mantendo os campos privados e fornecendo métodos getter e setter públicos para modificar e visualizar os campos.

## Implementação do encapsulamento em Java

Para obter o encapsulamento em Java:

1. Declare as variáveis de classe como `private`.
2. Forneça `public` métodos getter e setter para acessar e atualizar o valor de uma variável privada.

### Exemplo 1: Encapsulamento básico

```java
public class BankAccount {
    private double balance;

    // Getter method for balance
    public double getBalance() {
        return balance;
    }

    // Setter method for balance with validation
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
}
```

[Powered By](https://www.datacamp.com/datalab) 

Neste exemplo, a classe `Student` tem campos privados `name` e `age`. Os métodos públicos getter e setter são fornecidos para acessar e modificar esses campos. O setter para `age` inclui uma verificação de validação básica.

### Exemplo 2: Encapsulamento com validação

```java
public class BankAccount {     
	private double balance;      
	
	// Getter method for balance     
	public double getBalance() {         
		return balance;     
	}      
	
	// Setter method for balance with validation     
	
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
}
```

[Powered By](https://www.datacamp.com/datalab) 

A classe `BankAccount` encapsula o campo `balance`. Ele fornece os métodos `deposit` e `withdraw` para modificar o saldo, garantindo que somente operações válidas sejam realizadas.

## Dicas e práticas recomendadas

- **Use campos privados**: Sempre declare os campos de classe como `private` para protegê-los de modificações externas.
- **Fornecer métodos de acesso**: Use os métodos getter e setter do site `public` para controlar o acesso aos campos. Isso permite a validação e a flexibilidade na alteração da implementação interna.
- **Lógica de validação**: Implemente a lógica de validação nos métodos setter para garantir que o estado do objeto permaneça consistente.
- **Classes imutáveis**: Considere a possibilidade de tornar as classes imutáveis (sem setters) se o estado do objeto não for alterado após a criação. Isso aumenta a segurança e simplifica a programação simultânea.