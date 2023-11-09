# CQRS (Command Query Responsability Segregation)

É um padrão de design arquitetônico de software em que são separadas as operações de leitura das de gravação. 

**Comando**: são operações que irão gravar ou alterar um dado. Operações POST, PUT, DELETE, PATCH normalmente são transformadas nesses comandos.

**Leitura** (Queries): são operações de consulta de dado. Normalmente realizados por operações GET.

Benefícios:

- Modelagem mais clara o que facilita e mais próximas do motivo exato daquela implementação.

- Escalabilidade: operações podem ser escaladas independente

# Perguntas e Respostas (FAQ)

_Algumas perguntas e respostas foram tiradas do ChatGPT, outras inventadas e outras de sites que estão nas referências_

1. **O que é CQRS e por que você usaria num sistema?**

    Em sistemas com domínios muito complexos o CQRS pode se enquadrar bem por separar as camadas de gravação e as de leitura permitindo que cada operaões foque exclusivamente naquela função. O CQRS acaba deixando a modelagem dos dados mais clara, facilita a escalabilidade dessas operações e a manutenção quando houver algum problema.

1. **Quais são os benefícios de escalar operações de leitura e gravação independente do contexto do CQRS?**

    Permite que operações que sejam mais custosas dependendo do aplicativo possam ser escaladas independentemente das outras operações. Isso pode acarretar em um aumento de performance do sistema.
    
1. **Como o CQRS pode ser implementado em uma aplicação prática?**

    Pode ser implementado dividindo a lógica de operações de gravação das de consulta. Separando eles em camadas distintas uma das outras, normalmente separado em serviços apenas de gravação e outro somente de consulta.

1. **Quais são os desafios de implementar o CQRS?**

    A complexidade inicial de implementação do CQRS é alta e também a manutenção necessária para deixar o sistema coeso conforme ele vai mudando.

1. **Como os comandos se diferem de consultas?**

    Comandos são utilizados para operações de gravação de dados enquanto os de consulta são apenas leitura desses mesmos dados. São separados em camadas diferentes para facilitar a manutenção e aumentar a escalabilidade do mesmo.

1. **Por que é importante separar ações de leitura das de gravação quando se faz uma arquitetura de uma API?**

    Para poder escalar as operações de leitura ou de gravação de forma independente. A vantagem do CQRS é que torna possível escalar as operações de forma independente para resolver problemas de performance no sistema sem interferir em outras operações.

1. **Quais são os casos comuns para se aplicar o CQRS?**

    Em sistemas em que uma operação é muito mais comum que a outra e que elas precisam de sua performance aumentada.

1. **Quando eu não deveria usar o CQRS?**

    Não se deve usar o CQRS quando o domínio é muito simples, orçamento é baixo e quando a equipe não está qualificada para implementar o CQRS. Segregar as aplicações em operações de Command e Query podem gerar um alto custo para a empresa e também se o domínio é muito simples não há o motivo de complicar o aplicativo.

1. **CQRS é relacionado com Event Sourcing?**

    Não são, mas são frequentemente usados em conjunto. Event Sourcing é uma forma de persistir os dados dos eventos que resultaram naquele dado de forma imutável. Em vez de registrar o resultado final, são armazenados os eventos que resultaram naquele dado. CQRS é uma forma de arquitetura de software que separa os comandos de gravação e os de leitura. Event Sourcing e CQRS normalmente são usados em conjunto por se complementarem porque o CQRS define a forma que são separadas as operações e o Event Sourcing fornece uma maneira de persistir esses eventos para resultar num dado.

1. **CQRS precisa de mais de um banco de dados?**

    Não ncessariamente. As operações podem consumir do mesmo banco de dados. O que muda é que uma ação será utilizada exclusivamente para armazenar e outra para ler o mesmo dado.


# Referências

1. [Padrão CQRS](https://learn.microsoft.com/pt-br/azure/architecture/patterns/cqrs)
1. [CQRS (Command Query Responsibility Segregation) em uma Arquitetura de Microsserviços](https://medium.com/@marcelomg21/cqrs-command-query-responsibility-segregation-em-uma-arquitetura-de-micro-servi%C3%A7os-71dcb687a8a9)
1. [CQRS – O que é? Onde aplicar?](https://www.eduardopires.net.br/2016/07/cqrs-o-que-e-onde-aplicar/)
1. [20 Command Query Responsibility Segregation Interview Questions and Answers](https://climbtheladder.com/command-query-responsibility-segregation-interview-questions/)
1. [CQRS Simplified](https://medium.com/@miked/cqrs-simplified-1e3543ea0e1)