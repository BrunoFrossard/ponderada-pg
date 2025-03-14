1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.

console.log(x);
var x = 5;
console.log(y);
let y = 10;
a) A saída será undefined seguido de erro

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log

**Resposta: a) A saída será undefined seguido de erro**

**Justificativa: no primeiro console.log, a variável x não havia sido definida, ou seja, 'undefined'. No segundo, temos um let, que só pode ser chamada dentro do seu próprio bloco, e como o console.log está tentando acessa-la antes da sua declaração, dará erro.**



2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.

function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
a) Substituir if (a || b === 0) por if (a === 0 || b === 0)

b) Substituir if (a || b === 0) por if (a === 0 && b === 0)

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)


**Resposta: a) Substituir if (a || b === 0) por if (a === 0 || b === 0)**

**Justificativa: O operador lógico || está analisando apenas se b === 0, dessa maneira dará erro. Nesse sentido, deixar explícito que se a ===b ou b=== 0 console.log(...), resolverá o problema.**



3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.

function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
a) O código imprime 1000.

b) O código imprime 200.

c) O código imprime 50.

d) O código gera um erro.

**Resposta: b) O código imprime 200.
Justificativa: O switch para de rodar com a declaração de um break. Nesse código, o primeiro break é declarado após a definição do valor 200, 'vestuário', ou seja, o valor impresso será 200.**






4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.

let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);

a) 0

b) 6

c) 18

d) 24

**Resposta: d) 24
Justificativa: Primeiro, o .map troca a array para [2,4,6,8,10]. Depois disso, o .filter descarta os número que, na nova array, são menores do que 5, assim sobrará 6,8 e 10. O reduce soma os números: 6+8+10 = 24.**



5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.

let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

c) ["banana", "abacaxi", "manga", "laranja"]

d) ["banana", "maçã", "uva", "abacaxi", "manga"]

**Resposta: c) ["banana", "abacaxi", "manga", "laranja"].**

**Justificativa: O .splice serve pra adicionar e excluir elementos da lista ao mesmo tempo, com a sintaxe [ posição, elemento deletado, qual elemento]. Assim, eliminaremos o elemento maçã, e adicionaremos abacaxi e manga após banana.**


6) 6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.

II. Em JavaScript, a herança é implementada através da palavra-chave extends.

a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.

**Resposta: a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.**

**Justificativa: A declaração de 'extends', segue a lógica de uma classe extender informações de outra, assim ela justifica a afirmativa I.**

7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.

class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.
II) O método apresentar() da classe Funcionario sobrepõe o método apresentar() da classe Pessoa, mas chama o método da classe pai usando super.
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

a) I e II são verdadeiras.

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.


**Resposta: a) I e II são verdadeiras.**
**Justificativa: Só a III está incorreta, já que o JavaScript pode sim suportar herança de classes. A I e II estão corretas, já que é declarado um extends Pessoa na classe funcionário, que faz com que essa classe herde as informações da classe Pessoa.**


8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.


Asserção: O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.
Razão: Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

b) A asserção é verdadeira e a razão é falsa.

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

**Resposta: b) A asserção é verdadeira e a razão é falsa.**

**Justificativa: Através do polimorfismo, é possível atribuir uma mesma ação para diferentes variáveis, como por exemplo: ao definir uma função som(){}, podemos chamar a função gato miar e cachorro latir, e as duas realizarem essa função.**

9) function somaArray(numeros) {
//defini soma e i como variáveis, já que o erro dado era que 'soma' não estava definido.
     var soma = 0;
   
    var i = 0;

  // usei .length, pois estamos tratando o tamanho da lista em relação à sua extensão, e não largura e altura.
    for (var i = 0; i < numeros.length; i++) {
        soma += 2 * numeros[i];
    }
    return soma;
}

console.log(somaArray([1, 2, 3, 4])



10) class Produto {
    constructor(nome, preco) {
        this.nome = nome;
        this.preco = preco;
    }

    calcularDesconto() {
        return this.preco * 0.9;
    }
}

class Livro extends Produto {
    constructor(nome, preco, autor) {
        super(nome, preco);
        this.autor = autor;
    }

    calcularDesconto() {
        return this.preco * 0.8;
    }
}

const produto = new Produto("Rayban", 300);
const livro = new Livro("A Arte da Guerra", 60);

console.log(produto.calcularDesconto()); 
console.log(livro.calcularDesconto()); 

**A herança, nesse contexto, funcioa da seguinte forma: a classe livro que criamos herda preço e produto que foram criadas na classe produto. Outra forma de alteração no método na classe Livro, seria implementar o desconto de forma direta, utilizando a variável do produto com o valor de desconto que queremos, como 0.8 com valor de 20% de desconto.




