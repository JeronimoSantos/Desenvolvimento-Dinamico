# Funções em JavaScript (02/16)

As funções em JavaScript são blocos de código que permitem executar tarefas específicas de forma organizada e reutilizável. Elas desempenham um papel crucial no desenvolvimento dinâmico, permitindo que o código seja modular, legível e eficiente. Através das funções, é possível encapsular lógicas, evitando repetições desnecessárias e facilitando a manutenção. Nesta aula, vamos explorar o conceito de funções, entender sua estrutura, como utilizá-las corretamente e como elas contribuem para a modularidade do código. O objetivo é garantir que você compreenda a importância e a aplicação prática das funções em projetos.

### O que são Funções?

As funções são blocos de código independentes, projetados para realizar tarefas específicas e que podem ser reutilizados em diferentes partes de um programa. No JavaScript, funções são componentes fundamentais para a construção de um código mais organizado, modular e eficiente. Elas permitem que desenvolvedores agrupem instruções de código em uma única entidade, que pode ser chamada sempre que necessário, evitando a duplicação de código e promovendo a reutilização.

Uma função em JavaScript é declarada utilizando a palavra-chave function, seguida por um nome, uma lista de parâmetros entre parênteses e um bloco de código entre chaves. Aqui está um exemplo básico de uma função que realiza a soma de dois números:

### Exemplo Prático: 

```
function somar(a, b) {
    return a + b;
}
```

> Neste caso, a e b são parâmetros que a função espera receber, e o operador return é utilizado para devolver o resultado da soma. Sempre que chamarmos a função somar(5, 3), por exemplo, o valor retornado será 8.

As funções são extremamente úteis porque permitem a abstração de tarefas. Imagine que, ao invés de somar números manualmente em várias partes do código, você pode simplesmente chamar a função somar sempre que precisar dessa operação. Isso reduz a repetição de código e facilita a manutenção, já que qualquer alteração na forma como a soma é feita pode ser aplicada diretamente na função, afetando todas as partes do código que a utilizam.

Além disso, funções podem ou não aceitar parâmetros. Quando não há necessidade de fornecer valores específicos, os parênteses na declaração da função ainda são obrigatórios, mas podem ficar vazios, como no exemplo abaixo:

### Exemplo Prático: 

```
function exibirMensagem() {
    console.log(“Bem-vindo ao JavaScript!”);
}
```

Essa função não recebe parâmetros e simplesmente exibe uma mensagem no console. A flexibilidade que as funções oferecem permite que sejam usadas para executar tarefas simples ou muito complexas, organizando o fluxo de lógica de um programa. Por isso, o conceito de função é central em qualquer linguagem de programação, não apenas no JavaScript.

### Importância de Usar Funções

Usar funções em JavaScript não é apenas uma boa prática, mas também uma forma essencial de manter o código organizado, modular e eficiente. A importância de funções vai além de evitar repetições. Elas promovem uma série de vantagens que facilitam o desenvolvimento de aplicações escaláveis e de fácil manutenção.

Primeiramente, as funções proporcionam reutilização de código. Ao criar uma função para realizar uma tarefa específica, você pode reutilizá-la em várias partes do programa sem precisar reescrever o mesmo código. Isso não só economiza tempo, mas também minimiza a chance de erros, pois o mesmo bloco de código será usado em todas as chamadas da função.

Além disso, as funções aumentam a legibilidade do código. Dividir um programa em funções pequenas, com nomes que descrevem claramente sua função, torna o código mais fácil de entender, tanto para o desenvolvedor original quanto para outras pessoas que venham trabalhar no mesmo projeto. Considere o seguinte exemplo:

### Exemplo Prático: 

```
function calcularMedia(nota1, nota2) {
    return (nota1 + nota2) / 2;
}
```

> O nome calcularMedia já diz claramente o que a função faz. Isso facilita a leitura do código e permite que outros desenvolvedores compreendam rapidamente a lógica sem precisar examinar cada linha detalhadamente.

Outro ponto essencial é que funções permitem modularizar o código. Modularidade significa que você pode dividir um programa em pequenos blocos independentes, cada um responsável por uma tarefa específica. Essa abordagem facilita o processo de manutenção do código, pois, se algo não funcionar corretamente, você pode isolar a função responsável e corrigir o problema sem interferir em outras partes do sistema. Além disso, ao dividir um grande problema em várias funções menores, a resolução torna-se mais organizada e gerenciável.

Por fim, as funções ajudam a controlar o escopo das variáveis. Quando você define uma variável dentro de uma função, ela fica isolada naquele escopo e não interfere em outras partes do programa. Isso evita conflitos de nomes e ajuda a manter o código mais organizado e livre de erros inesperados.

### Exemplo Prático:

```
function calcularAreaRetangulo(largura, altura) {
    let area = largura * altura;
    return area;
}
```

> A variável area existe apenas dentro da função calcularAreaRetangulo. Esse isolamento ajuda a evitar interferências indesejadas no restante do código.

## Funções Regulares

As funções regulares são as formas mais tradicionais e amplamente usadas de funções em JavaScript. Elas são definidas usando a palavra-chave function, seguidas por um nome, parâmetros opcionais e um bloco de código. Esse tipo de função oferece flexibilidade tanto na forma de declarar como de utilizar.

### Exemplo Prático:

