# Calculator Experience

Calculator Experience é um projeto de desenvolvimento front-end criado para praticar a construção de uma calculadora web utilizando **HTML5, CSS3 e JavaScript**.

O projeto utiliza **CSS Grid** para organizar a interface da calculadora e JavaScript para implementar operações matemáticas básicas e interações com o display.

## Demonstração

- **View:** https://kallebyalencar.github.io/calculator-experience/

- **Repositório:**  
https://github.com.io/kallebyalencar/calculator-experience

Acesse o repositório pelo GitHub para visualizar os arquivos do projeto e executar a aplicação localmente.

## Sobre o projeto

O Calculator Experience foi desenvolvido como um exercício prático de desenvolvimento web, utilizando uma calculadora como base para trabalhar conceitos de estruturação, estilização e interação.

A interface possui um display para exibição dos valores e botões organizados em uma grade de quatro colunas.

O projeto foi desenvolvido utilizando apenas tecnologias fundamentais de front-end, sem frameworks ou bibliotecas de JavaScript.

## Funcionalidades

A calculadora permite realizar operações matemáticas básicas através de uma interface gráfica.

Entre as funcionalidades implementadas estão:

- **Operações básicas:** `+`, `-`, `*` e `/`;
- **AC (All Clear):** limpa todo o conteúdo do display;
- **Inverter sinal (`+/-`):** alterna o valor entre positivo e negativo;
- **Decimal (`.`):** permite realizar operações com números decimais;
- **Botão igual (`=`):** calcula o resultado da operação digitada;
- **Exibição dos valores:** apresenta os números e operadores inseridos diretamente no display.

## Tecnologias utilizadas

### HTML5

Utilizado para estruturar a interface da calculadora.

A página contém:

- Display para entrada e exibição dos valores;
- Botões numéricos;
- Botões de operações;
- Botões de controle;
- Organização dos elementos da calculadora.

Exemplo da estrutura utilizada:

```html
<input class="display">

<button class="gray-button" onclick="limparTela()">AC</button>
<button class="gray-button" onclick="inverte()">+/-</button>

<button class="blue-button" onclick="adicionarCaracter('/')">/</button>
<button class="blue-button" onclick="adicionarCaracter('*')">*</button>
```

### CSS3

O CSS é responsável pela construção da interface visual e pela organização dos elementos através de **CSS Grid**.

Entre os conceitos utilizados estão:

- CSS Grid;
- `grid-template-columns`;
- `grid-template-rows`;
- Posicionamento de elementos na grade;
- Gradiente de fundo;
- Cores;
- Bordas arredondadas;
- Espaçamentos;
- Tipografia;
- Estados de interação com `:hover`;
- Organização visual dos botões.

A calculadora utiliza uma grade com quatro colunas:

```css
grid-template-columns: repeat(4, 1fr);
```

O display ocupa as quatro colunas e as duas primeiras linhas:

```css
.display {
    grid-row: 1/3;
    grid-column: 1/5;
}
```

O botão `=` também utiliza o sistema de posicionamento do CSS Grid:

```css
.equal {
    grid-row: -3/-1;
    grid-column: -2/-1;
}
```

O botão `0` ocupa duas colunas:

```css
.zero {
    grid-column: 1/3;
}
```

### JavaScript

O JavaScript é responsável pelo comportamento e pelas operações da calculadora.

As principais funções implementadas são:

#### `adicionarCaracter()`

Adiciona números e operadores ao valor atualmente exibido no display.

```javascript
function adicionarCaracter(caracter){
    const valorInput = document.querySelector('.display').value;
    
    document.querySelector('.display').value = valorInput + caracter;
}
```

#### `limparTela()`

Remove o conteúdo atual do display.

```javascript
function limparTela(){
    document.querySelector('.display').value = '';
}
```

#### `calcular()`

Obtém a expressão digitada e calcula o resultado utilizando `eval()`.

```javascript
function calcular(){
    const valorInput = document.querySelector('.display').value;

    document.querySelector('.display').value = eval(valorInput);
}
```

