
Status: #Todo
### Resumão

O **Abstract Factory** é um padrão de projeto criacional que fornece uma interface para criar famílias de objetos relacionados sem especificar suas classes concretas. Ele usa o polimorfismo para garantir que o código cliente possa trabalhar com objetos sem conhecer suas classes específicas, tornando o sistema mais flexível e escalável.

**Como funciona o Abstract Factory:**

1. **Fábrica Abstrata (Interface ou Classe Abstrata):** Define os métodos para criar objetos abstratos.
    
2. **Fábricas Concretas:** Implementam a fábrica abstrata, criando instâncias específicas dos objetos.
    
3. **Produtos Abstratos:** Interfaces ou classes abstratas que definem a estrutura dos objetos a serem criados.
    
4. **Produtos Concretos:** Implementam os produtos abstratos, fornecendo as versões específicas.
    

👉 **Exemplo Resumido:**  
Imagine um sistema que cria componentes gráficos diferentes para Windows e Linux:

- `GUIFactory` é a interface que define o método `createMenu()`.
    
- `WinFactory` e `LinuxFactory` são fábricas concretas que implementam `createMenu()` e retornam objetos específicos (`WinMenu` ou `LinuxMenu`).
    
- `Menu` é a interface abstrata para os menus.
    
- `WinMenu` e `LinuxMenu` são produtos concretos que implementam `Menu`.
    

**Uso do Polimorfismo:**  
Ao chamar `createMenu()` através de `GUIFactory`, o código não precisa saber se a implementação é de Windows ou Linux. O polimorfismo garante que o método certo seja executado dependendo da fábrica concreta utilizada.

### **Refatorações e Polimorfismo**

A **Refatoração** visa melhorar o código sem alterar seu comportamento funcional. Ela torna o código mais limpo, legível e fácil de manter.

#### **Substituir Comando Condicional por Polimorfismo**

Essa refatoração resolve problemas onde comandos condicionais (como `switch` ou `if-else`) verificam o tipo de um objeto para executar ações específicas. Esse tipo de código é difícil de manter, especialmente quando novos tipos são adicionados.

👉 **Antes da Refatoração (Código Condicional):**  
Imagine uma classe `TipoEmpregado` que usa um `switch` para calcular o salário:

```java
public class TipoEmpregado {     
	public int quantiaAPagar() {         
		switch(lerTipo()) {             
			case TipoDeEmpregado.ENGENHEIRO:                 
				return _salarioMensal;             
			case TipoDeEmpregado.VENDEDOR:                 
				return _salarioMensal + _comissao;             
			case TipoDeEmpregado.GERENTE:                 
				return _salarioMensal + _bonus;             
			default:                 
				throw new RuntimeException("Tipo inválido");         
		}     
	} 
}
```

➡️ **Problema:** Toda vez que um novo tipo de empregado é adicionado, é preciso modificar o método, o que viola o princípio de aberto/fechado (OCP).

👉 **Depois da Refatoração (Usando Polimorfismo):**  
A refatoração cria subclasses específicas que sobrescrevem o método para cada tipo de empregado:

```java
public class Empregado {     
	private TipoDeEmpregado _tipo;          
	
	public int quantiaAPagar() {         
		return _tipo.quantiaAPagar(this);     
	} 
}  

public abstract class TipoDeEmpregado {     
	abstract int quantiaAPagar(Empregado emp); 
	
}  

public class Engenheiro extends TipoDeEmpregado {     
	public int quantiaAPagar(Empregado emp) {         
		return emp.lerSalarioMensal();     
	}
}  

public class Vendedor extends TipoDeEmpregado {     
	int quantiaAPagar(Empregado emp) {         
		return emp.lerSalarioMensal() + emp.lerComissao();     
	} 
}  

public class Gerente extends TipoDeEmpregado {     
	int quantiaAPagar(Empregado emp) {         
		return emp.lerSalarioMensal() + emp.lerBonus();     
	} 
}
```

✅ **Vantagens da Refatoração com Polimorfismo:**

- Evita o uso de condicionais explícitos.
    
- Facilita a adição de novos tipos sem modificar a classe principal.
    
- Reduz o acoplamento e melhora a coesão.
    
- Segue o Princípio Aberto/Fechado (OCP) - Classes devem estar abertas para extensão e fechadas para modificação.