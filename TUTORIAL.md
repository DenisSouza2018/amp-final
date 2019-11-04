Iremos converte uma pagina HTML para uma pagina AMP

Passo 1: Precisamos adicionar a biblioteca do AMP no HTML
que iremos converte;

  <script async src="https://cdn.ampproject.org/v0.js">
  </script>

-----------------------------------------------------------------------
Passo 2: Vamos ativar o validados do AMP, para isso iremos inserir no final na URL
  
  #development=1 

-----------------------------------------------------------------------
Passo 3: Especificar o atributo do AMP na raiz da tag <html>

  <html ⚡ lang="en">
  <html amp lang="en">

-----------------------------------------------------------------------
Passo 3.2: Incluir link Canonico

  <link rel="canonical" href="index.html">

-----------------------------------------------------------------------
Passo 3.3: Precisamos especificar a janela de visualização que AMP irá usar.

  <meta name="viewport" content="width=device-width,minimum-scale=1,initial-scale=1">

-----------------------------------------------------------------------
Passo 3.4: Substituir as folhas de estilo externas com o codigo

    <style amp-custom>
      /* Copiar todo conteudo do arquivo style.css aqui */
    </style>

-----------------------------------------------------------------------
Passo 3.5: Excluir todo javaScript de terceiros

  REMOVER:<script type="text/javascript" src="script.js"></script>

-----------------------------------------------------------------------
Passo 3.6: Incluir CSS padão do AMP

  <style amp-boilerplate>
    body {
      -webkit-animation: -amp-start 8s steps(1, end) 0s 1 normal both;
      -moz-animation: -amp-start 8s steps(1, end) 0s 1 normal both;
      -ms-animation: -amp-start 8s steps(1, end) 0s 1 normal both;
      animation: -amp-start 8s steps(1, end) 0s 1 normal both
    }

    @-webkit-keyframes -amp-start {
      from {
        visibility: hidden
      }

      to {
        visibility: visible
      }
    }

    @-moz-keyframes -amp-start {
      from {
        visibility: hidden
      }

      to {
        visibility: visible
      }
    }

    @-ms-keyframes -amp-start {
      from {
        visibility: hidden
      }

      to {
        visibility: visible
      }
    }

    @-o-keyframes -amp-start {
      from {
        visibility: hidden
      }

      to {
        visibility: visible
      }
    }

    @keyframes -amp-start {
      from {
        visibility: hidden
      }

      to {
        visibility: visible
      }
    }
  </style><noscript>
    <style amp-boilerplate>
      body {
        -webkit-animation: none;
        -moz-animation: none;
        -ms-animation: none;
        animation: none
      }
    </style>
  </noscript>

-----------------------------------------------------------------------
Passo 3.7: Substituir todas as tag <img> pelo padrão AMP <amp-img>

  exemplo:
    <amp-img src="mountains.jpg" layout="responsive" width="266" height="150"></amp-img>


-----------------------------------------------------------------------
Extra Teste de performance de páginas

  * http://www.websiteoptimization.com/services/analyze/

