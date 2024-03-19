# Abstract

É uma keyword que pode ser atribuída tanto para métodos, classes e propriedades. Significa que está faltando parte da implementação e que pode ser sobrescrita. Quando usada em classes informa que a classe não pode ser instânciada e deve ser utilizada como classe base, polimorfismo.

Ao usar numa propriedade ou em um método, quer dizer que aquela propriedade/método não possuem implementação e será obrigatório a implementação deles na classe não-abstrata.

Exemplo:

```csharp
public abstract Monster
{
    public abstract int Health;
    public abstract void Attack();
}

public class OrcShaman
{
    private int health;
    public override int Health {
        get
        {
            return health;
        }
        set
        {
            health = value;
        }
    }
    public override void Attack(){
        Console.WriteLine("Firebolt!");
    }
}
```
- Classes abstratas não podem ser instanciadas
- Classes abstratas não podem conter a keyword ```sealed``` porque as duas são opostas. ```sealed``` não permite que uma classe seja herdada dela e a abstrata precisa ser herdada para ser instanciada.
- Classes que herdam da abstrata precisam implementar todos os métodos/propriedades que estão marcados como abstratos.

# Perguntas e Respostas (FAQ)

_Algumas perguntas e respostas foram tiradas do ChatGPT, outras inventadas e outras de sites que estão nas referências_

1. Qual a diferença entre abstract e virtual?

## Referências

- [abstract (C# Reference)](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/abstract)