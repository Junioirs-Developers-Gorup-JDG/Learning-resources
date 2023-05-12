# SOLID

Um conceito no meio da programação usado em aplicações de médio/grande porte para fazer-las estáveis, fáceis de manter e escalar.

## Principio 1 (Single Responsibility Principle / Principio da Responsabilidade Única)

### No contexto de funções JS

Uma função deve fazer apenas oque ela diz e se propõe a fazer.

Exemplo:

Uma função que deve somar x e y

``` JavaScript
function soma(x, y) {
  const resultado = x + y;

  console.log(`O resultado da soma de ${x} + ${y} é ${resultado}`);
}

soma(5, 8);

// Console: O resultado da soma de 5 + 8 é 13
```

O exemplo acima não esta seguindo o primeiro principio, já que a função deveria somar e nada mais.

Para que o exemplo acima siga primeiro principio devemos ao invés de fazer o console.log dentro da função, apenas retornar o resultado da soma e fora da função fazer o console.log

``` JavaScript
function soma(x, y) {
  const resultado = x + y;

  return resultado;
}

const x = 9;

const y = 2;

const resultadoDaSomaDeXEY = soma(x, y);

console.log(`O resultado da soma de ${x} + ${y} é ${resultadoDaSomaDeXEY}`);

// Console: O resultado da soma de 5 + 8 é 13
```

Imaginando que essa função esta dentro de um projeto gigante e com muitas partes desse projeto dependendo dela, quando retiramos tudo que ela não deveria fazer de dentro dela, evitamos erros e cooperamos com as futuras implementações.

Já que agora ela apenas soma os números, a parte do log ficou totalmente separada dela e então se alguém precisar que o texto mandado ao console seja diferente de "O resultado da soma de x + y é z" fica infinitamente mais simples e viável.

### Contexto de Componentes React

O mesmo se aplica a componentes React, se tivermos um componente de header, ele deve apenas ser responsável pelo layout e funcionamento básico do header, nada mais.

Exemplo:

``` JSX
function Header() {
  return (
    <main>
      <header>
        <h1>Titulo da página</h1>
  
        <h2>Subtitulo da página</h2>
      </header>
      

      <section>
        <p>Conteúdo da página</p>
      </section>  
    </main>
  )
}
```

O exemplo esta novamente errado pois o componente se diz ser um Header, então ele deveria conter apenas informações, funcionalidades e layout de um header, e não parte do conteúdo da página.

Para corrigir é simples, podemos apenas separar cada parte em seu próprio componente

``` JSX
function Header() {
  return (
    <header>
      <h1>Titulo da página</h1>

      <h2>Subtitulo da página</h2>
    </header>
  )
}

function Section() {
  return (
    <section>
      <p>Conteúdo da página</p>
    </section>  
  )
}

function Página() {
  return (
    <main>
      <Header />

      <Section />
    </main>
  )
}
```