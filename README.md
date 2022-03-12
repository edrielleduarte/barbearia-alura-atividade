# CRIAÇÃO FORMULÁRIOS

- Para criarmos um formulário, colocamos a tag main e depois form
  label e input sempre andam juntos pois o label tem o id do input e serve pra facilitar ao clicar na mensagem
  e seleciona.

type="submit" value="Enviar Formulario"> // isso é igual o botão de enviar

# CSS FORMULARIO

Vamos então observar na nossa estrutura do HTML. Temos aqui a tag “form” e a tag “main”, mas uma das coisas que reparamos, inclusive olhando as páginas anteriores, é que queremos o conteúdo com 940 pixels de largura e que ele esteja sempre centralizado. Se queremos isso, vamos no nosso estilo CSS alterar isso no main. Então, na tag main, vamos colocá-la com 940 pixels de largura “width: 940px;” e uma margem zero auto “margin: 0 auto;”. Salvando e recarregando isso na página, nosso conteúdo já está centralizado.

    Pra isso, usamos o:
    form{
    margin: 40px 0;
    }

Eu quero agora, começando a página do contato, que a minha tag do formulário “form {” tenha uma margem superior de 40 pixels, para os lados 0, e inferior de 40 pixels “margin: 40px 0;”. Eu quero que tenha um espaço entre o fim do cabeçalho e o início do meu formulário, e entre do meu formulário e o início do rodapé.

    Pra isso, usamos o:
    form{
    margin: 40px 0;
    }

Reparem que quando nós olhamos nos módulos anteriores, vimos que todo elemento tem um tipo de display. Ou ele é um display do tipo inline ou é um display do tipo block. Por padrão, os elementos como o parágrafo são display do tipo block, ou seja, eles ocupam 100% da largura da página. O elemento do tipo inline ocupa só o tamanho do seu conteúdo.

Conseguimos observar aqui no nosso formulário que todos os campos de um formulário são do tipo inline, eles só ocupam o tamanho do seu conteúdo. Após o label, imediatamente vem o input, e após o input imediatamente vem outro label. Nós precisamos começar a quebrar essa estrutura. E para quebrar a estrutura nós precisamos que todos os campos, que são os labels do meu formulário, sejam block “display:block;”. E preciso também que todos os inputs do meu formulário sejam block.

    form label {
    display: block;
    }

    form input {
    display: block;
    }

Espaço dos labels, posso fazer com o margin, conforme o exemplo:
form {
margin: 40px 0;
}

    form label {
    display: block;
    font-size: 20px;
    margin: 0 0 10px;
    }

    form input {
    display: block;
    margin: 0 0 20px;
    }

Para caixa de texto para escrever, utilizamos a tag:<br>
`<textarea> </textearea>` ou pra colocar coluna ou linhas podemos colocar: <br>
` <textarea cols="70" rows="10"></textarea>`

# OPÇÕES DE CONTATO USANDO RADIO

São exemplos embaixo o uso de radio para caixinhas selecionadas.

            <label for="email">Email</label>
            <input type="radio" name="contato" id="email" value="email">

            <label for="telefone">Telefone</label>
            <input type="radio" name="contato" id="telefone" value="telefone" checked>

            <label for="whatsapp">Whatsapp</label>
            <input type="radio" name="contato" id="whatsapp" value="whatsapp">

            <input type="submit" value="Enviar Formulario">

Para começar colocando uma ja marcada, so no final do input antes da tag > de fechamento, colocamos o checked

- A propriedade name só pode ser "preenchida" uma única vez, por isso que, quando eu seleciono um dos itens, ele desmarca o outro, mantendo somente um selecionado.
  - Ou seja todo input de checkbox e radio o name faz com as opções seja do mesmo grupo e faz escolher um ou outro.

# SOBRE CSS

tag = peso 1
class = 10
id = peso 100
Se tivermos duas tag ex: form p { color: red; } ela vai ser mais forte do que apenas p { color: blue;} <br>
Se tivermos a classe na hora de chamar no css .nomeclasse , vai ser mais forte e o id tb, na hora de chamar #nomeidentifador { color: orange;}

O inline é mais forte que todos, que fica nas tags do htmo exemplo: `<p style="color: purple;"> oi </p>`
nada substitui o inline

# DROPDOWN

O seletor não é um campo do tipo input, ele é um campo do tipo select, e um campo do tipo select tem dentro dele várias opções. As opções são campos de conteúdo, e aqui eu vou colocar os valores: `<option>Manhã</option>`, uma outra opção que é a `<option>Tarde</option> `e uma outra opção que é a `<option>Noite</option>`. E aqui, para ter o texto dizendo qual o horário prefere ser atendido, eu também vou colocar um parágrafo `<p>Qual horário prefere ser atendido?</p>`. E novamente para criar uma unidade no nosso HTML, vou colocar esse grupo dentro de uma div.

- Ficara como exemplo de baixo: <br>
  `<select>` <br>
  `<option value="">Manhã</option>` <br>
  `<option value="">Tarde</option>` <br>
  ` <option value="">Noite</option>` <br>
  `</select>`

# TIPOS TYPE NO MOBILE

Pensa no seu dia a dia. Quantas horas você passa no celular, quantas horas você passa no computador, e mesmo que você esteja no computador do trabalho, você ainda está usando um celular? Por isso é muito importante que nossa página, nosso formulário e nossos campos estejam adaptados para isso.

Para falar dos campos específicos e da forma como o formulário se apresenta no celular, eu não vou poder no computador aqui mostrar, mas existe um recurso bem legal na internet que é um site chamado Mobile Input Types. Se vocês jogarem isso no Google, o primeiro o resultado já vai ser esse site. E aqui ele mostra visualmente qual o resultado esperado quando estamos usando um tipo de HTML5 de input em um celular.

- TEM VARIOS INPUT

# FORMULARIO FILDSET

Mas dentro do formulário, quando queremos agrupar os campos e quando queremos ter um título para isso, temos tags específicas, que deixam nosso formulário melhor escrito. A primeira é a divisão, quando temos um campo e um texto, ou vários campos referentes a alguma coisa, não usamos a tag div, usamos a tag fieldset. Ela é referente à configuração de um ou mais campos referentes a um assunto específico.

Quando eu poderia usar esse aqui além do que eu já estou usando? Quando, por exemplo, eu tenho o preenchimento dos dados de um cartão de crédito. Todos os dados referentes àquele cartão podem estar dentro de um fieldset. Ou os dados de um endereço. E dentro de um fieldset não temos parágrafos, nós temos o título, e o título de um fildset é chamado de legend.

Salvando e recarregando o nosso navegador, vimos que ele perdeu a formatação, mas por que ele perdeu a formatação? Porque no CSS estávamos usando a tag específica “form p”. Aqui podemos usar a tag legend. E todo “form legend” vai ter aquela configuração da fonte que queríamos. Reparem que o nosso formulário continua se apresentando visualmente da mesma forma. A única coisa que fizemos é deixar o nosso código melhor escrito.

Ficara como no exemplo a seguir:

                <fieldset>
                    <legend>Qual horário prefere ser atendido?</legend>
                    <select>
                        <option value="">Manhã</option>
                        <option value="">Tarde</option>
                        <option value="">Noite</option>
                    </select>
                </fieldset>

# BUTTON CSS

Podemos fazer varias alterações no botão, como transição, aumentar e uma delas é o transform, na qual mexe com a rotação conforme a baixo.
E o transtion all para todos sentindos:

    transition: 1s all;


    .enviar:hover {
    background: darkorange;

    transform: rotate(20deg) scale(1.2);
    }

# TABELA

Abaixo do nosso formulário, vamos começar a tabela, e a tag da tabela é a tag `<table>.` O que é uma tabela? Uma tabela é uma sequência de linhas e colunas. É exatamente isso que precisamos fazer com o CSS. Uma linha é uma `<tr>`, e nós teremos quatro linhas. Em cada uma das linhas, teremos duas células, e a célula se chama `<td>`. Então em cada uma das linhas teremos duas `<td>`.
Exemplo abaixo:

<table>
            <tr>
                <td>Dia</td>
                <td>Horário</td>
            </tr>
            <tr>
                <td>Segunda</td>
                <td>08h ~ 20h</td>
            </tr>
            <tr>
                <td>Quarta</td>
                <td>08h ~ 20h</td>
            </tr>
            <tr>
                <td>Sexta</td>
                <td>08h ~ 20h</td>
            </tr>
        </table>

## OUTRO EXEMPLO DE TABELA

Dentro de uma tabela, podemos separá-la em três: o cabeçalho, o conteúdo e o rodapé. Assim como separamos o nosso conteúdo da página principal em header, main e footer, dentro da tabela, usamos tags específicas da tabela para poder fazer isso. Dentro da tabela, o cabeçalho eu marco com a tag <thead>, e dentro dele vamos ter essa primeira linha. Dentro do cabeçalho, para dizer que aquela célula é uma célula do cabeçalho, ao invés de usarmos a tag <td>, usamos ainda a tag <th>, que é uma célula do head da tabela. Com isso, nós conseguimos ter um cabeçalho bem mais semântico.
Mas não basta só separarmos o cabeçalho. Separamos também o corpo da tabela, e o corpo da tabela é o <tbody>. Todas essas três linhas vão estar dentro do <tbody>, e nós o fechamos aqui embaixo.
Se tivéssemos ainda uma tabela que fosse, por exemplo, um cálculo, uma planilha, na última linha geralmente temos o somatório daquela coluna inteira. E poderíamos ainda usar o <tfoot>, dentro dele uma tag `
” para cada uma das linhas, e “” para cada uma das células dentro do rodapé da tabela. No nosso caso não temos esse conteúdo, estruturamos a tabela dessa forma.

    <thead>
                <tr>
                    <th>Dia</th>
                    <th>Horário</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Segunda</td>
                    <td>08h ~ 20h</td>
                </tr>
                <tr>
                    <td>Quarta</td>
                    <td>08h ~ 20h</td>
                </tr>
                <tr>
                    <td>Sexta</td>
                    <td>08h ~ 20h</td>
                </tr>
            </tbody>
    </thead>

# PRINCIPAL INDEX SECTION E DIV

- A diferença entre `<div>` e `<section>` é que no primeiro caso, trata-se apenas de uma divisão visual. Já no caso da `<section>` teremos uma divisão por conteúdo complexo, semanticamente homogêneo.

Na parte de benefícios, também possuímos conteúdos fechados em si, neste caso também substituiremos a `<div>` por `<section>`

- margin: 0 0 0 0px; = margin: cima direita baixo esquerda;

# FLOAT CSS

O próximo passo é fazer com que o texto englobe essa imagem. Conhecemos algumas formas de tratar esses elementos, a primeira é utilizar o display do elemento para inline-block, e então todos os parágrafos seguirão o mesmo modo. Neste caso específico esta abordagem não funcionará, pois o display altera o comportamento do elemento padrão, e neste caso queremos que a imagem ocupando uma área específica e que o texto ocupe a largura inteira da página, mas que ceda espaço para a imagem.

Estudamos também o posicionamento(position) relativo, que coleta o ponto inicial e a partir disso faz deslocamentos. Aprendemos ainda sobre o posicionamento absoluto, em que podemos deslocar o ponto inicial para qualquer lugar. Neste caso, a imagem ficará por cima do texto, descolada da apresentação. Em suma, trabalhar com position não resolverá nossos problemas.

Temos, ainda, mais uma forma de posicionar e tratar elementos: o float, em tradução livre "flutuação". Quando utilizamos este recurso,o elemento "descola" da página mas o que seria a sua sombra, continua sendo ocupada virtualmente, isto é, o texto respeita esse espaço ocupado.

Para fazermos nossa imagem "flutuar" acessaremos style.css e definiremos em utensilios qual é o lado que desejamos que a flutuação ocorra, neste caso, left.

    .utensilios {
        width: 150px;
        float: left;
    }

Feita essa alteração, os parágrafos começam a se alinhar de acordo com a imagem. Contudo, o elemento está posiconado na extrema esquerda da tela, e o texto se inicia na mesma linha e o título "Benefícios" também foi desalinhado. O float é um recurso que altera completamente a estrutura da página, todos os elementos abaixo do float passam a ser afetados por ele. Podemos criar uma "barreira" que delimitará seu alcance na página.

De volta a style.css em titulo-principal, adicionaremos a propriedade clear que "limpa" o float que está posicionado à esquerda.

    .titulo-principal {
        text-align: center;
        font-size: 2em;
        margin: 0 0 1em;
        clear: left;
    }

# SOBRE ILINE BLOCK, IMAGEM DO LADO DO OUTRO

O display quando configurado com inline-block, possui um detalhe que modifica o modo de exibição: ele interpreta no HTML todas as linhas do bloco de código, incluisive os espaços vazios entre a lista e a imagem. Portanto, quando utilizamos esse recurso, os elementos no HTML precisam estar colados, para que esse espaço não reflita na exibição da pagina.

# CSS PRIMEIRA LINHA DE UMA LISTA EM NEGRITO

A próxima etapa é negritar o primeiro item da lista. Antigamente, a única possibilidade de realizar esse tipo de operação era criar classes específicas para uma alteração que deveria ser no CSS. Hoje em dia com as atualizações e melhorias do CSS, temos os já mencionados pseudo-elementos. <br>
.itens:first-child { <br>
font-weight: bold; <br>
}

No CSS temos algo chamado pseudo-elementos. Conhecemos alguns deles, como :hover, :active, :visited, :required. Tais recursos são utilizados para marcar melhor nossos elementos e gerar um comportamento mais interessante em nosso site.

Dessa maneira, o primeiro item estará em negrito ao carregarmos o navegador. Dessa maneira criamos, via CSS, uma marcação. Além do first-child, temos a opção last-child que marcará o último item da lista. Isso é interessante, porque não precisaremos mais saber quantos itens existem na lista para passar configurações precisas, essa caracaterística é muito útil em manipulação de tabelas, por exemplo.

Por fim, temos a possibilidade de selecionar qualquer elemento da lista por via do nth-child(), que receberá o número que quisermos, como por exemplo 4, que se refere ao quarto elemento da lista. Podemos ainda utilizar valores como 2n com o nth-child(), o que quer dizer marcamos todos os elementos pares da lista, isto é, o segundo, quarto e sexto elemento da lista ficam em negrito.

- Exemplo:<br>
  .itens:nth-child(4){<br>
  font-weight: bold; <br>
  }

  # TRANSIÇÃO

Podemos no css usar o `background: linear-gradient(45deg, orange 50%, blue, purple);`, coloco as cores, o grau que quer começar, a porcentagem da onde e etc.

# NEGRITO APENAS NA PRIMEIRA LETRA COM CSS

Quero na frase "Nega e flor é linda" e a letra N em negrito com css
Utilizamos a tag, class no caso, identificador, exemplo:

    .nomeclasse:first-letter{
        font-weight: bold;
    }

Para colocar todos paragrafos da pagina em italico é so realizar seguinte procedimento:

    p:first-line {
    font-style: italic;
    }

O before que vem antes e o after depois no css sempre tem o content: "conteudo que quer";, é o conteudo que vai aparecer.

# SELECIONANDO PARAGRAFOS

Para selecionar uma certa tag, vamos supor tenho uma main e em seguida um paragrafo tag p, quero fundo vermelho para isso utilizamos no css o:

    main > p {
        background: red;
    }

Mas como selecionar o primeiro parágrafo que sucede uma imagem, por exemplo? Conseguimos selecionar o primeiro filho com o seletor que acabamos de conhecer, mas neste caso estamos falando do primeiro irmão que vem depois de um elemento.

Neste caso, usamos img como elemento âncora e para o primeiro irmão usamos o sinal de "+", exemplo:

    img + p {
        background: blue;
    }
          - Tem que seguir do pai, irmão e dps + o filho

Para selecionar todos os parágrafos localizados depois de uma imagem usamos o seletor ~

    img ~ p {
        background: yellow
    }

Se eu quiser não selecionar uma suposta tag, coloco conforme o exemplo:

    .principal p:not(#missao) {
    background:orange;
    }

# CALCULO CSS

Em nosso CSS, verificaremos que o tamanho da imagem é de 120px, mas como podemos fazer com que esse tamanho seja proporcional? Basta mudar para percentual, isto é, 20% de largura tendo a tela como referência.

Para que a imagem sempre ocupe a medida correta em outros dispositivos, utilizamos a propriedade calc. O calculo que desejamos realizar é escrito entre parênteses, em que inserimos o primeiro valor, o tipo de operção e o resultado esperado.

    .utensilios {
            width: calc(40% - 26px);
            float: left;
            Margin: 0 20px 20px}

Dessa forma, foi calculado precisamente 350px de largura para este elemento. É possível encadear quantas operações quisermos, no mesmo modelo de sintaxe.

    .utensilios {
    width: calc(40% - (26px * 4);
    float: left;
    Margin: 0 20px 20px

    }

- A propriedade calc nos dá o poder de fazer com o que cremos valores proporcionais específicos.

# OPACIDADE

Usamos a propriedade opacity, exemplo no css opacity: 0.3

ou com CSS 3, podemos utilizar mais uma camada - a de opacidade, chamada alfa - nas cores em RGB. Para tanto, utilizamos o rgbae então definir os valores que quisermos.

    .titulo-principal {
    text-align: center;
    font-size: 2em;
    margin: 0 0 1em;
    clear: left;
    color: rgb(0,0,0,0.3);
    }

Esse recurso pode ser utilizado em todas as cores: de fundo, texto, borda e assim por diante.

# SOMBRAS CSS

O nome da propriedade que utilizaremos para gerar esse efeito é box-shadow, que possui a propriedade do eixo X, T e uma cor. Queremos deslocar 10px no eixo X e Y, a cor que utilizaremos será preto.

    .imagem-beneficios {
        width: 60%
        opacity: 1;
        transition: 400ms;
        box-shadow: 10px 10px #000000;
        }

Ao recarregarmos a página, teremos uma sombra projetada, quadrada.

odemos melhorar a qualidade estética dessa sombra ao adicionarmos uma terceira propriedade chamada blur, em que podemos aplicar um nível de desfoque específico, no caso, inseriremos um valor de 5px. Quanto maior a quantidade de pixels que inserirmos, mais claro sera o efeito de desfoque.

    .imagem-beneficios {
        width: 60%
        opacity: 1;
        transition: 400ms;
        box-shadow: 10px 10px 5px #000000;
    }

Temos ainda uma quarta propriedade que configura a intensidade da borda a partir do tamanho do elemento, isto é, o tamanho da sombra projetada. Neste caso, inseriremos 20px:

    .imagem-beneficios {
    width: 60%
    opacity: 1;
    transition: 400ms;
    box-shadow: 10px 10px 5px 20px #000000;

    }

Podemos adicionar várias sombras em um mesmo elemento, basta que o conteúdo esteja separado por uma vírgula. Essa nova sombra terá valores negativos e terá a cor amarela.

- box-shadow: 10px 10px 5px 20px #00000, -10px -10px yellow;

Outra possibilidade no CSS 3 é criar sombras internas. Utilizaremos a própria sessão de benefícios para exempliciar esse efeito, que será utilizado em box-shadowe se chama inset. Seu posicionamento será a partir do centro do elemento e terá a cor vermelha.

    .beneficios {
    padding: 3em 0;
    background: #888888;
    box-shadow: inset 0 0 #FF0000;
    }

Ao carregarmos a página, não notaremos qualquer mudança. Isso se deve pelo fato de que a sombra possui o mesmo tamanho do elemento. Para que ela se torne perceptível, criaremos um espaçamento de 30px.

     .beneficios {
    padding: 3em 0;
    background: #888888;
    box-shadow: inset 0 0 30px #FF0000;
    }

Para fechar o tópico de sombras, por último aprenderemos a inserir sombras em textos. Em titulo-principal, utilizaremos a propriedade text-shadow, que recebem os valores que já conhecem.

    .titulo-principal {
    text-align: center;
    font-size: em;
    margin: 0 0 1em;
    clear: left;
    text-shadow: 2px 2px #FF0000;
    }

# Meta tag de Viewport

Temos que preparar o site para também ser visto e utilizado no celular
No momento em que habilitamos essa opção, nosso site passa a se comportar como se estivesse sendo visualizado via celular: o conteúdo é compartimentando em 940px, o mínimo para esse tipo de plataforma. Atualmente, temos alguns problemas nesse tipo de visualização: a logo marcar está pequena,o menu está pouco legível assim como o conteúdo da lista de benefícios.

Primeriamente, precisamos compreender quantos pixels existem na tela para trabalhamos em uma melhor exibição. Atualmente, nossa tela se adapte ao tamanho disponibilizado pelo navegador, sendo o mínimo 940px. No caso de celulares o panorama é diferente: mesmo que a resolução do dispositivo seja de 2000px de largura, a quantidade de pixels existentes na tela sempre será diferente. Esses valores são chamados de DPI, isto é, a densidade de pixels por polegada.

Geralmente, os celulares possuem 320px de largura de tela,alguns maiores oscilam entre 350px e 480px. Portanto se o mínimo é 940px, teremos um valor discrepante. Uma informação crucial é saber quantos pixels possui a tela do usuário.

Trabalharemos com uma nova tag <meta>, mas dessa vez com propriedade e valor name="viewport" embutidas. Queremos, ainda, saber a largura do dispositivo, e para isso usaremos a propriedade content com o valor width=device-width.

            <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width">
        <title>Barbearia Alura</title>
        <link rel="stylesheet" href="style-home.css">
        <link href="https://fonts.googleapis.com/css?family=Montserrat&display=swap" rel="stylesheet">
        </head>

Precisaremos, então, adaptar o CSS para que ele funcione nessa tela. Precisamos entregar para telas até 450px um estilo diferente, e faremos isso por meio de media queries. Perguntaremos ao navegador qual é o tamanho da tela em questão e, se for aquele que desejamos, entregaremos o estilo correto.

Para realizar isso, utilizaremos o @media, com o valor do tipo de tela screen e a pesquisa. Todas as telas que tenham até 450, terão esse estilo diferente, reescrito. Para exempliciar, colocaremos no background um estilo da cor vermelha.

    @media screen and (max-width: 480px) {
        body {
            background: red;
        }
    }
    - É dentro dessa media query que criamos um estilo visual que compreenda telas de até 480px.

# ADAPTAR RESPONSIVE

Primeiramente nos atentaremos para o cabeçalho, que possui 940px de altura. Se inserirmos uma altura automática, o posicionamento dos elementos que compõe a sessão se deforma, portanto essa não é uma boa saída para solucionar a questão. Em style.css mudaremos a altura da caixa para auto. Quando elaboramos layouts responsivos, precisamos trabalhar exclusivamente no elemento que será modificado.

Faremos o mesmo procedimento para principal, conteudo-beneficios, mapa-conteudo e video.

    @media screen and (max-width: 480px) {
        .caixa, .principal, .conteudo-beneficios, .mapa-conteudo, .video {
            width: auto;
        }
    }

Precisaremos ainda fazer uma pequena alteração na classe video, e anterar o width para 100%, assim evitamos uma deformação no layout.

- Na página index.html, dentro do head, adicione a tag meta viewport, logo abaixo da tag meta charset:

  ` <meta name="viewport" content="width=device-width">`

2. Altere o tamanho do vídeo, para não ser mais fixo e sim ocupar toda a largura da tela, com width="100%":

`<iframe width="100%" height="315" src="https://www.youtube.com/embed/wcVVXUV0YUY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>`

3. No arquivo style.css, adicione um estilo diferente para dispositivos de até 480 pixels de largura:

`@media screen and (max-width: 480px) {
.caixa, .principal, .conteudo-beneficios, .mapa-conteudo, .video {
width: auto;
}

    h1 {
        text-align: center;
    }

    nav {
        position: static;
    }

    .lista-beneficios, .imagem-beneficios {
        width: 100%;
    }

}`
