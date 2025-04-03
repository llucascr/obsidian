2025-03-27

Status: #Todo

Tags: [[Diferença entre Classe Abstrata x Interface]]

---

### ✅ **Classe Abstrata:**

- Serve como um **modelo parcial** para outras classes, permitindo definir **métodos concretos (implementados)** e **métodos abstratos (sem implementação)**.
	
- Utilizada quando há um **relacionamento forte** entre as classes (exemplo: "um cachorro é um animal").
	
- Permite herança simples, ou seja, uma classe só pode herdar de uma única classe abstrata.
	
- Pode ter atributos, construtores e métodos normais.
    
- Exemplo prático: Uma classe abstrata "Animal" pode ter um método concreto "respirar" e um método abstrato "emitirSom".

```java
public abstract class Animal {
    void respirar() {
        System.out.println("Respirando...");
    }

    abstract void emitirSom();
}

public class Cachorro extends Animal {
    void emitirSom() {
        System.out.println("Latindo...");
    }
}

```

### ✅ **Interface:**

- Define um **contrato totalmente abstrato**, ou seja, só contém **assinaturas de métodos** (a implementação é feita pelas classes que a utilizam).
    
- Usada para garantir que **objetos diferentes tenham comportamentos comuns**, sem herança múltipla.
    
- Uma classe pode implementar **múltiplas interfaces**.
    
- Não pode ter atributos nem construtores, apenas constantes (valores fixos).
    
- Exemplo prático: Uma interface "Som" pode garantir que qualquer classe que a implemente tenha o método "emitirSom".
    

```java
interface Som {
    void emitirSom();
}

class Cachorro implements Som {
    public void emitirSom() {
        System.out.println("Latindo...");
    }
}

class Gato implements Som {
    public void emitirSom() {
        System.out.println("Miando...");
    }
}

```

### 💡 **Resumindo:**

- **Classe Abstrata** é ideal para reutilização de código e compartilhamento de comportamentos entre classes relacionadas.
    
- **Interface** é ideal para garantir um comportamento comum entre classes não relacionadas.



---
# Referências
[[Diferença entre Classe Abstrata x Interface]]