# Virtual

É uma keyword que indica que o método ou propriedade pode ser override numa classe derivada. Métodos/Propriedades podem conter implementação prévia.

```csharp
public class Monster
{
    public virtual void Growl()
    {
        Console.WriteLine("Raaaw!!");
    }
}

public class Orc : Monster
{
    public override void Growl()
    {
        Console.WriteLine("ROOOOOOOW!");
    }
}
```

Também é possível chamar a implementação da classe base utilizando a keyword ```base```.

```csharp
public class Monster
{
    public int health = 10;

    public virtual void TakeHit(int damage)
    {
        health -= damage;
    }

    public void Die()
    {
        //do something
    }
}

public class Orc : Monster
{
    public override void TakeHit(int damage)
    {
        base.TakeHit(damage);

        if(health <= 0) Die();
    }    
}
```

# Perguntas e Respostas (FAQ)

_Algumas perguntas e respostas foram tiradas do ChatGPT, outras inventadas e outras de sites que estão nas referências_


## Referências

- [virtual (C# Reference)](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/virtual)