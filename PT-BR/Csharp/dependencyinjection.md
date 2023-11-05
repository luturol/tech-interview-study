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

## Referências

- [Dependency injection in .NET](https://learn.microsoft.com/en-us/dotnet/core/extensions/dependency-injection)
- [Architectural principles](https://learn.microsoft.com/en-us/dotnet/architecture/modern-web-apps-azure/architectural-principles#dependency-inversion)
- [AddTransient, AddScoped and AddSingleton Services Differences](https://stackoverflow.com/questions/38138100/addtransient-addscoped-and-addsingleton-services-differences)
- [Tutorial: Use dependency injection in .NET](https://learn.microsoft.com/en-us/dotnet/core/extensions/dependency-injection-usage)
