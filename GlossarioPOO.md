## Construtor
Construtor é responsável por criar o objeto em memória, ou seja, instanciar a classe que foi definida, um mecanismo que permite fazer inicializações no objeto assim que ele é instanciado, com a palavra reservada "new" no Java.  
Exemplo de Construtor:
``` Java
class Glossario {
    public Glossario() {
        System.out.println("Aqui está o construtor");
    }
}
```
## Instanciação
A instanciação é um processo por meio do qual se realiza a cópia de um objeto (classe) existente. Uma classe, a qual tem a função de determinar um tipo de dado, deve ser instanciada para que possamos utilizá-la.  
Exemplo de Instanciação:
``` Java
public class Instanciacao {
    private Glossario glossario = new Glossario();
}
```
## Encapsulamento
Um mecanismo da linguagem de programação para restringir o acesso a alguns componentes dos objetos, escondendo os dados de uma classe e tornando-os disponíveis somente através de métodos.
## Getters/Setters
Estes métodos são seletores e modificadores dos atributos de sua classe. Consiste em os atributos de uma classe não poderem ser acessados diretamente.  
Exemplo de Encapsulamento com Getters/Setters:
``` Java
public class Encapsulamento {
    private double pontuacao;
    
    public void setPontuacao(double pontuacao) {
        this.pontuacao = pontuacao;
    }
    
    public double getPontuacao() {
        return pontuacao;
    }
}
```
## Assinatura de método
Dois métodos tem a mesma assinatura se eles tiverem o mesmo nome e tipos de parâmetro, ou seha é a junção do nome do método, e os seus parâmetros tipados.
``` Java
public class AssinaturaMetodo {
    public void metodo(String a) {
    }
    public int metodo(Int a) {
        return 0;
    }
}
```
## Sobrecarga de método
A sobrecarga de métodos (overload) é um conceito do polimorfismo que consiste basicamente em criar variações de um mesmo método, ou seja, a criação de dois ou mais métodos com nomes totalmente iguais em uma classe. A Sobrecarga permite que utilizemos o mesmo nome em mais de um método contanto que suas listas de argumentos sejam diferentes para que seja feita a separação dos mesmos.
``` Java
public class Calculadora{
    public int calcula( int a, int b){
        return a+b;
    }

    public double calcula( double a, double b){
        return a+b;
    }

    public String calcula( String a, String b){
        return a+b;
    }
}
```
## Escopo de classe
Escopo refere-se à vida e acessibilidade de uma variável. Quão grande é o alcance depende de onde uma variável é declarada. Por exemplo, se uma variável é declarada na parte superior de uma classe, ela será acessível a todos os métodos de classe. Se for declarada num método, em seguida, só pode ser utilizada em tal método.
``` Java
public class Planetas {
 
 // Variavel da classe é compartilhada por todos
 public static long numeroDePlanetas;
 
 // Variavel de intancias
 private double x, y;
 private double massa;
 public String apelido;
 
      // Construtor
  	//  x e y são  variaveis instanciadas,
  	//  mas newX and newY são variaveis locais
  	//  O construtor incrementa o valor
    public  Planetas(double novoX, double novoY, double novaMassa)
    {
       x = novoX;
       y = novoY;
 
       massa = novaMassa;
   	numeroDePlanetas++;
    }
}
```
## Escopo de objeto
Escopo do objeto é onde ele está, dentro da classe, sendo um atributo, ou dentro de um método, sendo uma variável.  
Exemplo de uso:
``` Java
public class escopoObjeto{
    private Calculadora calculadora = new Calculadora();
    // Escopo da Classe
    
    public Calculadora getCalculadora() {
        Calculadora calculadora = new Calculadora();
        //Escopo do método
        calculadora = this.calculadora;
        return calculadora;
    }
}
```
## Palavras reservadas "public/private"
O modificador public deixará visível a classe ou membro para todas as outras classes, subclasses e pacotes do projeto Java.
O modificador private deixará visível o atributo apenas para a classe em que este atributo se encontra.  
Exemplos de uso:
``` Java
public class PublicPrivate {
    public int atributoPublico;
    private int atributoPrivado;
}
```
## Palavra reservada "new"
Operador utilizado para criar um objeto, instancia de uma classe.  
Exemplo de uso:
``` Java
public class New {
    private Glossario glossario = new Glossario();
    public Instaniciacao instanciacao = new Instanciacao();
}
```
## Palavra reservada "instanceof"
Operador usado para conferir se um objeto é de um certo tipo (classe, interface, enum, anotação), considerando toda a sua hierarquia.  
Exemplo de uso:
``` Java
public class InstanceOf {
    public boolean EhInstancia(Object obj) {
        boolean eh = false;
        if (obj instanceof InstanceOf) {
            eh = true;
        } else {
            eh = false;
        }
        return eh;
    }
}
```
## Palavra reservada "this"
Utilizamos a palavra reservada "this" quando estamos trabalhando dentro de uma determinada classe e queremos fazer menção a mesma.  
Exemplo de uso:
``` Java
public class This {
   private int id;
   public int getId() {
      return id;
   }
   public void setId(int id) {
      this.id = id;
   }
}
```
## Palavra reservada "final"
É um método que não pode ser sobrescrito nas subclasses.
Usado para garantir que um determinado algoritmo não possa ser modificado pelas subclasses.  
Exemplo de uso:
``` Java
class Final {
    private int jogador;
    public final int jogador() {
        return jogador;
    }
    ...
}
```
## Associação Simples
É quando uma classe possui um atributo vindo de outra classe. Atributo da Classe.
Símbolo UML "<-------->"
## Relacionamento de dependência
Ocorre quando uma classe utiliza os serviços de outra classe. Ocorre no método da classe.
Símbolo UML "- - - - - >".
## Relacinamento de Agregação
É quando duas classes têm uma relação todo-parte, a parte consegue existir sem o todo. Atributo da Classe.
Símbolo UML "-------<>"
## Relacionamento de Composição
É quando duas classes têm uma todo-parte, a parte não consegue existir sem o todo. Atributo da Classe.
Símbolo UML "-------<//>"
