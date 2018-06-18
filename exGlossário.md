# Glossário
- [Construtor](https://github.com/gherickds/Geral/blob/master/exGloss%C3%A1rio.md#construtor)
- [Instanciação](https://github.com/gherickds/Geral/blob/master/exGloss%C3%A1rio.md#instancia%C3%A7%C3%A3o)
- [Palavra reservada new](https://github.com/gherickds/Geral/blob/master/exGloss%C3%A1rio.md#palavra-reservada-new)
- [Palavra reservada instanciof](https://github.com/gherickds/Geral/blob/master/exGloss%C3%A1rio.md#palavra-reservada-instanceof)
- [Encapsulamento](https://github.com/gherickds/Geral/blob/master/exGloss%C3%A1rio.md#encapsulamento)
- [Palavra reservada this](https://github.com/gherickds/Geral/blob/master/exGloss%C3%A1rio.md#palavra-reservada-this)
- [Getters/Setters](https://github.com/gherickds/Geral/blob/master/exGloss%C3%A1rio.md#getters-e-setters)
- [Palavra reservada public/private](https://github.com/gherickds/Geral/blob/master/exGloss%C3%A1rio.md#palavra-reservada-publicprivate)
- [Assinatura de método](https://github.com/gherickds/Geral/blob/master/exGloss%C3%A1rio.md#assinatura-de-m%C3%A9todo)
- [Sobrecarga de método](https://github.com/gherickds/Geral/blob/master/exGloss%C3%A1rio.md#sobrecarga-de-m%C3%A9todos)
- [Escopo de classe]()
- [Escopo de objeto]()
- [Palavra reservada final]()
- [Relacionamento de dependência]()
- [Relacinamento de Agregação]()
- [Relacionamento de Composição]()
- [Referências](https://github.com/gherickds/Geral/blob/master/exGloss%C3%A1rio.md#refer%C3%AAncias)
# Construtor
- É um método chamado apenas no momento da criação do objeto através do operador new. Deve ter o mesmo nome da classe e não possui indicação do tipo de retorno, nem mesmo void.

```javascript
public class Pokemon{
/* criação do construtor da classe Pokemon  */
public Pokemon(){
}
}

public class ChamarPokemon {
public static void main(String[] args) { 
/* Chamar construtor */
Squirtle = new Pokemon(); 
}
}
```
# Instanciação
A instanciação é um processo por meio do qual se realiza a cópia de um objeto (classe) existente. Uma classe, a qual tem a função de determinar um tipo de dado, deve ser instanciada para que possa ser utilizada. Portanto, devemos criar sua instância, a qual é definida como um objeto referente ao tipo de dado que foi definido pela classe.
```javascript
public class Pokemon{
public string nome;
public string tipo;
}

public class Pokedex{
static void Main(){

/* É feita declaração da classe e a instanciação. */

Pokemon objPokemon = new Pokemon();

/* deve ser definido o valor dos campos criados na classe Pokemon */

objPokemon.nome = "Squirtle";
objPokemon.tipo = "Água";
}
}
```
# Palavra reservada new
- É utilizada para instanciar um objeto. 
#### Exemplos podem ser vistos em Construtor e Instanciação. "new Pokemon();"

# Palavra reservada instanceof
- Determina se um objeto é a instancia de uma classe, superclasse ou interface.
```javascript
class Pokemon{
}
class Nome extends Pokemon{
}
class Squirtle extends Nome{
public static void main(string[] args) {
Squirtle s = new Squirtle();
if (s instanceof Pokemon) {
System.out.println("Squirtle é um pokémon"):
}
}
}
```
# Encapsulamento
- O propósito do encapsulamento é o de organizar os dados que sejam relacionados, agrupando-os (encapsulando-os) em objetos (classes), reduzindo as colisões de nomes de variáveis e, da mesma forma, reunindo métodos relacionados às suas propriedades. Este padrão ajuda a manter um programa mais legível e fácil de trabalhar e manter.
![Exemplo](http://arquivo.devmedia.com.br/revistas/easyjava/imagens/43/1/image007.jpg)

- Como se pode notar, estas classes encapsulam os dados relacionados a cada objeto de forma que possamos acessar cada um deles sem conflito, por estarem cada um em seu domínio. Ou seja, para saber a idade de um homem, podemos perguntar por Homem.idade e, da mesma forma, para saber a idade de um cachorro, podemos perguntar por Cachorro.idade. Os dois atributos têm o mesmo nome, mas cada um tem o seu próprio domínio.
# Palavra reservada this
- É uma variável de referência que diz respeito a instancia atual de um objeto;
```javascript
class MinhaClasse{

private int numero;

MinhaClasse(int numero){

this.numero = numero;
/* Colocando a variável this o compilador consegue identificar quem é quem */
}
}
```
# Getters e Setters
- Getters são utilizados quando se quer pegar um valor de determinada variável.
```javascript
public class FalarBomDia { 
private String fala = "Bom dia"; 
public String getFala() 
{ 
return fala; 
} 
}
```
- Setters são utilizados para setar valores em determinadas variavéis.
```javascript
public class FalarBomDia { 
private String fala = "Bom dia"; 
public void setFala(String fala) 
{ 
this.fala = fala;
/* Neste caso o valor recebido é igualado a variavel local */
} 
}
```
# Palavra reservada public/private
- Public: uma declaração com o modificador public faz com que uma classe, método ou variável possa ser acessado a partir de qualquer outra classe;
```javascript
package garagem;
public class Carro {
public String marca;
public String cor;
public Motor motor;
public void ligar()
{
this.motor.darPartida();
}
public String toString()
{
return marca + " " + cor + " " + motor.potencia;
}
}
```
- Private: uma declaração com o modificador private faz com que um método ou variável possa ser acessado somente de dentro da própria classe.
```javascript
class Circulo
{    
private float raio;
Circulo()
{
super();
setRaio( 3.0 );
}
raio = r
}
}
class Pneu extends Circulo
{
Pneu p = new Pneu();
p.raio = 10.0; /* Ocorre um erro de compilação. O Atributo raio é privado da classe Circulo */
p.setRaio(10.0); /* Correto, pois a classe Pneu está utilizando os métodos definidos na classe Circulo para fazer
                 /* acesso ao atributo privado raio 
}
```
# Assinatura de método
- Assinaturas de método são uma combinação do nome do método, tipos e ordem dos seus parâmetros.
#### Declaração:
```javascript
public void facaAlgo (int Valor, String st)
```
#### Assinatura:
```javascript
facaAlgo(int, String)
```
# Sobrecarga de métodos
- A sobrecarga de métodos consiste na possibilidade de criar o mesmo método com possibilidades de entradas diferentes. Essas entradas, caracterizadas como parâmetros, devem sempre ser de tipos diferentes, quantidades de parâmetros diferentes ou posições dos tipos diferentes.
```javascript
public class TV {
int canal;
int volume;
boolean ligada;
int tamanho;
 
void ligar() {
this.ligar(3, 25, true);
}
 
void ligar(boolean ligada) {
this.ligar(3, 25, ligada);
}
void ligar(int canal, int volume) {
this.ligar(canal, volume, true);
}

void ligar(int canal, int volume, boolean ligada) {
this.canal = canal;
this.volume = volume;
this.ligada = ligada;
}
}
```
# Referências
- https://www.devmedia.com.br/construtores-em-java/28618
- https://www.devmedia.com.br/conceitos-e-exemplos-instanciacao-estrutura-da-linguagem/18817
- https://www.devmedia.com.br/o-que-significa-cada-palavra-reservada/8320
- http://www.guj.com.br/t/quando-usar-o-instanceof/183227/3
- https://www.devmedia.com.br/encapsulamento-em-java-primeiros-passos/31177
- http://www.guj.com.br/t/a-palavra-reservada-this/51211
- https://www.vivaolinux.com.br/dica/Entendendo-os-getters-e-setters-em-Java
- https://pt.wikibooks.org/wiki/Java/Modificadores
- http://high5devs.com/2015/02/modificadores-de-acesso-em-java/
- https://pooperrotti.wikispaces.com/Assinatura+de+m%C3%A9todos
- http://www.tiexpert.net/programacao/java/sobrecarga-de-metodo.php
