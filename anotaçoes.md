Typescript | Primeiros passos - 03/02/23 

tony stark - javascript
homem de ferro - typescript 

superset - tuna o javascript
    -tipagem do js 

transpilação - tradução e compila os arquivo TS em JS 

https://www.typescriptlang.org/

Instalando typescript

global - instala na maquina
ou instala pelo npx no projeto
ai precisa instalar em cada projeto

Rodar o TS
    o node interpreta javascript
para rodar o TS:
    npx tsc nomeDoArquivo.ts 

ele cria um arquivo JS do seu arquivo

 > configurar o typescript para como ele deve se comportar, pq ele cria o arquivo js no mesmo local, podendo causar conflito.

vamos colocar para converter tudo em massa, criando um arquivo de configuracao
    npx tsc --init
cria um tsconfig.json
no site oficial tem todas as configurações possiveis que podem ser forceConsistentCasingInFileNames

outDir colocar a pasta de saida ./build
rootDir colocar a pasta de leitura ./src

quando der o comando npx tsc ele vai criar ler a pasta src, cria e manda para a pasta build ja em JS

para otimizar rodar as coisas no terminal
criar um script novo no package.json
 "start": "npx tsc && build/index.js",

 para chamar npm run nomeDoScript

## Variaveis

 tipos primitivos
 - boolean > guarda conteudo verdadeiro ou falso
 - number > guarda valor numerico
 - string > guarda texto

forma de declarar
    let nome: boolean = false ou true;
    let nome: string = "texto";
    let numero: number =30;

Variaveis especiais
- null
- undefined 

let nulo:  null = null;
let indefinido : undefined = undefined;
nao aceita nada, so nulo, o mesmo vale pro undefined.

tipos abrangentes
- any > qualquer coisa
- void > vazio

ex funcao q nao retorna nada. poderia ter uma variavel void, usado em funcoes de execucao de query 

let retorno: void 
let retornoView: any = aceita qqlr coisa, string, numero, boolean
usado quando vc nao tem um valor presivivel 
pode retornar qqlr coisa

Objeto - sem previsibilidade 
let produto: objetct = {
    name: "maria",
    cidade: "sp",
    idade: 30,
};

Objeto tipado - mais correto usar essa estrutura

type ProdutoLoja = {
    nome:string;
    preço:number;
    unidade:number;
};

let meuProduto: ProdutoLoja ={
    nome: "tenis",
    preço: 89.99,
    unidade: 10,
}

## Arrays 
formas de declarar
let dados: string [] = ["maria", "felipe"];
let dados2: Array<string>=[]

## Arrays de Multi Types

declarar um array de multitipos
| > quer dizer ou 
let infos:(string | numbber)[] = ["maria", 30]

## Tuplas
vetor de multitypes, com lugar predefinido, seguir a exata ordem

let boleto:[string, number, number] = ["agua conta", 130, 43566344];
vc segue a ordem declarada




