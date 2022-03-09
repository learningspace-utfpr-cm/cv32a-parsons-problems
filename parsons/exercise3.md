---
layout: default
title: Mostrar duas imagens pré-definidas em sequência
---

Construa um programa que mostre duas imagens JPEG (arquivo com extensão <code>.jpg</code>)
pré-definidas e em sequência, mas reutilize o código que mostra a imagem, colocando-o
em uma função.

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Obter comentário" type="button" /> 
    <input id="newInstanceLink" value="Reiniciar problema" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "from jes4py import *\n" +
    "def mostrarImagem(nomeArquivoImagem):\n" +
    "        print(&#039;Olá! Você escolheu um arquivo&#039;, nomeArquivoImagem)\n" +
    "        imagem = makePicture(nomeArquivoImagem)\n" +
    "        show(imagem)\n" +
    "\n" +
    "mostrarImagem(&#039;/home/...&#039;)\n" +
    "mostrarImagem(&#039;/home/...&#039;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


[Exercício anterior](./exercise2.html)
[Próximo exercício](./exercise4.html)
