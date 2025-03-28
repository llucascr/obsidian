
Source: https://www.linkedin.com/pulse/encapsulamento-em-java-como-manter-integridade-dos-plaster-moreira/?originalSubdomain=pt

O encapsulamento é um dos princípios fundamentais da programação orientada a objetos em Java. Ele se refere à ideia de que cada objeto deve manter a integridade de seus dados, garantindo que estes sejam acessados apenas por meio de métodos específicos da classe. Dessa forma, é possível manter o código mais organizado, seguro e fácil de manter.

### **O que é encapsulamento?**

Em Java, encapsulamento é a prática de esconder os detalhes de implementação de uma classe, e expor apenas uma interface pública para interagir com ela. Isso significa que os atributos de uma classe devem ser privados e o acesso a eles deve ser feito somente por meio de métodos públicos.

Por exemplo, considere a seguinte classe em Java:

![[Pasted image 20250325201524.png]]

Nesse exemplo, os atributos "nome" e "idade" são privados, o que significa que eles não podem ser acessados diretamente por outras classes. Em vez disso, a classe Pessoa oferece métodos públicos de acesso ("getNome()" e "getIdade()") e métodos públicos de alteração ("setNome()" e "setIdade()") para manipular esses atributos.

Isso garante que outras classes não possam alterar diretamente os dados da classe Pessoa sem passar pelos métodos de acesso e alteração definidos na própria classe. Isso ajuda a manter a integridade dos objetos e a prevenir erros de programação.

### **Vantagens do encapsulamento**

O encapsulamento traz diversas vantagens para o desenvolvimento de software em Java. Algumas das principais vantagens são:

- **Maior segurança:** ao esconder a implementação interna da classe, o encapsulamento torna mais difícil que outros desenvolvedores cometam erros ao manipular os dados da classe.
- **Maior organização do código:** com o encapsulamento, os atributos e métodos de uma classe ficam organizados em uma interface pública bem definida, facilitando a compreensão e manutenção do código.
- **Maior flexibilidade:** o encapsulamento torna mais fácil fazer mudanças na implementação interna de uma classe sem afetar o restante do código que a utiliza.

### **Exemplo de encapsulamento em Java**

A seguir, apresentamos um exemplo de encapsulamento em Java:
![[Pasted image 20250325202142.png]]

Nesse exemplo, a classe ContaBancaria encapsula os dados de uma conta bancária. Ela possui dois atributos privados ("numero" e "saldo") e métodos públicos de acesso ("getNumero()" e "getSaldo()") e de alteração ("depositar()" e "sacar()") para manipular esses atributos.

Note que o método "sacar()" verifica se o valor solicitado é maior do que o saldo disponível na conta. Se isso ocorrer, o método lança uma exceção para sinalizar o erro. Isso é um exemplo de como o encapsulamento pode ser usado para manter a integridade dos objetos e prevenir erros de programação.

### Encapsula uma lista de contas bancárias

Nesse exemplo, a classe Banco encapsula uma lista de contas bancárias, com métodos públicos para adicionar e remover contas, e para consultar o saldo total de todas as contas. A classe interna ContaBancaria representa uma conta bancária individual, com atributos privados para o nome do titular e o saldo da conta, e métodos públicos para depositar e sacar dinheiro.

Note que a classe interna ContaBancaria é declarada dentro da classe Banco, o que permite que a classe Banco acesse diretamente seus atributos e métodos privados, mas impede que outras classes acessem esses atributos e métodos sem passar pela classe Banco. Isso é um exemplo de encapsulamento de nível mais avançado, em que uma classe encapsula outra classe.
![[Pasted image 20250325202157.png]]

Esse exemplo mostra como o encapsulamento pode ser aplicado a situações mais complexas, envolvendo várias classes e relacionamentos entre elas. Além disso, o exemplo também ilustra o uso de exceções para lidar com situações de erro durante a execução do código.

### **Conclusão**

O encapsulamento é um dos princípios fundamentais da programação orientada a objetos em Java. Ele é usado para manter a integridade dos objetos, garantindo que seus dados sejam acessados e manipulados apenas por meio de métodos específicos da classe.

Ao seguir as práticas de encapsulamento em Java, é possível escrever códigos mais seguros, organizados e flexíveis. A adoção dessas práticas é especialmente importante em projetos de grande porte ou em equipes com múltiplos desenvolvedores.

Espero que este artigo tenha sido útil para entender melhor o encapsulamento em Java. Lembre-se de que sempre é possível melhorar a qualidade do seu código, e seguir os princípios da orientação a objetos é um passo importante nessa direção.
