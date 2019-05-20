# Curso de Unity
> Resumo das aulas de unity <br>
> Curso ["UNITY 5 - Aprenda C#" Marcos Schultz](https://www.youtube.com/playlist?list=PL0TaCOFAHoO-Wpq6FuN9gwr7WAdPEKUnh)

## Anotações
- Para criar um prefab basta arrastar um GameObject para a pasta assets
- Pode-se forçar uma saída de um viod usando as Ex.
```c#
GameObject obj = Instantiate(PreFab) as GameObject;
GameObject obj = (GameObject)Instantiate(PreFab); // Semelante ao PHP
// A saída da função é uma viod dessa forma eu forço uma saída GameObject...
```
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
- Todos os script tem um objeto "gameObject" que refere-se ao gameObject local 
- Os components tem um atributo chamado **enabled** que permite desabilitar o component
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
### Metodos de Atualização do canvas
- **Awake** <br>
  Executa antes do carregamento da cena
- **Start**  <br>
Executado apenas uma vez no inicio do cena, junto ao primeiro frame
- **Update**  <br>
Executado em todos os frames; Para Nomalizar usa-se Time.deltaTime
- **LateUpdate** <br>
Executado após o update
- **FixedUpdate** <br>
Executada a uma taxa fixa de 30/1s independente da taxa de frames

### Metodos de fisica
- **OnTriggerEnter**  <br>
Executado quanto entra em contato com algum colisor; <br>
Para funcionar o colizor deve estar com a opção "IsTrigger" marcada <br>
O objeto que vai colidir tem que ser Rigidbody <br>
- **OnTriggerExit** <br>
Executado quando sai do contato com o colisor
### Metodos de manipulação de eventos
- **OnMouseEnter** <br>
Executa quando o mouse entra em contato (hover) com o objeto...
- **OnMouseExit** <br>
Executa quando o mouse sai do objeto...

### Outros metodos
- **OnGUI** <br>
Criar botões na tela ????

----
## Components(class) da Unity...
- **Camera** cria uma instancia de uma camera
- **GameObject** Objeto agrupador da unity;
- **BoxCollider** Objeto que cria uma area de colisão
- **Rigidbody** Atribui comportamento fisico a um objeto
  - __isKinematic__ Se true as leis da fisica não fazem efeito...

----
## Funções
- **GetComponent** Usa-se para cunseguir uma instacia de um componente.
  - __Pega a instacia do escopo__ Ex:.
```c#
Camera cam = GetComponent<Camera>();
```
  - __Pega a instacia de GameObject__ Ex:.
```c#
GameObject.GetComponent<Rigidbody>();
```
- **Time.deltaTime** retorna um delta relativo aos frames...
- **isActiveAndEnabled** retorna true caso um componete eesteja ativado e habilitado...
- **Input.GetMouseButtonDown(int)** Observa a ação do botão do mouse..
----
## Funções do gameObject
- **gameObject.SetActive(bool)** define o status do gameObject pai...
- **gameObject.activeInHierarchy** parametro que define o status do GO
- **gameObject.activeSelf** define o status do GO baseado no __SetActive()__...
- **GameObject.CreatePrimitive(PrimitiveType)** Cria um objeto em GameObject..
  - __PrimitiveType.Cube__ Cria um objeto primitivo do tipo CUBO...
- **Instantiate(GameObject, [ Vector3 position, Quaternion rotation ])** Cria uma instacia de um objeto na scene....
- **GameObject.AddComponent( typeof(Componente) )** Adiciona um Componente a uma instacia de GameObject.. Ex:.
```c#
GameObject.AddComponent( typeof(Rigidbody) );
```