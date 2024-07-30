 [Projeto Aula 01](https://github.com/guilhermeonrails/flashcard/blob/aula_1/index.html)

## Faça como eu fiz: 
## Instalando o VS Code
Durante essa unidade utilizaremos o editor de códigos *Visual Studio Code* ou *VS Code*. Caso você precise instalá-lo em seu dispositivo, você pode acessá-lo através do link abaixo:

[VS Code](https://code.visualstudio.com/download)

Após acessar o link, faça o donwload do instalor de acordo com o sistema operacional do seu dispositivo.

Com o download terminado, clique no arquivo ```.exe``` para executar o instalador e prossiga com a instalação clicando em *next* e finalmenete em *instal*.

## Instalando o Live Preview

O *Live Preview* é uma extenção do VS Code que nos permite visualizar nosso projeto. Para instalá-la, 


## Preparando o ambiente

No decorrer da Aula 02 realizaremos a estilização da fonte utilizada em nosso projeto, e para isso, você precisará ter essa fonte instalada em seu dispositivo.

Você pode fazer o download da fonte *Bai Jamjuree* acessando o link abaixo:

[Link de download](https://fonts.google.com/specimen/Bai+Jamjuree?query=Bai+Jamjuree)

Após acessar o link, você será direcionada para a página do *Google Fonts*. Selecione a opção *Get Font* ou *Pegar Fonte*.

![A imagem exibe a interface do Google Fonts, destacando uma fonte específica chamada “Bai Jamjuree”. O nome da fonte está em destaque, com opções clicáveis como “Specimen”, “Test Drive”, “Pairings”, “About” e “License”. Além disso, há um botão vermelho com a inscrição “Get font”, sugerindo que os usuários podem adquirir essa fonte.](aula02-img01)

Na página seguinte, pressione o botão download, a direita da tela.

![Captura de tela da página do Google Fonts para "Bai Jamjuree". O destaque está no botão "Baixar tudo", indicando que os arquivos de fonte podem ser baixados.](Aula02-img2)

Após baixar a fonte, na pasta de download do seu dispositivo, clique sobre a pasta *Bai_Jamjuree*.

![Captura de tela de um explorador de arquivos mostrando dois ícones de pasta, em destaque a pasta "Bai_Jamjuree". ](Aula02-img03)

Com a pasta aberta, clique sobre o arquivo *BaiJamjuree-Regular*:

![Captura de tela de um repositório com fundo preto, contendo vários arquivos tipográficos, em destaque a fonte BaiJamjuree-Regular.](Aula02-img04)

Após abrir o arquivo, pressione o botão instalar, localizado no lado esquerdo superior da tela.

![Captura de tela de um diretório aberto, que possui aplicações de um tipode fonte. O fundo da imagem é branco e possui na parte superior um menu na cor cinza, contendo a opção Instalar destacada.](Aula02-img05)

## Aula 02

## Faça como eu fiz: Personalizando o rodapé da página

Em nossa última aula, criamos a base HTML do nosso projeto.

![A imagem mostra uma página web simples sendo exibida no navegador, acessada pelo endereço local 127.0.0.1:5500/index.html. A página contém dois blocos de texto, o primeiro possui o título “Programação” a pergunta “O que é Java Script” e a respectiva resposta. O segundo bloco, também está intitulado programação, e apresenta uma pergunta “O que é CSS” e sua respectiva resposta. Ao final apresenta o texto  "Projeto desenvolvido pela Alura, sem fins lucrativos.". A formatação é simples, com títulos em negrito e o restante do texto em formato padrão.](Aula02-img06)

Contudo, nosso resultado ainda não está de acordo com nosso protótipo. Para deixar a aparência do nosso projeto mais bonita, utilizaremos a linguagem de estilização CSS.

## Criando a pasta de estilização

Primeiro, iremos até o *Explorador* do VS Code, podemos abri-lo utilizando o atalho *Ctrl+B*. Então, criaremos uma nova pasta clicando no ícone *New Folder* ou *Nova Pasta* e a nomearemos de *assets*.

![A imagem mostra uma captura de tela de um editor de código, com um painel de explorador de arquivos à esquerda. O explorador de arquivos exibe dois itens sob o diretório “FLASHCARD”: uma pasta chamada “assets” e um arquivo chamado “index.html”. A pasta “assets” está destacada. ](Aula02-img07)

Com a pasta ```assets``` selecionada, clicaremos em *Novo Arquivo* e criaremos um arquivo chamado ```style.css``` :

![A imagem exibe uma captura de tela de um editor de código, com um painel de explorador de arquivos à esquerda. O foco está na seção do explorador de arquivos, onde a estrutura de um projeto é visível. O projeto contém uma pasta chamada “assets”, que está expandida para mostrar o arquivo “style.css”. Além disso, há outro arquivo fora da pasta “assets” chamado “index.html”.](img8)

Depois disso, voltaremos ao index.html e dentro de ```head```, e uma linha antes de ```title```, vamos digitar ```link:css```. No código gerado, para que o arquivo CSS seja acessado na pasta ```assets```, iremos adicionar antes do link do arquivo *assets/*, conforme o código:

```sh
<link rel="stylesheet" href="assets/style.css">
```

## Estilizando a aplicação

Com o arquivo criado, podemos iniciar a estilização do nosso código. Para alterar a cor de fundo da aplicação, utilizaremos ```body``` como seletor e entre chaves ({}), utilizaremos a propriedade ```background-color```, com a cor ```bisque```:

```sh
body {
    background-color: bisque;
}
```
Em seguida, começaremos a estilização do rodapé da página. Para isso, utilizaremos como seletor ```footer``` e para alterar a cor de fundo do rodapé, entre chaves ({}) digitaremos ```background-color```, com a cor ```black```. Uma linha abaixo, utilizaremos a propriedade```color``` para alterar a cor do texto para ```white```, como vemos abaixo:

```sh
footer {
    background-color: black;
    color: white;
}
```
Agora, para fixar o rodapé na parte inferior da página, adicionaremos ```bottom:0;``` e ```position:fixed;```. Alteraremos também a largura do rodapé para 100%, garantindo que ele ocupe toda a porção inferior da tela e para isso, digitaremos inseriremos ```width:100%;``` como vemos no código:

```sh
footer {
    background-color: black;
    color: white;
    bottom:0;
    position:fixed;
    width:100%;
}
```
Assim, o rodapé do nosso projeto estará com a seguinte aparência:

![A imagem exibe um fundo bege, e um rodapé com fundo preto. O texto, na cor branca, diz “Projeto desenvolvido pela Aluna, sem fins lucrativos.” Isso significa que o projeto foi criado por uma estudante e não tem fins lucrativos.](img-09)

Para deixar o texto do rodapé centralizado, adicionaremos o seletor ```footer p```, e entre chaves ({}), ```text-align: center```. Mudaremos também, o tamanho do texto do rodapé, inserindo a propriedade ```font-size```, com o valor de ```0.6rem```:

```sh
footer p{
    text-align: center;
    font-size: 0.6rem;
}

```

Para acrescentar mais altura ao nosso rodapé, dentro de ```footer```, adicionaremos ```height``` com o valor ```2rem```:

```sh
    height:2rem;
```
Feito isso, para adicionar um distanciamento entre o texto e a parte superior do rodapé, adicionaremos em ```footer p```, uma margem superior no valor de ```0,5rem```, como no código a seguir:

```sh
    margin-top: 0,5rem;
```

## Adicionando uma nova fonte

Por último, acrescentaremos uma nova fonte para os textos da nossa aplicação. Faremos isso, adiconando em ```body```, a propriedade ```font-family``` e adicionaremos a fonte ```Bai Jamjuree```.

```sh
 font-family: Bai Jamjuree;
```
Com as alterações feitas durante a aula, nosso projeto terá a seguinte aparência:

![A imagem exibe uma captura de tela de uma interface de computador com texto em português relacionado à programação. Possui perguntas sobre a temática programação incluindo: "O que é Java Script?" e "O que é CSS?" além de suas respectivas respostas. A página apresenta um rodapé na cor preta, com o texto: O projeto foi desenvolvido pela Alura sem fins lucrativos.](img10).

## Aula 03


## Para saber mais: Construindo uma Identidade Visual Flexível

Ao desenvolvermos uma aplicação, os elementos de estilo são ferramentas poderosa de comunicar, por meio de formas, cores e espaços, mensagens sutis que criam a identidade visual de uma página web.

Nessa construção de significados, a simetria é utilizada para produzir estabilidade visual, equilibrio e ordem.

O efeito de simetria pode ser produzido em uma página web ao utilizarmos propriedades de distribuição **flexbox** para controlar o espaço entre itens flexíveis, dentre essas propriedades, podemos ressaltar:

-  **`flex-grow`**:Essa propriedade especifica a proporção de espaço que um item deve ocupar em relação aos outros itens dentro do mesmo contêiner. Assim, quando o contêiner se expande, os itens com valores maiores de `flex-grow` aumentam mais do que os itens com valores menores. Se temos dois itens no mesmo contêiner e um item tem `flex-grow: 1` e o outro tem `flex-grow: 3`, o segundo item crescerá três vezes mais do que o primeiro quando o contêiner expandir.

- **`flex-shrink`**: A propriedade `flex-shrink` define a capacidade de um item flexível diminuir de tamanho, caso necessário, quando o espaço disponível diminui.Logo, se o contêiner encolher, os itens com valores maiores de `flex-shrink` diminuem menos do que os itens com valores menores. Uma vez que temos dois itens no mesmo contêiner e um item tem `flex-shrink: 2` e o outro tem `flex-shrink: 1`, o primeiro item diminuirá duas vezes mais do que o segundo quando o contêiner encolher.

- **`flex-basis`**: A `flex-basis` especifica o tamanho inicial de um item flexível antes de distribuir o espaço restante. Desse modo, é preciso estabelecer o tamanho base do item antes de aplicar as regras de crescimento ou encolhimento. Se um item possui `flex-basis: 100px`, ele começará com 100 pixels de largura antes de considerar o espaço adicional disponível.

Essas propriedades são essenciais para criar layouts flexíveis, responsivos e visualmente coerentes em uma aplicação.

## Faça como eu fiz: Estilizando os elementos em tela

Ao analisarmos nosso projeto no *Live Preview*, observamos que nossos cartões não estão dispostos de acordo com nosso protótipo:

![A imagem contém um fundo bege claro com duas seções de texto. Ambas as seções estão sob o título "Programação" em negrito. A primeira seção de texto pergunta "O que é Java Script?" e responde "O Java Script é uma linguagem de programação." A segunda seção de texto pergunta "O que é CSS?" e responde "O CSS é uma linguagem de estilização." No rodapé da imagem, há um texto em branco sobre um fundo preto que diz "Projeto desenvolvido pela Alura, sem fins lucrativos."](Aula03-img01)

## Modificando a disposição dos elementos 

Para modificarmos a disposição dos cartões, em nosso arquivo `style.css` abaixo da estilização de `body`, adicionaremos `container` como seletor, e por ser um elemento `id` utilizaremos uma cerquilha (`#`) na frente e, entre chaves ({}) a propriedade `display` com o valor `flex`:

```sh
#container {
    display:flex ;
}
```
## Personalizando os cartões

Continuaremos estilizando nossos cartões, adicionando espaçamentos e para isso, nosso seletor será `.cartao` e adicionaremos entre chaves ({}) `margin` com o valor de `1rem 1rem`:

```sh
.cartao {
    margin: 1rem 1rem;
}
```
Após isso, no arquivo `index.html`, acrescentamos um paragráfo para conter os textos de perguntas e respostas. Para isso, localizaremos a `div class="cartao__conteudo__pergunta"` e a `div class="cartao__conteudo__resposta"`, digitamos o atalhos do teclado **p + Enter** na linha que contém o ínicio do texto e movemos a tag de fechamento para o final do texto. 

Faremos isso, para o primeiro cartão:

```sh
<div class="cartao__conteudo__pergunta">
    <p>O que é Java Script?</p>
</div>                        
<div class="cartao__conteudo__resposta">
    <p>O Java Script é uma linguagem de programação.</p>
</div>
```
E também para o segundo cartão:

```sh
<div class="cartao__conteudo__pergunta">
    <p>O que é CSS?</p>
</div>                        
<div class="cartao__conteudo__resposta">
    <p>O CSS é uma linguagem de estilização.</p>
</div>
```
Feito isso, de volta ao arquivo `style.css`, continuaremos estilizando nossos cartões. Primeiro, Estabeleceremos uma altura de `20rem` para nossos cartões e para melhorar a visualização das alterações feitas, adicionaremos a cor fantasia `aqua` como cor de fundo, como exibido no código abaixo:
```sh
.cartao {
    margin: 1rem 1rem;
    background-color: aqua;
    height: 20rem;
}
```

Em seguida, para que a disposição de todos os cartões seja igual em tela acrescentaremos a propriedade `flex-grow: 1` e, para dividir o espaço de tela em três, vamos inserir a propriedade `flex-basis` repassando como parametro a função `cal(33% - 6rem)`, desse modo, teremos o seguinte código:

```sh
.cartao {
    margin: 1rem 1rem;
    background-color: aqua;
    height: 20rem;
    flex-grow: 1;
    flex-basis: calc(33% -6rem);
}
```
## Adicionando um novo cartão

Depois disso,  incluiremos um novo cartão na aplicação. Para fazer isso, no arquivo `index.html`, copiaremos a tag `<article>` de um dos nossos cartões e a colaremos logo abaixo dos códigos dos dois primeiros cartões:

```sh
<article class="cartao">
    <div class="cartao__conteudo">
        <h3> Programação </h3>
        <div class="cartao__conteudo__pergunta">
            <p>O que é CSS?</p>
        </div>                        
        <div class="cartao__conteudo__resposta">
            <p>O CSS é uma linguagem de estilização.</p>
        </div>
    </div>
</article>
```
Com isso, nossa tela terá a seguinte aparência:

![A imagem apresenta um fundo bege claro com três seções distintas, cada uma com um fundo azul claro. Cada seção possui o título "Programação" em negrito. A primeira seção possui a pergunta "O que é Java Script?" e tem como resposta "O Java Script é uma linguagem de programação.". A segunda seção apresenta a pergunta "O que é CSS?" e a resposta "O CSS é uma linguagem de estilização." A terceira e útima seção pergunta "O que é CSS?" e responde "O CSS é uma linguagem de estilização."
Cada seção é delineada de forma clara com o texto centrado no fundo azul, proporcionando uma aparência organizada e fácil de ler](Aula03-img02)

Agora, para estilizarmos o texto dos cartões, usaremos como seletor a classe `cartao__conteudo`. E entre chaves ({})centralizaremos o texto com `text-align` com o valor `center`, e `height` no valor de `100%`:
```sh
    .cartao__conteudo {
    text-align: center;
    height: 100%;
}
```
## Personalizando a categoria dos cartões

Para estilizar a categoria das perguntas, nosso seletor será `.cartao__conteudo h3`. Entre chaves ({}), adicionaremos uma cor fantasia `background-color: tomato`, para facilitar nossa visualização, alinharemos o texto da categoria a esquerda, inserindo `text-align` com o valor `left`e um espaçamento interno, `padding`, de `0,5rem`:

```sh
.cartao__conteudo h3 {
    background-color: tomato;
    text-align: left;
    padding: 0.5rem;
}
```
Além disso, vamos inserir a propriedade `position` com o valor `absolute`, uma margem externa, `margin`, com valor de `0.6rem`, arredondaremos as bordas da categoria com `border-radius` com `0.6rem`, por último, estabeleceremos a proporção para a fonte em `font-size: 1vw;`. Com isso, o código para estilização das categorias será:

```sh
.cartao__conteudo h3 {
    background-color: tomato;
    text-align: left;
    padding: 0.5rem;
    position: absolute;
    margin: 0.6rem;
    border-radius: 0.6rem;
    font-size: 1vw;
}
```
Com os estilos aplicados, nossa aplicação estará da seguinte forma:

![A imagem apresenta um fundo bege claro com três seções, cada uma com um fundo azul claro. No topo de cada seção, há um rótulo vermelho com cantos arredondados e o texto "Programação" em negrito.A primeira seção possui a pergunta "O que é Java Script?" e tem como resposta "O Java Script é uma linguagem de programação.". A segunda seção apresenta a pergunta "O que é CSS?" e a resposta "O CSS é uma linguagem de estilização." A terceira e útima seção pergunta "O que é CSS?" e responde "O CSS é uma linguagem de estilização."
Cada seção é delineada de forma clara com o texto centrado no fundo azul, proporcionando uma aparência organizada e fácil de ler]().

### Opinião

Quando precisamos garantir a precisão ao dimensionar elementos ou na aplicação de propriedades do CSS, a função **calc()** é uma poderosa aliada. Essa função nos ajudou a combinar valores com unidades diferentes ao personalizarmos nossos cartões. Em nossa próxima aula, continuaremos desenvolvendo nossa aplicação, até lá!

## Aula 04

Nosso projeto até o momento se encontra com a seguinte aparência:

![A imagem apresenta um fundo bege claro com três seções, cada uma com um fundo azul claro. No topo de cada seção, há um rótulo vermelho com cantos arredondados e o texto "Programação" em negrito.A primeira seção possui a pergunta "O que é Java Script?" e tem como resposta "O Java Script é uma linguagem de programação.". A segunda seção apresenta a pergunta "O que é CSS?" e a resposta "O CSS é uma linguagem de estilização." A terceira e útima seção pergunta "O que é CSS?" e responde "O CSS é uma linguagem de estilização."
Cada seção é delineada de forma clara com o texto centrado no fundo azul, proporcionando uma aparência organizada e fácil de ler](Aula04-img01)

## Adicionando a pasta de imagens
Nessa aula, nós iremos aprimorar o design da nossa aplicação e, para isso, primeiro iremos abrir a pasta ```flash-card``` disponibilizada para download na seção **Preparando o ambiente** e copiaremos a pasta `img`usando o atalho **Ctrl + C**.

![A imagem exibe uma tela de computador com uma janela de pasta aberta, mostrando dois itens dentro da pasta chamada “flashcard-imagens”. O primeiro item é uma subpasta intitulada “img”, representada por um ícone de pasta ligeiramente aberta com o que parece ser uma imagem saindo. O segundo item é um arquivo chamado “readme”, representado por um ícone de documento branco com uma seta azul para baixo e um sinal de ‘X’. O fundo da janela é cinza escuro, e há ícones de navegação no canto superior esquerdo, indicando opções para voltar, avançar ou subir na estrutura de diretórios. Essa imagem pode ser relevante para ilustrar como arquivos e pastas digitais são organizados em um sistema de computador ou para discutir como navegar por essas estruturas.](Aula04-img02)

Feito isso, abriremos o diretório `FLASHCARD`, onde se encontram os arquivos da nossa aplicação, e acessaremos a pasta assets. Em seguida, colaremos  a pasta img em assets com o atalho **Ctrl + V**.

![A imagem exibe uma tela de computador com uma janela de pasta aberta. O nome da pasta selecionada é “FLASHCARD”, destacado em vermelho no canto superior esquerdo. Dentro dessa pasta, há dois subdiretórios visíveis. O primeiro subdiretório tem um ícone que se assemelha a um arquivo de imagem com várias camadas ou versões de uma imagem, e está rotulado como “img”. O segundo item é um arquivo chamado “style”, representado por um ícone que se parece com uma engrenagem ou roda dentada em cima de um documento branco. O plano de fundo da janela do explorador de arquivos é cinza escuro, e as pastas e arquivos estão dispostos em uma visualização de grade. Essa imagem pode ser relevante para ilustrar como ativos digitais são organizados dentro de pastas de projetos, especialmente em projetos de desenvolvimento de software ou web, onde imagens e arquivos de estilo (como CSS) são comumente usados.](Aula04-img03)

## Alterando a imagem de fundo da aplicação
Com a pasta adicionada, abriremos o arquivo `style.css`, e na estilização de `body` apagaremos a cor fantasia que estava sendo utilizada em `background-color` e utilizaremos a propriedade `backgroung`, recebendo como valor `url()`. E entre aspas simples (''), repassaremos o caminho para nossa imagem de fundo `img/bg-desktop.webp`, como vemos no código a seguir:

```sh
body {
    background: url('img/bg-desktop.webp');
    font-family: Bai Jamjuree;
}
```

## Modificando o padrão de cores do projeto
Em seguida, copiaremos do arquivo `readme.md` disponibilizado juntamente com a pasta `img`, o código para criação de variáveis de cor, e o colaremos uma linha acima de `body`, em nosso CSS:

```sh
:root {
    --text-color: #DBE4EF;
    --card-front-color: #144480;
    --card-back-color: #00F4BF;
}
```
Com as variáveis de cor adicionadas, alteraremos a estilização de `cartao__conteudo__h3`. 

Removeremos o `background-color:` com a cor `tomato`, e atribuiremos uma cor para o texto da categoria. Faremos isso, utilizando `color` com a variável `--text-color`. Adicionaremos ainda, uma borda com a mesma cor utilizada para o texto, através da propriedade `border` com o valor de `1px solid var(--text-color)`. Resultando no seguinte código:

```sh
.cartao__conteudo h3 {
    color: var(--text-color);
    border: 1px solid var(--text-color);
    text-align: left;
    padding: 0.5rem;
    position: absolute;
    margin: 0.6rem;
    border-radius: 0.6rem;
    font-size: 1vw;
}
```
Após isso, modoficaremos a cor dos cartões.Adicionaremos, em `.cartao__conteudo`, `background-color`com a variável `--card-front-color`:

```sh
.cartao__conteudo {
    text-align: center;
    height: 100%;
    background-color: var(--card-front-color);
}
```
Outro ajuste necessário, será remover em `.cartao` o `background-color` com a cor fantasia `aqua` que adicionamos.

Com essas modificações, nossa aplicação possuirá o seguinte aspecto:

![A imagem exibe três cartões separados, cada um com uma pergunta e resposta distintas relacionadas ao desenvolvimento web, dentro da categoria programação. O painel esquerdo tem um fundo azul com a pergunta “O que é JavaScript?” e a resposta abaixo diz “É uma linguagem de programação.” O painel do meio, também em fundo azul, pergunta “O que é CSS?” com a resposta “É uma linguagem de estilização.” O painel da direita repete o mesmo padrão e pergunta do painel do meio.](Aula04-img04)

## Estilizando a cor e o peso dos textos
Vamos atribuir pesos e cores diferentes aos textos das perguntas e das respostas. Para as perguntas, utilizaremos como seletor `.cartao__conteudo__pergunta p`e, entre chaves ({}), adicionaremos `color` com o valor `var(--text-color)` e alteraremos o peso da fonte com a propriedade `font-weight:500`:

```sh
.cartao__conteudo__pergunta p{
    color: var(--text-color);
    font-weight: 500;
}
```
Para o texto das respostas, selecionaremos `.cartao__conteudo__resposta p` e entre chaves ({}), adicionaremos `color`com a variável `--card-back-color`, e atribuiremos para `font-weight` o valor de `700`:

```sh
.cartao__conteudo__resposta p{
    color: var(--card-back-color);
    font-weight: 700;
}
```
Com isso, nossa aplicação estará semelhante a imagem a seguir:

![A imagem contém três cartões retangulares com fundo azul e textos em verde e branco. Os cartões estão posicionado lado a lado. Em uma forma de botão arredondado nas extremidades há a palavra "Programação", categorizando as perguntas.O primeiro cartão (à esquerda), possui a pergunta: "O que é Java Script?" e a resposta "O Java Script é uma linguagem de programação.". O segundo e o terceiro cartão, apresentam a pergunta "O que é CSS?" e a resposta "O CSS é uma linguagem de estilização." Na parte inferior da imagem, há um rodapé, com um pequeno texto branco que diz: "Projeto desenvolvido pela Alura, sem fins lucrativos."Os três cartões são apresentados em um fundo com tonalidades de verde e azul.](Aula04-img05).


# Aula 5 - Inserindo o Efeito no cartão

## Projeto da Aula Anterior


Olá, estudante!
Em nossa última aula,  continuaremos desenvolvendo nosso projeto. 
Portanto, você precisará do código que foi desenvolvido até o momento. Caso seja necessário, você pode obter o código criado através deste link:

 [Projeto Aula 04](https://github.com/guilhermeonrails/flashcard/blob/aula_4/index.html)

Vídeo 5.1 - Visibilidade e Rotação

Para saber mais: CSS: Pseudo-classes, Transições e Transformações

Conteúdo

Quando estamos aprendendo sobre desenvolvimento web, entender como estilizar nossas páginas de forma dinâmica e atrativa é essencial. A linguagem de estilização CSS nos apresenta várias alternativas para isso, dentre elas:

`:hover`:
Ao adicionarmos essa palavra-chave a um seletor CSS, podemos criar um efeito sobre um elemento quando o cursor do mouse passa sobre ele. No exemplo abaixo, ao passarmos o mouse sobre o botão ele adquire a cor rosa.

```sh
button:hover {
  background-color: pink;
}
```

`transforme`:
Essa propriedade nos permite aplicar uma série de transformações a um elemento, como mover, girar, escalar e inclinar.
Podemos associá-la a propriedade `rotate` para girar um elemento em torno de um ponto fixo definido, como no exemplo:

```sh
div {
  transform: rotate(45deg);
}
```
`transition`:
A propriedade `transition` permite que as mudanças de estilo em um elemento ocorram de forma suave e projetada durante um período de tempo especificado, criando o efeito de animação sem a necessidade do JavaScript. No exemplo abaixo, estabelecemos que o tempo para que um determinado evento ocorra com a cor de fundo do botão é de 0.3 segundo e que deverá ser suave.

```sh
button {
  transition: background-color 0.3s ease;
}
```
Para conhecer mais sobre transformações, transições e propriedades de animação em CSS, acesse o link:

[Guia de animações em CSS: o que são e quais são os principais benefícios](https://www.alura.com.br/artigos/animacoes-em-css#:~:text=As%20propriedades%20CSS%20de%20anima%C3%A7%C3%A3o,ou%20outra%20linguagem%20de%20programa%C3%A7%C3%A3o.)



Faça como eu fiz: Alternando a visualização das perguntas e repostas

Nessa aula aprendemos como alternar em nosso projeto a exibição de perguntas e respostas, produzindo o efeito de *flashcard*, para isso, seguimos alguns passos:

## Criando o efeito de giro

Observando nosso projeto no Live Preview, notamos que nossos cartões exibem perguntas e respostas simultaneamente, o que não é nossa intenção.

![A imagem contém três cartões retangulares com fundo azul. Cada cartão contém textos em verde e branco. Os cartões estão posicionados lado a lado. Em cada um há um botão com as extremidades arredondadas com a palavra "Programação", categorizando as perguntas.O primeiro cartão (à esquerda), possui a pergunta: "O que é Java Script?" e a resposta "O Java Script é uma linguagem de programação.". O segundo e o terceiro cartão apresentam a pergunta "O que é CSS?" e a resposta "O CSS é uma linguagem de estilização." Na parte inferior da imagem, há um rodapé com um pequeno texto branco que diz: "Projeto desenvolvido pela Alura, sem fins lucrativos."Os três cartões são exibidos em um fundo com tonalidades de verde e azul.](Aula05-img01.png).


Para que ao passarmos o mouse sobre o flashcard ele possua o efeito de giro, no arquivo `style.css`, acima da estilização de `footer`, adicionaremos `.cartao:hover` e `.cartao__conteudo`, e entre chaves ({}), a propriedade `transform` que receberá como valor `rotateY(180deg)`, como vemos abaixo:

```sh
.cartao:hover .cartao__conteudo {
    transform: rotateY(180deg);
}
```

## Personalizando a exibição da resposta

Após isso, para que o texto da resposta não seja invertido ao ser exibido primeiramente, no seletor `.cartao__conteudo`, adicionaremos `transform-style: preserve-3d;`e também acrescentaremos um tempo de transição para a rotação do cartão, inserindo a propriedade `transition`, com o valor `transform 300ms ease-in-out`, como vemos a seguir no código:

```sh
.cartao__conteudo {
    background-color: var(--card-front-color);
    text-align: center;
    height: 100%;
    transform-style: preserve-3d;
    transition: transform 300ms ease-in-out;
}
```

Além disso, para que ao girarmos o cartão a categoria não apareça em tela, em `.cartao__conteudo h3` adicionaremos a propriedade `backface-visibility:` e passaremos como valor ` hidden;`, conforme o código:

```sh
.cartao__conteudo h3 {
    color: var(--text-color);
    border: 1px solid var(--text-color);
    text-align: left;
    padding: 0.5rem;
    position: absolute;
    margin: 0.6rem;
    border-radius: 0.6rem;
    font-size: 1vw;
    backface-visibility: hidden;
}
```
Vamos em seguida especificar que não desejamos que o inverso de nossas perguntas e respostas sejam apresentados em tela ao girarmos os cartões. Para isso, abaixo da estilização de `.cartao:hover`, selecionaremos `.cartao__conteudo__pergunta` e `.cartao__conteudo__resposta`, e entre chaves ({})`bakcface-visibility: hidden`,observe:

```sh
.cartao__conteudo__pergunta,
.cartao__conteudo__resposta {
    backface-visibility: hidden;
}
```

## Revelando as respostas ao girar o cartão

Agora, para que somente o conteúdo da resposta seja exibido ao girarmos o cartão, vamos inserir o seletor `.cartao__conteudo__resposta` e entre chaves ({}), `transform: rotateY(180deg)`, como podemos ver no código:

```sh
.cartao__conteudo__resposta {
    transform: rotateY(180deg);
}
```
Feito isso, ao observarmos nosso projeto no *Live Preview*, ao passarmos o mouse sobre um cartão teremos o seguinte efeito:

![A imagem animada ou gif mostra um cartão de informação ou um flashcard em um layout retangular, com fundo azul escuro e texto branco. O cartão de um lado exibe a pergunta "O que é CSS?", que se encontra na categoria "Programação", que se encontra destacada dentro de um botão arredondado de borda branca com texto branco, a esquerda superior do cartão. Quando o cursor do mouse passa sobre o cartão é exibida a resposta a pergunta "CSS é uma linguagem de estilização".O fundo fora do cartão é em um gradiente de verde escuro para azul escuro. O design é simples e limpo, com foco no título e subtítulo.](Aula05-img02)

## Aprimorando a disposição dos textos

Para que pergunta e resposta sejam exibidos no mesmo local do cartão, no seletor CSS `.cartao__conteudo__pergunta, .cartao__conteudo__resposta` adicionaremos as propriedades `position` com o valor `absolute`, `height: 100%` e `width: 100%`:

```sh
.cartao__conteudo__pergunta,
.cartao__conteudo__resposta {
    backface-visibility: hidden;
    position: absolute;
    height: 100%;
    width: 100%;
}
```
Finalizando, adicionaremos `.cartao__conteudo p`, com uma margin superior, `margin-top`, no valor de `4rem`, como vemos no código:

```sh
.cartao__conteudo p {
    margin-top: 1rem;
    padding: 2rem;
    margin-top: 4rem;
}
```

Assim, ao final da aula nosso projeto terá a seguinte aparência:

![A imagem mostra uma interface de uma página web com um fundo de cor verde escura com alguns círculos desfocados. No centro da imagem, há três cartões retangulares em azul escuro posicionadas horizontalmente, uma ao lado da outra. Os três cartões fazem parte da categoria "Programação", que se encontra destacada dentro de um botão arredondado de borda branca com texto branco, a esquerda superior do cartão. No centro de cartrão, há uma pergunta sendo a primeira, à esquerda: "O que é Java Script?"; a segunda, no centro: "O que é CSS?" e a terceira, à direita: "O que é CSS?". A parte inferior da imagem contém uma barra preta com um texto branco que diz: "Projeto desenvolvido pela Alura, sem fins lucrativos."](Aula05-img03)


### Opinião do autor 

Nosso projeto está bem mais próximo do estipulado em nosso protótipo, com o auxílio da linguagem CSS conseguimos produzir o efeito de girar nossos cartões. Em nossa próxima aula utilizaremos o Java Script para deixar nossa aplicação ainda mais interativa.

### O que aprendemos

## Nessa aula, você aprendeu como:

Adicionar uma imagem ao plano de fundo de uma aplicação;
Utilizar variáveis globais de cor em propriedades CSS;
Alterar o peso das fontes nos textos de diferentes elementos da aplicação.

# Aula 06: Crianco cartões com JS

## Projeto da aula anterior:

## Preparando o ambiente:

## Video: O arquivo perguntas.js

## Para saber mais:

## Faça como eu fiz: 

Nessa aula finalizamos a estilização dos nossos cartões e começamos o desenvolvimento do arquivo `perguntas.js`. Para fazer isso, primeiro analizaremos nosso projeto da aula anterior, após adicionarmos em CSS o efeito de transição:

![A imagem mostra uma interface de uma página web com um fundo de cor verde escura com alguns círculos desfocados. No centro da imagem, há três cartões retangulares em azul escuro posicionadas horizontalmente, uma ao lado da outra. Os três cartões fazem parte da categoria "Programação", que se encontra destacada dentro de um botão arredondado de borda branca com texto branco, a esquerda superior do cartão. No centro de cartrão, há uma pergunta sendo a primeira, à esquerda: "O que é Java Script?"; a segunda, no centro: "O que é CSS?" e a terceira, à direita: "O que é CSS?". A parte inferior da imagem contém uma barra preta com um texto branco que diz: "Projeto desenvolvido pela Alura, sem fins lucrativos."](Aula06-img01)

## Adicionandando novos cartões

Iniciaremos criando um novo cartão e para isso, no arquivo `index.html` selecionaremos a primeira tag `article` que contém os códigos para a criação de um cartão e utilizaremos os atalhos **Ctrl + C** para copiar o código e o **Ctrl + V** para colá-lo uma linha abaixo:

```sh
<article class="cartao">
    <div class="cartao__conteudo">
        <h3>Programação</h3>
        <div class="cartao__conteudo__pergunta">
            <p>0 que é JavaScript?</p>
        </div>
        <div class="cartao__conteudo__resposta">
            <p>0 JavaScript é uma linguagem de programação</p>
        </div>
    </div>
</article>
```
Em seguida, alteraremos no código copiado, os conteúdos de`<h3>` para *Geografia*, de `<p>` na classe `cartao__conteudo__pergunta` para *Qual a capital da França* e, por último na classe `cartao__conteudo__pergunta` modificaremos o texto de `<p>` para *A capital da França é Paris*, como vemos no código a seguir:

```sh
<article class="cartao">
    <div class="cartao__conteudo">
        <h3>Geografia</h3>
        <div class="cartao__conteudo__pergunta">
            <p>Qual a capital da França?</p>
        </div>
        <div class="cartao__conteudo__resposta">
            <p>A capital da França é Paris</p>
        </div>
    </div>
</article>
```
Mas ao observarmos o projeto no *Live Preview*, veremos que sempre que inserimos um novo cartão ele será adicionado **em linha**. Observe:

![A imagem mostra uma interface de uma página web com um fundo de cor verde escura com alguns círculos desfocados. No centro da imagem, há quatro cartões retangulares em azul escuro posicionadas em uma linha horizontalmente, um ao lado da outro. Três cartões fazem parte da categoria "Programação" e um cartão da categoria "Geografia", que se encontra destacada dentro de um botão arredondado de borda branca com texto branco, a esquerda superior do cartão. No centro de cada cartão, há uma pergunta sendo a primeira, à esquerda: "O que é Java Script?"; a segunda: "Qual a capital da frança?"; a terceira: "O que é CSS?" e a quarta, à direita: "O que é CSS?"](Aula06-img2)

Adicionaremos mais um quinto cartão, ao nosso código, e para isso, uma linha abaixo do último criado vamos digitar **Ctrl+V** e alterar o `<h3>` para *Programação 2.0*:

```sh
<article class="cartao">
    <div class="cartao__conteudo">
        <h3>Programação 2.0</h3>
        <div class="cartao__conteudo__pergunta">
            <p>0 que é JavaScript?</p>
        </div>
        <div class="cartao__conteudo__resposta">
            <p>0 JavaScript é uma linguagem de programação</p>
        </div>
    </div>
</article>
```
Após isso, para que aconteça uma quebra de linha automática na disposição dos cartões na tela, em `style.css`, acrescentaremos a propriedade `flex-wrap` com o valor `wrap` a estilização de `container`, conforme o código a seguir:

```sh
#container {
    display: flex;
     flex-wrap: wrap;
}
```
Também, justificaremos o conteúdo, para que os cartões possuam o mesmo espaçamento, adicionando `justify-content` com o valor `space-between`, centralizaremos o conteúdo do cartão, inserindo um `padding` de `4rem`.

```sh
#container {
    display: flex;
     flex-wrap: wrap;
     justify-content: space-between;
     padding: 4rem;
}
```
Com essas alterações feitas vamos adicionar outro cartão. Para isso, retornaremos ao `index.html`, copiaremos a última tag `article` criada e colaremos uma linha abaixo. Feito isso, para melhorar a navegabilidade entre os cartões, adicionaremos um espaçamento maior entre eles, inserindo um `gap` com o valor de `3rem`na estilização de `container`, resultando no código:

```sh
#container {
    display: flex;
     flex-wrap: wrap;
     justify-content: space-between;
     padding: 4rem;
     gap: 3rem;
}
```
## Criando o arquivo Java Script

Para otimizar a criação dos cartões da aplicação, utilizaremos a linguagem **Java Script** para criar cada cartão. Para fazermos isso, primeiro abriremos o *Explorador* do *VS Code*, clicaremos no ícone *Novo Arquivo* e criaremos um arquivo com a extenção `perguntas.js`

![A imagem exibe uma captura de tela de uma interface de computador, especificamente a seção do explorador de arquivos do editor de códigos VS Code. O explorador mostra uma estrutura de diretórios que inclui vários arquivos e pastas. A pasta principal se chama “FLASHCARD” e, há arquivos chamados “perguntas.js”, “index.html” e também uma pasta chamada "assets" com uma pasta nomeada de "img" e o arquivo “style.css”. O arquivo “perguntas.js” está destacado, pois está sendo criado.](Aula06-img03)

No arquivo Java Script, escreveremos a função `criaCartao()`, e entre parenteses, passaremos os parametros `categoria`, `pergunta` e `resposta`, assim como no código a seguir:

```sh
criaCartao(
    categoria,
    pergunta,
    resposta
)
```
Depois disso, copiaremos a função criada e a colaremos uma linha abaixo. Faremos isso duas vezes, o que resultará no código:

```sh
criaCartao(
    categoria,
    pergunta,
    resposta
)

criaCartao(
    categoria,
    pergunta,
    resposta
)

criaCartao(
    categoria,
    pergunta,
    resposta
)
```
Com a estrutura das funções criadas, podemos alterar os elementos, repassando entre aspas simples ('') os textos referentes a *categoria*, *pergunta* e *resposta* de cada cartão, conforme o código abaixo:

```sh
criaCartao(
    'Programação',
    'O que é Python?',
    'O Python é uma linguagem de programação'
)

criaCartao(
    'Geografia',
    'Qual a capital da França?',
    'A capital da França é Paris'
)

criaCartao(
    'Programação',
    'O que é uma função?',
    'Uma função é um bloco de código que executa alguma tarefa'
)
```

Com a estrutura dos cartões elaborada em Java Script, retornaremos ao arquivo `index.html` e manteremos o código de criação de apenas um cartão e apagaremos os demais.

Com isso, em nossa aplicação visualizamos apenas um cartão, em nossa próxima aula utilizaremos as funções que começamos a desenvolver em Java Script para construir nossos outros cartões.

![A imagem mostra uma interface de uma página web com um fundo de cor verde escura com alguns círculos desfocados. No centro da imagem, há um cartão azul escuro. No canto superior esquerdo do cartão, há uma caixa de texto com a palavra “Programação” em fonte branca. No centro do cartão é exibida a pergunta: “O que é JavaScript?”, também em fonte branca.](Aula06-img04)


# Aula 07: Criando uma função

## Projeto da aula anterior:

## Preparando o ambiente:

## Video: Exibindo os parâmetros

## Para saber mais:

## Faça como eu fiz: 

Nessa aula, vamos continuar criando os códigos JavaScript que nos ajudarão a criar cartões automaticamente, mas primeiro vamos observar nosso código da aula anterior:

```sh
criaCartao(
    'Programação',
    'O que é Python?',
    'O Python é uma linguagem de programação'
)

criaCartao(
    'Geografia',
    'Qual a capital da França?',
    'A capital da França é Paris'
)

criaCartao(
    'Programação',
    'O que é uma função?',
    'Uma função é um bloco de código que executa alguma tarefa'
)
```
Esse é o conteúdo do arquivo `perguntas.js` mas, para que o JavaScript possa gerar os cartões, primeiro precisamos vinculá-lo ao `index.html`.

## Integrando o JavaScript ao Projeto

Faremos a integração dos arquivos, abrindo o `index.html` e, digitando uma linha após `</footer>`, a abreviação **script:src** + a tecla **Enter**, o que irá gerar o código:

```sh
<script src=""></script>
```
Então, entre as aspas ("") de `src` vamos adicionar o arquivo `perguntas.js`, como vemos abaixo:

```sh
<script src="perguntas.js"></script>
```

## Criando um gerador de perguntas
Manteremos o arquivo `perguntas.js` somente com o conteúdo das perguntas e criaremos um novo arquivo *JavaScript* para gerar as perguntas. Para isso, digitaremos o atalho do *VS Code* **Ctrl + B** para abrir o *Explorador de arquivos* e clicaremos no ícone *Novo arquivo* e o nomearemos como `app.js`:

![A imagem mostra a interface do Visual Studio Code. No painel esquerdo, está aberto o explorador de arquivos de um projeto chamado "FLASHCARD". O explorador exibe a estrutura de pastas e arquivos do projeto, que inclui uma pasta chamada "assets" e os arquivos "index.html" e "perguntas.js". O arquivo "app.js"  está sendo criado, com o texto destacado. Acima da lista de arquivos, há uma barra de ferramentas com vários ícones. Um dos ícones está destacado com um retângulo vermelho.](Aula07-img01)

Com o arquivo `app.js`criado, adicionaremos o seu link ao `index.html`, uma linha antes do `script` responsável pela inserção das perguntas, conforme o código:

```sh
<script src="app.js"></script>
<script src="perguntas.js"></script>
```
## A `function` criaCartao ()

Em `app.js`, criaremos uma função para realizar a tarefa de criar as perguntas. Para isso, utilizaremos a palavra reservada `function` seguido do  termo `criaCartao()`, o mesmo que utilizamos em `perguntas.js`. Passaremos a essa nova função os parametros que compõem os cartões, `categoria`, `pergunta` e `resposta`. Depois disso, abriremos chaves ({}), observe:

```sh
function criaCartao (categoria, pergunta, resposta) {

}
```
##  Mostrando os parametros dos cartões no console

Com isso, podemos testar a integração dos arquivos JavaScript exibindo os cartões criados em `perguntas.js`. Vamos fazer isso, digitando entre as chaves ({}) da função `console.log()` e, entre os parenteses vamos inserir os parametros `categoria, pergunta, resposta`, conforme o código:

```sh
function criaCartao (categoria, pergunta, resposta) {
    console.log(categoria, pergunta, resposta)
}
```
Feito isso, abriremos nossa aplicação com *Live Preview*, clicaremos com o botão direito do mouse sobre a tela e selecionaremos a opção *Inspecionar*, como mostra a imagem:

![A imagem mostra o menu de contexto do navegador Google Chrome, que é exibido quando o usuário clica com o botão direito do mouse em uma página web. O menu está sobreposto a uma parte da página que contém a pergunta "O que é Java Script?" em um fundo azul.A última opção do menu, "Inspecionar", está destacada com um retângulo vermelho, indicando que o usuário pretende abrir as ferramentas de desenvolvedor do navegador para inspecionar o código-fonte da página.](Aula07-img02)

Na aba aberta, no menu superior da tela, clicaremos em *Console*.
![A imagem mostra a interface das ferramentas de desenvolvedor do navegador. No topo da interface, há um aviso informando que as DevTools agora estão disponíveis em português.Abaixo desse aviso, a barra de navegação das ferramentas de desenvolvedor apresenta várias abas, incluindo "Elements", "Console", "Sources", "Network", entre outras. A aba "Console" está destacada com um retângulo vermelho, indicando que o usuário deve clicar nela para abrir o console.](Aula07-img03)

Assim, os parametros dos cartões estarão exibidos:

![A imagem mostra a interface de ferramentas do desenvolvedor aberta. A aba selecionada é “Console”, onde são exibidos comandos e mensagens em texto branco sobre um fundo escuro. Na área do console, vemos três linhas de texto. A primeira pergunta sobre a capital da França (respondida como Paris), a segunda indaga sobre o que é Python (respondido como uma linguagem de programação) e a terceira explica o conceito de função em Python.](Aula07-img04)

Em nossa próxima aula, vamos aprender como exibir nossos cartões na tela da nossa aplicação.

## Aula 08

## Faça como eu fiz: Gerando Cartões com JavaScript

Nesta aula vamos utilizar o JavaScript para exibir nossos cartões na tela da nossa aplicação. Que por enquanto, apresenta apenas um cartão.

![](Aula08-img01)

## Declarando variáveis para utilizar métodos

Nosso primeiro passo para exibir nosso cartões será buscar o elemento HTML que contém os cartões. 

Para isso, no arquivo `app.js`, vamos remover o `console.log()` da função `criaCartao` e em seu lugar, declarar uma variável `let` nomeada como `container`. 

```sh
function criaCartao(categoria, pergunta, resposta) {
        let container 
}
```

Para que a variável acesse o elemento `id=container` com os cartões da aplicação, passaremos como valor à ela `document.getElementById('container')` como vemos a seguir:

```sh
function criaCartao(categoria, pergunta, resposta) {
        let container = document.getElementById('container')
}
```

Depois disso, para que o JavaScript crie elementos do tipo `<article>`, o elemento HTML que utilizamos para conter um cartão, vamos declarar outra variável `let`, nomeada de `cartao` e, atribuiremos como valor `document.createElement('article')`:

```sh
function criaCartao(categoria, pergunta, resposta) {
        let container = document.getElementById('container')
        let cartao = document.createElement('article')
}
```
Além disso, é necessário repassar a classe HTML que atribuimos ao `article`. Faremos isso, digitando `cartao.className = cartao`, como vemos abaixo:

```sh
function criaCartao(categoria, pergunta, resposta) {
        let container = document.getElementById('container')
        let cartao = document.createElement('article')
        cartao.className = 'cartao'
}
```
## Passando o conteúdo do cartão para o JavaScript

Agora, para que a estrutura que construimos em HTML seja repassada para os cartões que serão gerados pela função `criaCartao`, vamos utilizar a variável `cartao` que criamos e a propriedade `.innerHTML` e como valor, entre crases (``)o  código HTML responsável pela estrutura do conteúdo do cartão, conforme o código a seguir:

```sh
cartao.innerHTML = `
<div class="cartao__conteudo">
<h3>Programação</h3>
<div class="cartao__conteudo__pergunta">
        <p>O que é JavaScript?</p>
</div>
<div class="cartao__conteudo__resposta">
        <p>O JavaScript é uma linguagem de programação</p>
</div>
</div>
`
```
Após isso, vamos associar a variável `cartao` a variável `container`, uma vez que cada cartão criado precisa estar contido dentro de `container`. Para isso, digitaremos `container.`, o método `appendChild` e entre parentêses a variável `cartao`, resultado no seguinte código:

```sh
container.appendChild(cartao)
```
Assim, ao visualizarmos nosso projeto no *Live Preview*, ele terá a seguinte aparência:

![A imagem mostra uma interface de uma página web com um fundo de cor verde escura com alguns círculos desfocados. No centro da imagem, há quatro cartões retangulares em azul escuro. Cada cartão têm um fundo azul e contêm texto branco. Eles estão dispostos em duas linhas. Na linha superior, há três quadrados dispostos lado a lado e na linha inferior, há um retângulo central. Todos os cartões têm um rótulo na parte superior, na porção esquerda, que diz "Programação" em uma pequena caixa de fundo azul claro com borda branca e o texto em branco. Dentro de cada quadrado e do retângulo, há a mesma pergunta escrita: "O que é JavaScript?"](Aula08-img02)

Para que somente os cartões gerados pelo *JavaScript* estejam vísiveis em tela, comentaremos no `index.html` todo conteúdo de `<article>`, inserindo `<!--` na abertura da tag, e `-->` em seu fechamento, como mostra o trecho de código a seguir:

```sh
        <!-- <article class="cartao">
                <div class="cartao__conteudo">
                        <h3>Programação</h3>
                        <div class="cartao__conteudo__pergunta">
                                <p>O que é JavaScript?</p>
                        </div>
                        <div class="cartao__conteudo__resposta">
                                <p>O JavaScript é uma linguagem de programação</p>
                        </div>
                </div>
        </article> -->
```
Com essa alteração, nossa aplicação exibirá somente os três cartões gerados pelo *JavaScript*, observe:

![](Aula08-img03)

## Exibindo perguntas 

Para que os cartões que elaboramos em `perguntas.js` sejam acessados, substituiremos os textos em `h3` e nas tags `p` pelos parametros categoria, pergunta e resposta, que repassamos à função `criaCartao`. 

Assim, em `h3` apagaremos o texto do título, digitaremos o caractere cifrão ($) e entre chaves ({}) `categoria`. Em `p` da classe `cartao__conteudo__pergunta` alteraremos o texto para `${pergunta}` e por último, em `cartao__conteudo__resposta` substituiremos o texto por `${resposta}`:

```sh
cartao.innerHTML = `
        <div class="cartao__conteudo">
        <h3>${categoria}</h3>
        <div class="cartao__conteudo__pergunta">
                <p>${pergunta}</p>
        </div>
        <div class="cartao__conteudo__resposta">
                <p>${resposta}</p>
        </div>
        </div>
`
```
Com essas modificações feitas, ao visualizarmos nossa página web com o *Live Preview*, visualizaremos os cartões que criamos no arquivo `perguntas.js`.

![](Aula08-img04)

Como teste, adicionaremos outra pergunta ao arquivo `perguntas.js`. Para isso, utilizaremos a função `criaCartao` que deve conter os parametros `categoria, pergunta, resposta` veja:

```sh
    criaCartao(
    'Lingua inglesa',
    'Como se diz OI em inglês?',
    'Oi em ingles é HI (RAI)'
) 
```
Com essa adição, passamos a ter quatro cartões em tela:

![](Aula08-img05)

Em nossa próxima aula, construiremos uma lista de perguntas para compor nossa aplicação.

## Para saber mais:

Quando uma página web é carregada por um navegador web, ele cria uma representação em árvore dessa página, chamada *DOM*. Essa representação possui uma hierarquia e cada elemento *HTML* é chamado de nó, cada nó podem ter "filhos" (outros elementos contidos neles) e "pais" (elementos que os contêm).

Para modificarmos esses nós, podemos utilizar métodos *JavaScript*, que são funções associadas a um objeto ou uma variável.

### Métodos comuns em *JavaScript*:

- `getElementById`: Este método permite que você encontre um elemento específico pelo seu ID. Por exemplo:

```sh
let container = document.getElementById('container')
```
Nesse trecho de código procuramos pelo `id` `container`.

- `innerHTML`: Este método permite que você obtenha ou altere o conteúdo *HTML* de um elemento. Por exemplo:

```sh
cartao.innerHTML = `
        <div class="cartao__conteudo">
        <!-- Código omitido… -->
        </div>
        `
```
- `createElement`: Este método cria um novo elemento HTML, mas não o adiciona automaticamente à página. Por exemplo:

```sh
let cartao = document.createElement('article')
```
- `appendChild`: Este método insere um novo nó filho (elemento) na estrutura do DOM de um documento. Por exemplo:

```sh
container.appendChild(cartao)
```
O código acima, insere a variável `cartao` como um elemento filho de `container`.

Para conhecer mais sobre o *DOM* e métodos *HTML*, você pode acessar o site da [w3schools](https://www.w3schools.com/js/js_htmldom.asp).


Aula 9: Virando o cartão com o clique

Video: O método AddEventListener()

Faça como eu fiz: Criando eventos de clique.

Em nossa última aula, conseguimos vincular a criação das perguntas da nossa aplicação ao nosso arquivos em Java Script `perguntas.js`, e sempre que passamos o mouse sobre um cartão criado ele mostra a resposta, observe:

![A imagem é um print de uma aplicação web de flashcards. O cartão está na categoria "Geografia" e apresenta a pergunta "Qual a capital da França?" em texto branco sobre um fundo azul. Quando o mouse sobrepõem o cartão, é exibida pela página web a resposta "A capital da França é Paris."](Aula09-img01)

Mas precisamos agora, que os cartões exibam as resposta somente quando forem clicados. 

Para isso, no arquivo `app.js`, uma linha antes do código `container.appendChild(cartao)`, vamos declarar uma variável do tipo `let` chamada `respostaEstaVisivel` com o valor `false`, para que sempre que iniciarmos a aplicação as respostas não estejam visíveis.

```sh
let respostaEstaVisivel = false

```
Logo abaixo da variável, vamos criar uma função para virar o cartão quando clicarmos nele. Faremos isso primeiro declarando `function ()` e adicionando entre chaves ({}), `respostaEstaVisivel= !respostaEstaVisivel`.

```js
function viraCartao(){
    respostaestaVisivel = !respostaEstaVisivel
}
```

A seguir, no arquivo `style.css`, apagaremos o `:hover` de `.cartao: hover`, e vamos adicionar a classe `.active`, em seu lugar:

```sh
.cartao.active .cartao__conteudo {
    transform: rotateY(180deg);
}
```
E de volta ao `app.js`, para controlar a exibição ou não da resposta nos cartões, dentro da `function ViraCartao()`, digitaremos `cartao.classList.toggle('active', respostaEstaVisivel)`, deixando nosso código da seguinte forma:

```sh
function viraCartao() {
    respostaEstaVisivel = !respostaEstaVisivel
    cartao.classList.toggle('active', respostaEstaVisivel)
}
```
Depois disso, abaixo da função que criamos, digitaremos `.cartao.` e utilizaremos o método `addEventListener()`, para que sempre que ocorrer um clique em um cartão, ele vire e exiba a resposta. Entre os parêntese adicionaremos como parâmetros o evento que precisa `click` e a função `viraCartao` com a tarefa que será executada quando o clique ocorrer, veja:

```sh
cartao.addEventListener('click', viraCartao)

```
Após isso, os cartões da nossa só exibem as respostas das perguntas quando clicamos sobre eles. E ao clicarmos novamnete, retornam a posição original.

![A imagem do tipo "gif" é um print de uma aplicação web de flashcards. O cartão está na categoria "Geografia" e apresenta a pergunta "Qual a capital da França?" em texto branco sobre um fundo azul.Quando ocorre um evento de clique sobre ele, o cartão gira e exibe a resposta "A capital da França é Paris". Após isso, ocorre um novo clique e o cartão volta a exibir a pergunta.](Aula09-img02)

Aula 10

Ao observarmos nosso projeto, veremos que ele está funcional e possui muitos elementos que estipulamos em seu protótipo.

![A imagem do tipo "gif" é um print de uma aplicação web de flashcards. O cartão está na categoria "Geografia" e apresenta a pergunta "Qual a capital da França?" em texto branco sobre um fundo azul.Quando ocorre um evento de clique sobre ele, o cartão gira e exibe a resposta "A capital da França é Paris". Após isso, ocorre um novo clique e o cartão volta a exibir a pergunta.](Aula10-img01)

Nessa aula, vamos refinar os elementos da nossa aplicação.

## Alterando a cor de fundo do cartão resposta e o tamanho dos textos

Para que nossos cartões possuam uma cor de fundo diferente no lado das respostas, no arquivo `style.css`, vamos alterar a estilização da classe `.cartao__conteudo__resposta`. Desse modo, a propriedade `background-color`, passará a receber `rdba(0, 244, 191, 0.2)`, conforme o código abaixo:

```sh
.cartao__conteudo__resposta{
    transform: rotateY(180deg);
    background-color: rdba(0, 244, 191, 0.2);
}
```
também adicionaremos uma borda ao redor da carta de resposta. Para isso, adicionaremos `border` com o valor `4px solid`, e com a cor `var(--card-back-color)`:

```sh
.cartao__conteudo__resposta{
    transform: rotateY(180deg);
    background-color: rgba(0, 244, 191, 0.2);
    border: 4px solid var(--card-back-color);
}
```
Contudo, ao observarmos o projeto no *Live Preview*, notaremos um pequeno espaço entre a carta e a margem que adicionamos, veja:

![](Aula10-img02)

Para que as margens que adicionarmos sempre ocupem a totalidade das dimenções do cartão, na estilização de `.cartao__conteudo__pergunta, .cartao__conteudo__resposta`, acrescentaremos `box-sizing` com o valor `border-box`:

```sh
.cartao_conteudo_pergunta,
.cartao_conteudo_resposta {
    backface-visibility: hidden;
    position: absolute;
    height: 100%;
    width: 100%;
    box-sizing: border-box;
}
```
Adequaremos também o tamanho das fontes utilizadas em nossa aplicação, adicionando em `.cartao__conteudo p`, a propriedade `font-size` com o valor de `1.4vw`:

```sh
.cartao__conteudo p {
    margin-top: 1rem;
    padding: 2rem;
    margin-top: 4rem;
    font-size: 1.4vw;
}
```
## Adaptando a exibição para dispositivos mobile

Para adequarmos os elementos da tela à exibição em telas menores, como de celulares, vamos adicionar ao final do arquivo `style.css` a regra `@media` e estabelecer que para telas com tamanho máximo de 560 pixels `max-width:560px`, aplicação deve ter o comportamento que vamos específicar entre chaves ({}):

```sh
@media (max-width: 560px){

}
```
Entre as chaves definiremos que a imagem de fundo da aplicação será a imagem disponibilizada especificamente para *mobile*. Para isso, digitaremos `body` e entre chaves `background:` e a url da imagem que desejamos, conforme o código a seguir:

```sh
@media (max-width: 560 px) {

    body {
        background: url('img/bd-mobile.webp');
    }

}
```

