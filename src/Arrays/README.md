# Arrays (07/16)

Arrays são estruturas fundamentais em JavaScript, usadas para armazenar e manipular coleções de dados de maneira eficiente. Cada elemento de um array é identificado por um índice numérico, permitindo fácil acesso, modificação e organização de dados. Em JavaScript, os arrays são extremamente versáteis, podendo conter diferentes tipos de dados, como números, strings, objetos e até outros arrays. Nesta aula, vamos explorar como criar, acessar e manipular arrays, além de aprender métodos básicos e avançados para lidar com grandes volumes de informações de forma dinâmica.

### Criação e manipulação de arrays

Os arrays são uma das estruturas de dados mais fundamentais e amplamente utilizadas em JavaScript. Um array é uma coleção ordenada de elementos, onde cada elemento é associado a um índice numérico. Diferente de muitas linguagens de programação, em JavaScript, um array pode conter diferentes tipos de dados, como números, strings, objetos, ou até mesmo outros arrays. Isso torna os arrays extremamente versáteis e úteis para armazenar e manipular grandes conjuntos de informações de maneira organizada.

Para criar um array, você pode usar colchetes [], que é a forma mais simples e comum, ou o construtor new Array(). Vamos ver um exemplo de como criar um array em JavaScript:

### Exemplo Prático:

```
let numeros = [1, 2, 3, 4, 5];

let misto = [42, “texto”, true, [1, 2, 3]];
```

No primeiro exemplo, o array numeros armazena uma lista de números inteiros. No segundo exemplo, o array misto armazena uma variedade de tipos de dados, incluindo números, strings, booleanos e até outro array. Essa flexibilidade é uma característica poderosa do JavaScript, que permite ao desenvolvedor lidar com diferentes tipos de dados em uma única estrutura.

Cada elemento em um array é acessado através de seu índice, que começa a partir de 0. Isso significa que o primeiro elemento está na posição 0, o segundo na posição 1, e assim por diante. Para acessar ou modificar um elemento, você pode utilizar a notação de colchetes. Por exemplo:

### Exemplo Prático:

```
console.log(numeros[0]); // Saída: 1

numeros[2] = 10; // Modifica o terceiro elemento

console.log(numeros); // Saída: [1, 2, 10, 4, 5]
```

Além de acessar e modificar valores, a manipulação de arrays inclui operações como adicionar, remover e alterar elementos em tempo real. É possível, por exemplo, criar arrays vazios e adicionar elementos posteriormente, ou criar arrays já preenchidos com valores iniciais. Arrays podem ser usados para modelar e representar conjuntos de dados complexos, como uma lista de usuários em um sistema ou os itens de um carrinho de compras.

> Em resumo, um array é uma estrutura que facilita o armazenamento e a manipulação de coleções de dados, permitindo operações como adição, remoção e acesso a elementos de forma muito eficiente. A capacidade de armazenar diferentes tipos de dados e manipular facilmente essas coleções torna os arrays essenciais no desenvolvimento JavaScript.

### Uso de Arrays na prática

Na prática, os arrays são fundamentais para o desenvolvimento de soluções em JavaScript. Eles permitem que grandes quantidades de dados sejam organizadas de maneira eficiente, e seu uso é comum em diversas aplicações, desde simples listas de valores até estruturas mais complexas, como armazenamento de informações de usuários ou produtos em um sistema.

Um dos principais benefícios do uso de arrays é a capacidade de armazenar dados de forma sequencial, o que facilita operações como a iteração e a busca por elementos específicos. No contexto de desenvolvimento web, arrays são frequentemente utilizados para armazenar coleções de dados dinâmicos, como entradas de formulários, listas de produtos ou respostas de APIs.

Um exemplo prático de uso de arrays é no desenvolvimento de um sistema de gerenciamento de estoque. Um array pode ser usado para armazenar os itens disponíveis em uma loja e manipular esses dados conforme o usuário adiciona ou remove produtos. Veja um exemplo de um array que armazena itens de estoque:

### Exemplo Prático:

```
let estoque = [“Camisa”, “Calça”, “Sapato”];

console.log(estoque); // [“Camisa”, “Calça”, “Sapato”]
```

> Agora, vamos supor que um novo item precisa ser adicionado ao estoque. Para isso, usamos o método push():

### Exemplo Prático:

```
estoque.push(“Cinto”);

console.log(estoque); // [“Camisa”, “Calça”, “Sapato”, “Cinto”]
```

> Se for necessário remover o último item, utilizamos o método pop():

### Exemplo Prático:

```
estoque.pop();

console.log(estoque); // [“Camisa”, “Calça”, “Sapato”]
```

Em sistemas mais complexos, os arrays são usados em conjunto com outras estruturas e métodos para realizar operações como filtragem e mapeamento. Por exemplo, você pode usar o método filter() para filtrar elementos de um array com base em uma condição específica. Suponha que você tenha um array de números e queira filtrar apenas os números maiores que 10:

### Exemplo Prático:

```
let numeros = [5, 10, 15, 20];

let maioresQueDez = numeros.filter(function(numero) {
  return numero > 10;
});

console.log(maioresQueDez); // [15, 20]
```

Essas operações são muito úteis quando se trabalha com grandes volumes de dados, permitindo a manipulação eficiente e a extração de informações relevantes sem a necessidade de iterar manualmente por cada elemento.

