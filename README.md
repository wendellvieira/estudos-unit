# Curso de Unity
> Resumo das aulas de unity <br>
> Curso ["UNITY 5 - Aprenda C#" Marcos Schultz](https://www.youtube.com/playlist?list=PL0TaCOFAHoO-Wpq6FuN9gwr7WAdPEKUnh)

## Anotações
- Variaveis e metodos em c# são privite por padrão...
- O Acesso a variaveis e metodos se dá com o "." (Ponto)
- o "this" é oculto... Ex.. Ao usar **transform** equivale a usar **this.transform**
- Variaveis do mesmo tipo podem ser declaradas separadas com ","...
- Varivaveis staticas são acessadas atráves do nome da classe ponto variaval EX:
```c#
public class Script {
    public static int number;
}
Script.number;
```
----

## Tipos de váriaveis 
> O c# é tipado... aff <br>
> Variaveis publicas aparecem no inspect... <br>
> Objetos e classes podem ser usados como tipo de obj...

- **int** numeros inteiros... Ex:. 0,1,2,3...
- **float** Numeros com ponto com até 7 casas decimais terminados com "f" Ex:. 1.55f, 54.456544f...
- **double** Numero com ponto com até 16 cadas decimais
- **string** Variavel literal... Ex:. "Ola mundo", "Seja bem vindo"


----
## Metodos da class MonoBehaviour
- **Awake**  <br>
> Executa antes do carregamento da cena
- **Start**  <br>
> Executado apenas uma vez no inicio do cena, junto ao primeiro frame
- **Update**  <br>
> Executado em todos os frames; Para Nomalizar usa-se Time.deltaTime
- **FixedUpdate** <br>
> ...
- **OnTriggerEnter**  <br>
> Executado quanto entra em contato com algum colisor; <br>
> Para funcionar o colizor deve estar com a opção "IsTrigger" marcada
- **OnGUI** <br>
> Criar botões na tela ????

----
## Components(class) da Unity...
- **Camera** cria uma instancia de uma camera
- **GameObject** Objeto agrupador da unity;


----
## Funções
- **GetComponent** Usa-se para cunseguir uma instacia de um componente do na scena...???
```c#
Camera cam = GetComponent<Camera>();
```
- **Time.deltaTime** retorna um delta relativo aos frames...

----
