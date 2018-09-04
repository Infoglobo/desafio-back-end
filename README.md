# Quer trabalhar em nosso time de Engenharia Backend?

Esse é o nosso desafio para você! O objetivo é avaliar o seu conhecimento e habilidades em desenvolvimento backend.

# Desafio

Criar um crawler que leia [este feed] (http://revistaautoesporte.globo.com/rss/ultimas/feed.xml)
e retorne um json estruturado da seguinte forma:

```
{
    'feed': [
        'item': {
            'title': 'titulo da materia',
            'link': 'url da materia',
            'description': [
                {
                    'type': 'text',
                    'content': 'conteudo da tag'
                },
                {
                    'type': 'image',
                    'content': 'url da imagem'
                },
                {
                    'type': 'links',
                    'content': ['urls dos links', ...]
                }
            ]
        },
        'item': {
            ...
        },
        'item': {
            ...
        },
        'item': {
            ...
        }
    ]
}
```

## Requisitos

* O campo titulo deve ser identico ao item do feed;
* O campo links deve ser identico ao item do feed;
* O campo description deve ser estruturado da seguinte forma: 
  * tag p (com conteúdo) deve gerar um bloco do tipo 'text' com o texto como content;
  * tag div//img deve gerar um bloco do tipo 'image' com o endereço da imagem como content;
  * tag div//ul deve gerar um block do tipo 'links', com o endereço de cada link no content;


Para escrever o teste sinta-se a vontade para usar linguagem e tecnologia que desejar mas lembre-se a proposta é avaliar a sua capacidade como desenvolvedor.

Ao concluir, publique o resultado em seu repositório e envie-nos a URL de seu desafio para que possamos avaliar.

## Diferenciais

* Cobertura de testes;
* Projeto conteinerizado;
* Organização e legibilidade do código;
* Desafio extra:
  * Implementar como um webservice;
  * Permitir que somente usuários cadastrados possam acessar o webservice;


## Exemplo do retorno


**Feed item:**

```
  <item>
    <title><![CDATA[Volkswagen Arteon aparece às vésperas do Salão de Genebra]]></title>
    <description><![CDATA[<div class="foto componente_materia midia-largura-620">
    <img alt="Volkswagen Arteon (Foto: Divulgação)" height="413" id="209451" src="http://s2.glbimg.com/DIgFxpN0aAu99uvuZ3WmSqAUV2E=/620x413/e.glbimg.com/og/ed/f/original/2017/03/06/1_WKIn5xh.jpg" title="Volkswagen Arteon (Foto: Divulgação)" width="620" /><label class="foto-legenda">Volkswagen Arteon (Foto: Divulga&ccedil;&atilde;o)</label></div>
<p>
    &nbsp;</p>
<p>
    <strong>A <a href="http://revistaautoesporte.globo.com/carros/volkswagen">Volkswagen</a> revelou hoje (6) o Arteon, cup&ecirc; de quatro portas escolhido para suceder o CC</strong> &ndash; antes chamado Passat CC &ndash; e que ser&aacute; apresentado ao p&uacute;blico durante o Sal&atilde;o de Genebra. <strong>O visual n&atilde;o chega a ser novidade, j&aacute; que &eacute; praticamente o mesmo h&aacute; dois anos</strong>, <a href="http://revistaautoesporte.globo.com/Noticias/noticia/2015/03/volkswagen-sport-coupe-gte-adianta-visual-de-futuros-sedas.html">quando deu as caras no evento su&iacute;&ccedil;o como o prot&oacute;tipo Sport Coup&eacute; GTE Concept</a>.</p>
<div class="foto componente_materia midia-largura-620">
    <img alt="Volkswagen Arteon (Foto: Divulgação)" height="413" id="209450" src="http://s2.glbimg.com/NgWcluzNZLlXwCu9Vs8N1UHXGbI=/620x413/e.glbimg.com/og/ed/f/original/2017/03/06/2_aEXyzmK.jpg" title="Volkswagen Arteon (Foto: Divulgação)" width="620" /><label class="foto-legenda">Volkswagen Arteon (Foto: Divulga&ccedil;&atilde;o)</label></div>
<p>
    &nbsp;</p>
<p>
    Para encarar o mundo real, a novidade recebeu ma&ccedil;anetas nas portas, antena no teto e alguns detalhes exigidos por lei... e s&oacute;! <strong>At&eacute; mesmo as rodas gigantes, os para-choques agressivos e a grade do motor integrada aos far&oacute;is continuam ali</strong> &ndash; para a alegria dos f&atilde;s. Al&eacute;m do pacote esportivo R-Line, tamb&eacute;m haver&aacute; op&ccedil;&otilde;es um pouco mais conservadoras.</p>
<div class="foto componente_materia midia-largura-620">
    <img alt="Volkswagen Arteon (Foto: Divulgação)" height="413" id="209449" src="http://s2.glbimg.com/lJKzhfcrbXSzQZRKXCcn7pEIRjw=/620x413/e.glbimg.com/og/ed/f/original/2017/03/06/3_BZIDgsI.jpg" title="Volkswagen Arteon (Foto: Divulgação)" width="620" /><label class="foto-legenda">Volkswagen Arteon (Foto: Divulga&ccedil;&atilde;o)</label></div>
<p>
    &nbsp;</p>
<p>
    Se por fora tudo &eacute; diferente (e muito mais agressivo) comparado aos &ldquo;irm&atilde;os&rdquo;, o painel segue fiel ao estilo da marca &ndash; afinal, &eacute; o mesmo do Passat. N&atilde;o sabemos se a queda do teto compromete o espa&ccedil;o para a cabe&ccedil;a de quem vai atr&aacute;s, <strong>mas os 563 litros do porta-malas s&atilde;o bem aproveitados gra&ccedil;as &agrave; tampa traseira que abre com o vidro</strong>, como um hatch.</p>
<div class="foto componente_materia midia-largura-620">
    <img alt="Volkswagen Arteon (Foto: Divulgação)" height="413" id="209447" src="http://s2.glbimg.com/RJ9LxS8YaH4bCAlP1f_1Nm8cocY=/620x413/e.glbimg.com/og/ed/f/original/2017/03/06/4_vYYIbul.jpg" title="Volkswagen Arteon (Foto: Divulgação)" width="620" /><label class="foto-legenda">Volkswagen Arteon (Foto: Divulga&ccedil;&atilde;o)</label></div>
<p>
    &nbsp;</p>
<p>
    A plataforma &eacute; a mesma MQB utilizada no Passat (que, gra&ccedil;as ao milagre da modularidade, tamb&eacute;m serve ao Golf e, futuramente, &agrave; nova gera&ccedil;&atilde;o do Gol nacional). <strong>S&atilde;o 4,86 metros de comprimento; 1,87 m de largura; 1,42 m de altura; e 2,84 m de entre-eixos</strong>. Ainda que pare&ccedil;a um latif&uacute;ndio, apenas quatro ocupantes viajam com conforto na cabine.</p>
<div class="foto componente_materia midia-largura-620">
    <img alt="Volkswagen Arteon (Foto: Divulgação)" height="413" id="209446" src="http://s2.glbimg.com/EDuoev-xcbKnAK_QVWRclJa4Mac=/620x413/e.glbimg.com/og/ed/f/original/2017/03/06/5_71gviOe.jpg" title="Volkswagen Arteon (Foto: Divulgação)" width="620" /><label class="foto-legenda">Volkswagen Arteon (Foto: Divulga&ccedil;&atilde;o)</label></div>
<p>
    &nbsp;</p>
<p>
    No Velho Continente, <strong>ser&atilde;o oferecidos motores a gasolina (1.5 turbo com 150 cv e 2.0 turbo nas op&ccedil;&otilde;es de 190 cv e 280 cv) e tamb&eacute;m a diesel (2.0 turbo nas op&ccedil;&otilde;es de 150 cv, 190 cv e 240 cv)</strong>. Com exce&ccedil;&atilde;o das vers&otilde;es de entrada, que t&ecirc;m c&acirc;mbio manual de seis marchas, a transmiss&atilde;o &eacute; sempre automatizada com dupla embreagem e sete marchas.</p>
<div class="saibamais componente_materia expandido">
    <strong>saiba mais</strong>
    <ul>
        <li>
            <a href="http://revistaautoesporte.globo.com/Noticias/noticia/2016/01/os-12-mimos-mais-legais-do-volkswagen-passat.html">OS 12 MIMOS MAIS LEGAIS DO VOLKSWAGEN PASSAT</a></li>
        <li>
            <a href="http://revistaautoesporte.globo.com/Analises/noticia/2015/11/avaliacao-novo-volkswagen-passat.html">AVALIA&Ccedil;&Atilde;O: NOVO VOLKSWAGEN PASSAT</a></li>
    </ul>
</div>
<p>
    &nbsp;</p>
<div class="foto componente_materia midia-largura-620">
    <img alt="Volkswagen Arteon (Foto: Divulgação)" height="413" id="209448" src="http://s2.glbimg.com/fkJMyLGJsX_ThzJBHalbemmcb4M=/620x413/e.glbimg.com/og/ed/f/original/2017/03/06/6_pih5QJE.jpg" title="Volkswagen Arteon (Foto: Divulgação)" width="620" /><label class="foto-legenda">Volkswagen Arteon (Foto: Divulga&ccedil;&atilde;o)</label></div>
<p>
    &nbsp;</p>
]]></description>
    <link>http://revistaautoesporte.globo.com/Noticias/noticia/2017/03/volkswagen-arteon-aparece-vesperas-do-salao-de-genebra.html</link>
    <dc:creator>Da redação de Auto Esporte</dc:creator>
    <guid>1139465</guid>
  </item>

```

**Json item:**

```
{
   "title":"Volkswagen Arteon aparece às vésperas do Salão de Genebra",
   "link":"http://revistaautoesporte.globo.com/Noticias/noticia/2017/03/volkswagen-arteon-aparece-vesperas-do-salao-de-genebra.html",
   "content":[
      {
         "type":"image",
         "content":"http://s2.glbimg.com/DIgFxpN0aAu99uvuZ3WmSqAUV2E=/620x413/e.glbimg.com/og/ed/f/original/2017/03/06/1_WKIn5xh.jpg"
      },
      {
         "type":"text",
         "content":"A Volkswagen revelou hoje (6) o Arteon, cupê de quatro portas escolhido para suceder o CC – antes chamado Passat CC – e que será apresentado ao público durante o Salão de Genebra. O visual não chega a ser novidade, já que é praticamente o mesmo há dois anos, quando deu as caras no evento suíço como o protótipo Sport Coupé GTE Concept."
      },
      {
         "type":"image",
         "content":"http://s2.glbimg.com/NgWcluzNZLlXwCu9Vs8N1UHXGbI=/620x413/e.glbimg.com/og/ed/f/original/2017/03/06/2_aEXyzmK.jpg"
      },
      {
         "type":"text",
         "content":"Para encarar o mundo real, a novidade recebeu maçanetas nas portas, antena no teto e alguns detalhes exigidos por lei... e só! Até mesmo as rodas gigantes, os para-choques agressivos e a grade do motor integrada aos faróis continuam ali – para a alegria dos fãs. Além do pacote esportivo R-Line, também haverá opções um pouco mais conservadoras."
      },
      {
         "type":"image",
         "content":"http://s2.glbimg.com/lJKzhfcrbXSzQZRKXCcn7pEIRjw=/620x413/e.glbimg.com/og/ed/f/original/2017/03/06/3_BZIDgsI.jpg"
      },
      {
         "type":"text",
         "content":"Se por fora tudo é diferente (e muito mais agressivo) comparado aos “irmãos”, o painel segue fiel ao estilo da marca – afinal, é o mesmo do Passat. Não sabemos se a queda do teto compromete o espaço para a cabeça de quem vai atrás, mas os 563 litros do porta-malas são bem aproveitados graças à tampa traseira que abre com o vidro, como um hatch."
      },
      {
         "type":"image",
         "content":"http://s2.glbimg.com/RJ9LxS8YaH4bCAlP1f_1Nm8cocY=/620x413/e.glbimg.com/og/ed/f/original/2017/03/06/4_vYYIbul.jpg"
      },
      {
         "type":"text",
         "content":"A plataforma é a mesma MQB utilizada no Passat (que, graças ao milagre da modularidade, também serve ao Golf e, futuramente, à nova geração do Gol nacional). São 4,86 metros de comprimento; 1,87 m de largura; 1,42 m de altura; e 2,84 m de entre-eixos. Ainda que pareça um latifúndio, apenas quatro ocupantes viajam com conforto na cabine."
      },
      {
         "type":"image",
         "content":"http://s2.glbimg.com/EDuoev-xcbKnAK_QVWRclJa4Mac=/620x413/e.glbimg.com/og/ed/f/original/2017/03/06/5_71gviOe.jpg"
      },
      {
         "type":"text",
         "content":"No Velho Continente, serão oferecidos motores a gasolina (1.5 turbo com 150 cv e 2.0 turbo nas opções de 190 cv e 280 cv) e também a diesel (2.0 turbo nas opções de 150 cv, 190 cv e 240 cv). Com exceção das versões de entrada, que têm câmbio manual de seis marchas, a transmissão é sempre automatizada com dupla embreagem e sete marchas."
      },
      {
         "type":"links",
         "content":[
            "http://revistaautoesporte.globo.com/Noticias/noticia/2016/01/os-12-mimos-mais-legais-do-volkswagen-passat.html",
            "http://revistaautoesporte.globo.com/Analises/noticia/2015/11/avaliacao-novo-volkswagen-passat.html"
         ]
      },
      {
         "type":"image",
         "content":"http://s2.glbimg.com/fkJMyLGJsX_ThzJBHalbemmcb4M=/620x413/e.glbimg.com/og/ed/f/original/2017/03/06/6_pih5QJE.jpg"
      }
   ]
}
```

# Sobre nós

## Infoglobo
A Infoglobo através de seus produtos - os jornais O Globo, Extra e Expresso, com os sites Globo e Extra e a Agência O Globo - tem o dever de apurar o fato, oferecendo aos seus leitores a informação mais completa, sempre com a preocupação de adequar a linguagem ao público a que se destina. Além de esclarecer o que acontece de mais importante no Brasil e no mundo, os produtos da Infoglobo também são uma ferramenta de acesso ao melhor do entretenimento e da cultura. A Infoglobo tem muito orgulho desse papel e trabalha com o compromisso de levar jornalismo sério e isento à população.

## Editora Globo
Desde 1952, a Editora Globo dissemina conhecimento entre os leitores e produz um jornalismo independente que antecipa as transformações da sociedade. Moderna, dinâmica e inovadora, a empresa conecta consumidores a conteúdos que transformam suas vidas e oferecem a eles a liberdade de escolherem em qual plataforma preferem ler. Com mais de 16 revistas no portfólio - incluindo as marcas Vogue, Casa Vogue, GQ e Glamour, após joint-venture estabelecida com a Condé Nast - a Editora Globo e Edições Globo Condé Nast têm 3,4 milhões de cópias por mês, 9,2 milhões de leitores, 18 websites, 11,4 milhões de visitantes únicos por mês, 40 eventos anuais, 25 aplicativos para iPhone, iPad e Android e mais de 1 milhão de downloads. Ainda, contamos com a marca Globo Livros, que tem mais de mil títulos no catálogo de livros, de autores nacionais e internacionais, publicados em menos de dois anos. No digital, a marca conta com 200 títulos e parcerias com os principais players do mercado, como Apple, Kobo Cultura, Google, Saraiva and Amazon.