#### `inverte()`

Multiplica o valor atual por `-1`, permitindo alternar entre valores positivos e negativos.

```javascript
function inverte(){
    const valorInput = document.querySelector('.display').value;

    document.querySelector('.display').value = valorInput * -1;
}
```

## Organização do projeto

A estrutura do projeto é organizada da seguinte maneira:

```text
calculator-experience/
├── assets/
│   └── style/
│       ├── reset.css
│       └── style.css
│
├── index.html
├── script.js
└── README.md
```

### `index.html`

Contém a estrutura da calculadora e seus elementos de interface.

### `assets/style/reset.css`

Contém as regras utilizadas para redefinir os estilos padrão dos elementos HTML.

### `assets/style/style.css`

Contém a estilização da calculadora, incluindo cores, dimensões, botões e organização utilizando CSS Grid.

### `script.js`

Contém a lógica JavaScript responsável pelas interações e operações da calculadora.

## Como executar

O projeto é uma aplicação front-end estática e não possui dependências de backend, banco de dados ou frameworks.

### 1. Clonar o repositório

```bash
git clone https://github.com/kallebyalencar/calculator-experience.git
```

### 2. Entrar no diretório

```bash
cd calculator-experience
```

### 3. Executar

Abra o arquivo:

```text
index.html
```

em um navegador moderno.

Também é possível utilizar o **Visual Studio Code** com a extensão **Live Server** para executar o projeto através de um servidor local.

## Interface

A interface utiliza uma combinação de cores escuras com destaque em roxo para os operadores e botão de resultado.

Os botões são divididos visualmente de acordo com sua função:

- **Cinza:** comandos de controle;
- **Escuro:** números e ponto decimal;
- **Roxo:** operadores matemáticos;
- **Roxo claro:** botão de resultado.

A organização da interface é realizada utilizando CSS Grid, permitindo controlar a posição e o espaço ocupado pelos diferentes elementos.

## Processo de desenvolvimento

O projeto foi desenvolvido como uma aplicação prática para exercitar conceitos fundamentais de desenvolvimento front-end.

Durante sua construção, foram trabalhados:

1. Estruturação de uma interface com HTML5;
2. Criação de uma calculadora utilizando elementos HTML;
3. Organização de elementos utilizando CSS Grid;
4. Definição de linhas e colunas da interface;
5. Posicionamento de elementos dentro da grade;
6. Estilização de botões;
7. Criação de estados visuais com `:hover`;
8. Manipulação do DOM com JavaScript;
9. Utilização de funções JavaScript;
10. Manipulação do valor de um campo de entrada;
11. Implementação de operações matemáticas;
12. Integração entre HTML, CSS e JavaScript.

## Objetivo de aprendizado

O principal objetivo do projeto foi colocar em prática conhecimentos fundamentais de **HTML5, CSS3 e JavaScript** através da construção de uma aplicação interativa.

O projeto permitiu trabalhar especialmente a utilização de **CSS Grid para construção de interfaces** e a integração entre estrutura, estilização e lógica utilizando as três tecnologias fundamentais do desenvolvimento front-end.

## Limitações atuais

O projeto possui uma implementação simples e utiliza `eval()` para interpretar e calcular as expressões matemáticas inseridas no display.

Essa abordagem atende ao objetivo educacional do projeto, mas não representa uma implementação recomendada para aplicações maiores ou que processem entradas não confiáveis.

Além disso, o projeto possui foco em uma interface de calculadora e não conta com backend, banco de dados ou persistência de informações.

## Status

**Status atual:** concluído como projeto de estudo.

## Autor

**Kalleby Alencar**

Estudante de Análise e Desenvolvimento de Sistemas e desenvolvedor em formação, atualmente focado no desenvolvimento web e na construção de fundamentos sólidos em programação.

**GitHub:**  
https://github.com/kallebyalencar

## Licença

Este projeto foi desenvolvido para fins educacionais e de portfólio.

Os recursos de terceiros eventualmente utilizados no projeto permanecem sujeitos às respectivas licenças e direitos de seus proprietários.
