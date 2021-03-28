# Typing - Typewriter animation effect (Escrevendo - Efeito de animação de máquina de escrever) 

<button><a href="preview/index.html">View Example</a></button>

![HEADER-Example](header.gif)
- ##### Give me the credits, please.
- ##### [English Translation](README.md)


## O que é?

<button><a href="https://rickbarretto.github.io/my-css-hacks-and-tricks/repos/typing-effect/preview/">Ver Exemplo</a></button>

It is a mini-project to animate Header text mainly, without line of JavaScript. You can use it in your project, just pasting in your code. Read the [MIT License](../../LICENSE) to more info!


## Glosário:
+ Use o menu do topo-esquerdo à esquerda do título README-PT-PTBR.md ou os links abaixo:
----
- [Typing - Typewriter animation effect (Escrevendo - Efeito de animação de máquina de escrever)](#typing---typewriter-animation-effect-escrevendo---efeito-de-animação-de-máquina-de-escrever)
  - [O que é?](#o-que-é)
  - [Glosário:](#glosário)
  - [+ Use o menu do topo-esquerdo à esquerda do título README-PT-PTBR.md ou os links abaixo:](#-use-o-menu-do-topo-esquerdo-à-esquerda-do-título-readme-pt-ptbrmd-ou-os-links-abaixo)
  - [Porque usar isso?](#porque-usar-isso)
  - [Como usá-lo:](#como-usá-lo)
  - [Explicação](#explicação)
    - [Por trás do código](#por-trás-do-código)
    - [Como encontrar a largura do conteúdo](#como-encontrar-a-largura-do-conteúdo)
  - [Parâmetros](#parâmetros)


## Porque usar isso?

> Esse é um código pronto, preparado e sob a Lincença MIT, assim, voce não precisará se preocupar em se prender à uma licença ou direitos de cópia. **A única coisa que peço são os créditos no rodapé da página usada,** com o [link para meu github](https://github.com/RickBarretto). O código ainda vem com [parâmetros](#parâmetros) para editar sem ter mais dores de cabeça, e uma [explicação de como ele funciona](#explicação).

## Como usá-lo:
1. Use a estrutura:
   1. ```html
        <div class="typing-container">
            <h2 class="typing-line">Line 1, abcdeft</h2>
            <h2 class="typing-line">Line 2,</h2>
            <h2 class="typing-line">Line 3, hehe!</h2>
        </div>
      ```
   2. Vocçê consegue mudar essa tag de cabeçalho `<h2>` por outras e as classes também, mas você terá de mudar os seletores de css também.
2. Copie e cole o `typing.css` para a sua pasta Css do seu projeto.
3. Adicione o `<link rel="stylesheet" href="css-folder/typing.css">` no `<head>` do seu html ou `@import url(../css-folder/typing.css)` no seu arquivo css principal.
4. Remova o estilo do `body` do `typing.css`;
5. Mude o conteúdo do html, e no `:root`:
   1. Mude as cores, tamanho da fonte, cursor... (se quiser)
   2. Mude o tempo de início: `--time-to-start`
   3. Mude a largura da linha, duração e quantidade de letras, `--line<position>-range`.

> Nesse momento, você deve estar confuso quanto ao terceiro tópico dos parâmetros do :root. Mas aqui vai uma explicação:
> 
> `--line<position>-width:` é a largura do conteúdo. Veja em [Como encontrar a largura do conteúdo](#como-encontrar-a-largura-do-conteúdo)
>
> `--line<position>-range:` é o número de letras da linha.
> 
> `--line<position>-time:` é o tempo de animaçao. Recomendo que seja igual à quantidade de letras dividida por 10 em segundos. Como: `tamanho = 13, então tempo = 1.3s`
> 

## Explicação
### Por trás do código
+ A primeira linha começa depois do `--time-to-start`;
+ Assim, a animaçao de piscar "roda" junto à do `width`, de crescer;
  + A animação de crescer é feita em etapas, essas etapas são determinadas pelo `--line<position>-range`;
+ Depois disso, é eecutada a próxima linha.
+ A primeira linha deve ter uma `border-rigth`, borda direita, não transparente, diferentemente do outros, que devem ter uma cor sólida;
+ A última linha não recebe a animação `cursor-disabled`, pois deve ser infinito.
  
### Como encontrar a largura do conteúdo
1. Ponha `fit-content` no `--line<number>-width`
2. Abra no navegador o `Ferramenta de Inspeção - Dev Tools`.
   1. `Ctrl + Shift + I`, ou `Botão-Direito-Do-Mouse > Inspecionar` ou `Menu > Mais ferramentas > Ferramentas do desenvolvedor`
3. Com a ferramenta de inspeção, veja a largura:
   1. ![Inspect](inspect.png)
4. Então, cole no `--line<number>-width: fit-content;` a largura certa, mas apenas use a parte inteira adicionada a 1px.

## Parâmetros

+ --font-size: size;
+ --font-color: color;
+ --line-aproximate: size;
+ --cursor-color: color;
+ --cursor-size: size;
+ --time-to-start: time;
+ --linex-width: size;
+ --linex-range: int;
+ --linex-time: time;


