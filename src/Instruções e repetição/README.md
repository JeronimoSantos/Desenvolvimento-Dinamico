# Instruções e repetição (04/16)

As instruções e repetições são componentes fundamentais da lógica de programação e são amplamente utilizadas em diversas linguagens, incluindo JavaScript. As instruções são ações que o programa executa, como atribuições, cálculos ou chamadas de função, enquanto as repetições permitem que um bloco de código seja executado várias vezes, de acordo com uma condição específica. Nesta aula, exploraremos como utilizar estruturas como if-else, switch, e os principais laços de repetição, como for, while e do...while, em JavaScript. O objetivo é compreender como aplicar essas ferramentas para tornar o código mais eficiente e dinâmico.

### Definição de Instruções e Repetição

Instruções e estruturas de repetição formam a base lógica de qualquer programa de computador, e em JavaScript isso é especialmente verdadeiro. Uma instrução em programação é uma unidade básica de ação: ela define algo que o computador deve fazer. Pode ser uma declaração de variável, uma operação matemática, ou até a chamada de uma função. Tudo que o programa faz é composto de instruções.

Cada vez que escrevemos algo no código que realiza uma ação, estamos criando uma instrução. Um programa é, portanto, uma sequência de instruções.

Além de simplesmente declarar variáveis ou fazer operações únicas, muitas vezes precisamos executar uma ação várias vezes. É aí que entram as estruturas de repetição, ou laços. Laços permitem que um bloco de código seja repetido múltiplas vezes, até que uma condição específica seja atingida. Em JavaScript, temos três tipos principais de laços: for, while, e do...while.

Imagine que você deseja imprimir os números de 1 a 10 na tela. Em vez de escrever console.log(1), console.log(2) até o número 10, podemos usar um laço for para simplificar:

### Exemplo Prático:

```
for (let i = 1; i <= 10; i++) {
  console.log(i);
}
```

> Aqui, o laço for possui três partes essenciais: a inicialização (let i = 1), a condição (i <= 10), e o incremento (i++). Esse laço começa com i igual a 1, verifica se i é menor ou igual a 10, e incrementa i em 1 a cada iteração, até que a condição i <= 10 não seja mais verdadeira.

Estruturas de repetição são essenciais para realizar operações repetitivas, economizando tempo e reduzindo erros. Em um fluxograma, podemos visualizar a repetição como um ciclo: começa em um ponto inicial, verifica uma condição e, enquanto ela for verdadeira, o código será executado. Caso contrário, o laço será interrompido.

### Exemplo Prático:

```
let vidas = 3;

while (vidas > 0) {
  console.log("Jogo em andamento. Vidas restantes: " + vidas);

  vidas–;  // Decrementa o número de vidas
}
```

> Neste código, o laço while continua rodando enquanto o número de vidas for maior que 0. Quando as vidas chegam a 0, o jogo termina.

### Instruções Condicionais If-Else

Instruções condicionais são blocos de código que permitem que o programa “tome decisões”. A estrutura mais comum é o if-else, que em português pode ser lido como “se… senão”. Ele funciona avaliando uma condição: se a condição for verdadeira, um bloco de código é executado; se for falsa, outro bloco de código pode ser executado. Por exemplo, imagine que você está escrevendo um código que decide se uma pessoa pode dirigir com base em sua idade:

### Exemplo Prático:

```
let idade = 20;

if (idade >= 18) {
  console.log(“Você pode dirigir.”);
  } else {
    console.log(“Você ainda não pode dirigir.”);
  }
```

Aqui, o programa verifica se a idade é maior ou igual a 18. Se for, a mensagem “Você pode dirigir” será exibida. Caso contrário, a mensagem “Você ainda não pode dirigir” será exibida.

Instruções condicionais são muito poderosas porque permitem que o programa siga caminhos diferentes dependendo dos dados ou das condições. Quando há mais de duas opções, podemos expandir a estrutura com else if, permitindo múltiplas verificações:

### Exemplo Prático:

```
let clima = “nublado”;

if (clima === “ensolarado”) {
    console.log(“Dia perfeito para um passeio.”);
    } else if (clima === “chuvoso”) {
        console.log(“Não esqueça o guarda-chuva!”);
        } else {
            console.log(“O clima está imprevisível.”);
        }
```

