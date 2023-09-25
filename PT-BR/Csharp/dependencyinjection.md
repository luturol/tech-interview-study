# Dependency Injection WIP

O .NET possui alguns jeitos de fazer a injeção de dependência que são utilizadas para chegar no IoC (Inversion of Control). Uma dependência é um objeto que depende de outro objeto para funcionar.

Tipos de injeção

- Scoped
- Transient
- Singleton

## Scoped

É criado uma vez por client request (conexão) e é deletada quando termina a conexão.

Exemplo: DbContext e conexão com o banco de dados

## Transient

É criado sempre que é requisitado para o service container e deletada no final. Muito útil para lightweight e stateless services.
Exemplo:

## Singleton

## Referências

- [Dependency injection in .NET](https://learn.microsoft.com/en-us/dotnet/core/extensions/dependency-injection)
- [Architectural principles](https://learn.microsoft.com/en-us/dotnet/architecture/modern-web-apps-azure/architectural-principles#dependency-inversion)
- [AddTransient, AddScoped and AddSingleton Services Differences](https://stackoverflow.com/questions/38138100/addtransient-addscoped-and-addsingleton-services-differences)