Em suma, o uso de arrays na prática vai muito além do armazenamento de valores simples. Eles são uma peça-chave para a manipulação de dados em JavaScript, possibilitando que desenvolvedores trabalhem de maneira eficiente com coleções de informações dinâmicas, armazenem dados de APIs, gerenciem listas e muito mais.

## Métodos básicos de Arrays

Para manipular arrays em JavaScript, a linguagem oferece uma série de métodos que facilitam a adição, remoção e modificação de elementos. Os métodos mais comuns e amplamente usados são push(), pop(), shift(), e unshift(). Cada um desses métodos tem uma função específica e é amplamente utilizado para resolver diferentes problemas ao manipular arrays.

O método push() adiciona novos elementos ao final do array, aumentando seu tamanho. Vamos ver um exemplo prático:

### Exemplo Prático:

```
let numeros = [1, 2, 3];

numeros.push(4);

console.log(numeros); // [1, 2, 3, 4]
```

Aqui, o método push() adiciona o número 4 ao final do array numeros, que agora contém quatro elementos. O push() é particularmente útil quando você precisa expandir um array com novos valores sem substituir os existentes.

> Por outro lado, o método pop() remove o último elemento de um array. Isso é útil quando você deseja “desempilhar” o último valor inserido.

### Exemplo Prático:

```
let numeros = [1, 2, 3];

numeros.pop();

console.log(numeros); // [1, 2]
```

Além do push() e pop(), o método shift() remove o primeiro elemento do array, deslocando todos os outros elementos para a esquerda:

### Exemplo Prático:

```
let frutas = [“maçã”, “banana”, “laranja”];

frutas.shift();

console.log(frutas); // [“banana”, “laranja”]
```

O método oposto de shift() é o unshift(), que adiciona novos elementos ao início do array:

### Exemplo Prático:

```
frutas.unshift(“uva”);

console.log(frutas); // [“uva”, “banana”, “laranja”]
```

Esses métodos são fundamentais no dia a dia do desenvolvimento JavaScript, pois permitem que os arrays sejam manipulados de maneira eficiente, seja adicionando novos elementos, removendo existentes, ou reorganizando os dados. Entender como e quando utilizar esses métodos é essencial para manipular dados de forma otimizada em qualquer aplicação.

### Métodos avançados de Arrays

Além dos métodos básicos, JavaScript oferece uma série de métodos avançados que permitem manipulações mais sofisticadas e dinâmicas dos dados armazenados em arrays. Entre os métodos mais poderosos estão concat(), splice(), e slice(). Estes métodos proporcionam maior flexibilidade ao trabalhar com arrays, possibilitando desde a junção de múltiplos arrays até a remoção ou substituição de elementos em posições específicas.

O método concat() é utilizado para unir dois ou mais arrays em um único array. Por exemplo:

### Exemplo Prático:

```
let numeros1 = [1, 2];

let numeros2 = [3, 4];

let numerosCombinados = numeros1.concat(numeros2);

console.log(numerosCombinados); // [1, 2, 3, 4]
```

Esse método é útil quando você deseja combinar coleções de dados sem modificar os arrays originais. Ele cria um novo array contendo todos os elementos dos arrays combinados.

> Outro método avançado é o splice(), que pode ser usado para remover, adicionar ou substituir elementos em qualquer posição do array. O splice() é extremamente poderoso porque permite alterar o conteúdo de um array de forma muito controlada:

### Exemplo Prático:

```
let frutas = [“maçã”, “banana”, “laranja”];

frutas.splice(1, 1, “uva”); // Remove “banana” e insere “uva”

console.log(frutas); // [“maçã”, “uva”, “laranja”]
```

Neste exemplo, o splice() remove um elemento (a “banana”) e insere um novo elemento (“uva”) em seu lugar. O primeiro número passado ao splice() é o índice inicial, o segundo número indica quantos elementos serão removidos, e os valores seguintes são os novos elementos a serem adicionados.

Já o método slice() cria uma cópia de uma parte de um array, sem modificar o original. Por exemplo, se você quiser criar um subarray contendo apenas uma parte de outro array, o slice() pode ser usado.

### Exemplo Prático:

```
let frutas = [“maçã”, “banana”, “laranja”, “uva”];

let subFrutas = frutas.slice(1, 3);

console.log(subFrutas); // [“banana”, “laranja”]
```

> Aqui, o slice() cria um novo array contendo os elementos da posição 1 até a posição 3 (não inclusa). Isso permite que você extraia pedaços de arrays de maneira eficiente, sem alterar o array original.

Esses métodos avançados ampliam o controle que você tem sobre os arrays em JavaScript, permitindo que você manipule dados de forma precisa e otimizada. Usar esses métodos adequadamente pode tornar o código mais eficiente e fácil de manter, especialmente ao lidar com grandes volumes de dados ou operações complexas.

## 💡 Conteúdo Bônus:

Nesse vídeo do Canal Sharpax ele explicar o que é array (matriz e vetor), de maneira rápida, didática e com exemplos para você não esquecer mais. [**``O que é ARRAY (Vetor - Matriz) - ENTENDA de uma vez por todas``**](https://youtu.be/poDFFYkp6g4)

## 👨‍💻 GitHub da Disciplina:

Você pode acessar o repositório da disciplina no GitHub a partir do seguinte link: [**``DesenvolvimentoDinamico``**](https://github.com/FaculdadeDescomplica/DesenvolvimentoDinamico)