Aqui, o programa avalia o valor da variável clima. Dependendo se está “ensolarado”, “chuvoso” ou outro valor, uma ação diferente será tomada. Essa flexibilidade torna as instruções condicionais fundamentais para criar programas dinâmicos e interativos.

### Instruções Condicionais Switch

A estrutura switch é usada quando temos várias condições para testar e queremos uma forma mais organizada de fazer isso. Enquanto podemos usar múltiplos if-else para tratar essas condições, o switch torna o código mais legível e fácil de manter. Ele verifica o valor de uma variável e executa diferentes blocos de código com base nesse valor. Por exemplo, imagine um sistema que exibe o dia da semana baseado em um número:

### Exemplo Prático:

```
let dia = 3;

switch (dia) {

  case 1:
    console.log(“Domingo”);
    break;

  case 2:
    console.log(“Segunda-feira”);
    break;

  case 3:
    console.log(“Terça-feira”);
    break;

  default:

    console.log(“Dia inválido”);
}
```

> Neste exemplo, o switch compara o valor da variável dia com os valores fornecidos em case. Se dia for igual a 3, o programa exibe “Terça-feira”. Caso não corresponda a nenhum case, a opção default será executada, exibindo “Dia inválido”.

O switch é especialmente útil quando temos muitas opções diferentes para testar e queremos evitar uma longa cadeia de else if.

## Laço e Repetição

Laços de repetição são blocos de código que se repetem enquanto uma condição for verdadeira. Em JavaScript, os principais laços são o for, o while e o do...while.

O laço for é usado quando sabemos o número exato de vezes que queremos executar um bloco de código. Por exemplo, para imprimir os números de 1 a 5:

### Exemplo Prático:

```
for (let i = 1; i <= 5; i++) {

  console.log(i);

}
```

O laço while é usado quando não sabemos ao certo quantas vezes algo precisa ser repetido. Ele continua executando enquanto a condição for verdadeira. Por exemplo:

### Exemplo Prático:

```
let contador = 0;

while (contador < 5) {
  console.log(contador);

  contador++;
}
```

Por fim, o laço do…while é semelhante ao while, mas ele garante que o código será executado ao menos uma vez, mesmo que a condição inicial seja falsa:

### Exemplo Prático:

```
let x = 6;

do {console.log(x);x++;} while (x < 5);
```

> Neste caso, o valor de x é 6, e mesmo que a condição x++; 5 seja falsa desde o início, o código dentro do do será executado uma vez.

## Blocos de Código e Rótulos

Blocos de código são usados para agrupar várias instruções dentro de chaves { }. Cada vez que usamos um if, for ou função, estamos criando blocos de código. Eles ajudam a organizar o código e garantir que as instruções sejam executadas juntas. Um exemplo simples de um bloco de código é:

### Exemplo Prático:

```
if (true) {
    console.log(“Isso será executado.”);
}
```

Já os rótulos são usados para identificar blocos de código de forma única. Eles permitem que você controle mais de perto o fluxo de execução, especialmente em laços de repetição complexos. Um exemplo é:

### Exemplo Prático:

```
outerLoop: for (let i = 0; i < 3; i++) {
  for (let j = 0; j < 3; j++) {

    if (i === j) {
      break outerLoop;
    }

    console.log(i: ${i}, j: ${j});}
}
```

> Aqui, o rótulo outerLoop identifica o laço externo, permitindo que o break saia do laço correto, mesmo estando dentro de um laço aninhado.

## 💡 Conteúdo Bônus:

[**``“Eloquent JavaScript”``**](https://github.com/braziljs/eloquente-javascript) é um livro altamente respeitado disponível gratuitamente online. O livro cobre fundamentos do JavaScript, incluindo capítulos específicos sobre instruções e laços de repetição, com exercícios práticos e uma abordagem teórica sólida.

## 👨‍💻 Github da Disciplina:

Você pode acessar o repositório da disciplina no GitHub a partir do seguinte link: [**``DesenvolvimentoDinamico``**](https://github.com/FaculdadeDescomplica/DesenvolvimentoDinamico)
