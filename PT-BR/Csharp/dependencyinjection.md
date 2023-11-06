# Dependency Injection WIP

O .NET possui alguns jeitos de fazer a injeção de dependência que são utilizadas para chegar no IoC (Inversion of Control). Uma dependência é um objeto que depende de outro objeto para funcionar.

Tipos de injeção

- Scoped
- Transient
- Singleton

## Scoped

É criado uma vez por escopo e é deletado somente quando termina as operações. Boa opção para quando temos que manter o estado de uma requisição.

## Transient

É criado sempre que é requisitado para o service container e deletada no final. Sempre será diferente toda vez que é criado. Muito útil para lightweight e stateless services. Ponto negativo, consome mais memória pelo motivo de ser instanciado toda vez e pode ter um impacto negativo no serviço.

## Singleton

Os objetos são os mesmos para todos os objetos e requisições. Cuidado que com o tempo eles podem sobrecarregar a memória.

## Instance

## Factory


# Perguntas e Respostas (FAQ)

_Algumas perguntas e respostas foram tiradas do ChatGPT, outras inventadas e outras de sites que estão nas referências_

1. **O que é injeção de dependência?**

    É um principio de software design utilizado para facilitar a manutenção em garantir que as classes em suas instâncias terão todas as dependências necessárias atribuidas antes do seu uso. Facilita nos testes e flexibilidade do código.

1. **Quais são os mais comuns tipos de injeção de dependência no .NET?**

    Os tipos mais comuns são Transient, Scoped, Singleton, Factory e Instance.

1. **Qual a diferença entre Transient, Scoped e Singleton?**

    Transient é instanciado toda a vez que é necessitado, Scoped dura toda a requisição HTTP e o Singleton é criado uma única vez e essa instância é compartilhada com os outros serviços.

1. **Quando você usaria Singleton em vez de Transient?**

    O Singleton é para ser utilizado em serviços que precisam ser compartilhados por todo o App, muito utilizado para serviços como Banco de dados e Cache. O Transient para classes que não são necessárias além do momento do uso delas, que não guardam estados e que podem ser recriadas a qualquer momento.

1. **O que é o ciclo de vida do Scoped?**

    O Scope é o ciclo de vida que vai ser mantido por toda a requisição HTTP e será compartilhado quando necessário durante a requisição. Quando a solicitação termina, ele é descartado.

1. **O que é serviço Factory e quando você o usaria?**

    O Factory é utilizado quando a instância precisa de mais configurações que serão adicionadas em tempo de execução do Aplicativo. Funciona da mesma forma que o Transient. É útil para instâncias mais complicadas que precisam de mais configurações.

1. **O que significa que um serviço tem o ciclo de vida "Instance"?**

    É um serviço em que a instância não será gerenciada pelo serviço de injeção de dependência.

1. **Quais são os benefícios da injeção de dependência e do uso de tipos de ciclo de vida apropriados?**

    O uso de injeção de dependência facilita a criação dos compenentes e garantem que o componente sempre terá tudo que precisa para funciona no momento de sua inicialização. Usar corretamente os tipos de injeção de dependência auxilia no controle de memória e também no controle de dados que são utilizados pelo sistema. Usando incorretamente pode acarretar em problemas de memória, performance e dados compartilhados incorretamente.


## Referências

- [Dependency injection in .NET](https://learn.microsoft.com/en-us/dotnet/core/extensions/dependency-injection)
- [Architectural principles](https://learn.microsoft.com/en-us/dotnet/architecture/modern-web-apps-azure/architectural-principles#dependency-inversion)
- [AddTransient, AddScoped and AddSingleton Services Differences](https://stackoverflow.com/questions/38138100/addtransient-addscoped-and-addsingleton-services-differences)
- [Tutorial: Use dependency injection in .NET](https://learn.microsoft.com/en-us/dotnet/core/extensions/dependency-injection-usage)
