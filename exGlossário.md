# Glossário
- Construtor
- Instanciação
- Palavra reservada new
- Palavra reservada instanciof
- Encapsulamento
- Palavra reservada this
- Getters/Setters
- Palavra reservada public/private
- Assinatura de método
- Sobrecarga de método
- Escopo de classe
- Escopo de objeto
- Palavra reservada final
- Relacionamento de dependência
- Relacinamento de Agregação
- Relacionamento de Composição
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
# Referências
- https://www.devmedia.com.br/construtores-em-java/28618
- https://www.devmedia.com.br/conceitos-e-exemplos-instanciacao-estrutura-da-linguagem/18817
- https://www.devmedia.com.br/o-que-significa-cada-palavra-reservada/8320
- http://www.guj.com.br/t/quando-usar-o-instanceof/183227/3
- https://www.devmedia.com.br/encapsulamento-em-java-primeiros-passos/31177
