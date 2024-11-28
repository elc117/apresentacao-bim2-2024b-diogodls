Modificador static
===

### Modificadores de acesso
Os modificadores de acesso tem o intuito de tornar as implementações mais adequadas a diversos objetivos. Temos vários exemplos de modificadores de acesso, como o final, native, static, synchronized e volatile. Além disso, eles podem ser usados em conjuntos, adquirindo assim características exclusivas além das individuais de cada modificador.

---

### Modificador static:
O modificador static faz com que os atributos sejam compartilhados entre todas as instâncias daquela clsse, com a possibilidade de ser aplicado em métodos e inicializadores.
___

## ⚙️ Exemplo em atributo

```java
class Contador {
    static int total = 0; // Atributo estático compartilhado por todas as instâncias

    void incrementar() {
        total++;
    }
}

public class Main {
    public static void main(String[] args) {
        Contador c1 = new Contador();
        Contador c2 = new Contador();

        c1.incrementar();
        c2.incrementar();

        System.out.println("Total de incrementos: " + Contador.total); // Saída: 2
    }
}
```
Outro exemplo de atributo estático também seria o valor de pi, referenciado por **java.lang.Math.PI**, usado diretamente do próprio java.

---

## Modificador static em métodos
Quando aplicado em um método, ele permite que o método seja usado sem ser criada uma instância para aquela classe, mas ele pode alterar ou retornar apenas atributos ou outros métodos que sejam **static** também.

## ⚙️ Exemplo em método

```java
class Calculadora {
    // Método estático para somar dois números
    static int somar(int a, int b) {
        return a + b;
    }
}

public class Main {
    public static void main(String[] args) {
        // Chamando o método sem instanciar a classe
        int resultado = Calculadora.somar(10, 20);
        System.out.println("Resultado da soma: " + resultado); // Saída: 30
    }
}
```
Outro exemplo de método estático é o método "Random()", da biblioteca **java.lang.Math**.

---

## Modificador static em constantes
Quando aplicado em uma constante, juntamente do modificador **final**, ele não pode mais ser iniciado pelo método construtor, apenas  diretamente na declaração do atributo ou no bloco de inicialização estático.

## ⚙️ Exemplo em constante

```java
class Configuracao {
    static final double PI = 3.14159; // Constante estática

    static double calcularCircunferencia(double raio) {
        return 2 * PI * raio;
    }
}

public class Main {
    public static void main(String[] args) {
        double circunferencia = Configuracao.calcularCircunferencia(5);
        System.out.println("Circunferência: " + circunferencia); // Saída: 31.4159
    }
}

```

## Considerações finais
No fim, o modificador static é mais usado para criar e armazenar constantes globais, como contadores e afins e gerenciar conteúdos compartilhados entre as classes.

---

### Bibliografia:

- [Modificadores de acesso](https://www.devmedia.com.br/modificadores-de-acesso-do-java/27065)
- Ferramentas de IA