```
function multiplicar(a, b) {
    return a * b;
}

let resultado = multiplicar(4, 5);

console.log(resultado);  // Exibe 20
```

No exemplo acima, a e b são os parâmetros da função, e o operador return é usado para retornar o produto de a e b. A função pode ser chamada em qualquer parte do código, fornecendo diferentes valores para os parâmetros.

As funções regulares podem ser usadas para executar uma grande variedade de operações, desde tarefas simples, como exibir uma mensagem no console, até cálculos complexos envolvendo vários parâmetros. Elas também podem ser projetadas para não retornar nenhum valor, simplesmente executando um bloco de código quando chamadas. Por exemplo:

### Exemplo Prático:

```
function exibirAlerta() {
    alert(“Essa é uma mensagem de alerta!”);
}
```

Funções regulares são particularmente úteis quando você deseja realizar uma ação repetidamente em diferentes partes do código. Outra vantagem das funções regulares é que elas suportam elevação (ou hoisting), o que significa que podem ser chamadas antes de sua declaração no código. Isso acontece porque o JavaScript, ao processar o código, move automaticamente as declarações de funções para o topo do escopo.

### Exemplo Prático:

```
console.log(somar(2, 3));  // Funciona mesmo antes da declaração da função

function somar(a, b) {
    return a + b;
}
```

> Essa flexibilidade e suporte à elevação tornam as funções regulares uma escolha poderosa e versátil em JavaScript.

## Funções Anônimas

Funções anônimas são funções que, como o nome sugere, não têm um nome associado a elas. Em JavaScript, essas funções são geralmente atribuídas a variáveis ou passadas como argumentos para outras funções. Funções anônimas são úteis quando a função será usada em um contexto específico e não precisa ser reutilizada em outras partes do código. Aqui está um exemplo de uma função anônima atribuída a uma variável:

### Exemplo Prático:

```
let saudacao = function(nome) {
    return "Olá, " + nome + “!”;
};

console.log(saudacao(“Ana”));  // Exibe “Olá, Ana!”
```

> Nesse exemplo, a função anônima recebe um parâmetro nome e retorna uma saudação personalizada. Para chamar essa função, utilizamos a variável saudacao.

Além de serem atribuídas a variáveis, funções anônimas são amplamente usadas como callbacks – funções passadas como argumento para outras funções e que serão executadas posteriormente. Isso é muito comum em métodos como map, filter e forEach ao trabalhar com arrays. Veja o exemplo:

### Exemplo Prático:

```
let numeros = [1, 2, 3, 4];

let dobrados = numeros.map(function(numero) {
    return numero * 2;
});
```

> Nesse caso, a função anônima passada para o método map realiza a multiplicação de cada elemento do array por 2, retornando um novo array com os valores dobrados.

As funções anônimas são muito úteis em situações em que você não precisa reutilizar a função em vários lugares. Elas também permitem que o código seja mais conciso e claro em operações específicas, como a manipulação de arrays ou o tratamento de eventos. No entanto, como essas funções não têm nome, podem dificultar a depuração em casos de erro, já que a mensagem de erro não indicará diretamente qual função está causando o problema.

## Funções Arrow

As funções arrow (ou funções “seta”) são uma forma mais concisa e moderna de declarar funções, introduzida no ECMAScript 6 (ES6). Elas oferecem uma sintaxe simplificada em comparação com as funções regulares e são especialmente úteis em situações onde se deseja manter o código mais enxuto.

### A estrutura básica de uma função arrow é a seguinte:

```
let somar = (a, b) => a + b;
```

Neste exemplo, a função somar recebe dois parâmetros e retorna a soma de a e b. A principal diferença em relação a uma função regular é que, ao usar a sintaxe da seta (=>), você não precisa utilizar a palavra-chave function nem o return se o corpo da função contiver apenas uma linha.

Funções arrow também oferecem vantagens no tratamento do escopo do this. Em funções regulares, o valor de this pode mudar dependendo do contexto em que a função é chamada. Já em funções arrow, o valor de this é fixo e sempre refere-se ao contexto onde a função foi definida. Isso as torna ideais para callbacks e métodos que precisam acessar o contexto da função externa.

### Exemplo Prático:

```
let dobrar = n => n * 2;

console.log(dobrar(4));  // Exibe 8
```

> Quando há apenas um parâmetro, os parênteses ao redor dele podem ser omitidos. Além disso, funções arrow podem ser usadas como callbacks de maneira muito eficiente.

### Exemplo Prático:

```
let numeros = [1, 2, 3, 4];

let dobrados = numeros.map(n => n * 2);
```

Essas funções são amplamente utilizadas em frameworks e bibliotecas modernas, como React e Vue.js, por sua simplicidade e clareza. Apesar de serem poderosas e práticas, é importante entender o comportamento de escopo dessas funções, especialmente ao trabalhar com o this, para evitar erros em aplicações mais complexas.


## 💡 Conteúdo Bônus:

O MDN oferece uma documentação completa e gratuita sobre JavaScript, cobrindo desde o básico até tópicos avançados. A seção de funções é bastante didática e inclui exemplos práticos.

Link da documentação: [**``MDN JavaScript``**](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)

## 👨‍💻 GitHub da Disciplina:

Você pode acessar o repositório da disciplina no GitHub a partir do seguinte link: [**``DesenvolvimentoDinamico``**](https://github.com/FaculdadeDescomplica/DesenvolvimentoDinamico)
