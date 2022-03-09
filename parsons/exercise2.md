---
layout: default
title: Mostrar duas imagens pré-definidas em sequência
---

Construa um programa que mostre duas imagens JPEG (arquivo com extensão <code>.jpg</code>) pré-definidas e em sequência.


<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Obter comentário" type="button" /> 
    <input id="newInstanceLink" value="Reiniciar problema" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "from jes4py import *\n" +
    "nomeArquivoImagem1 = &#039;/home/.../&#039;\n" +
    "print(&#039;Olá! Você escolheu um arquivo&#039;, nomeArquivoImagem1)\n" +
    "imagem1 = makePicture(nomeArquivoImagem1)\n" +
    "show(imagem1)\n" +
    "nomeArquivoImagem2 = &#039;/home/.../&#039;\n" +
    "print(&#039;Olá! Você escolheu um arquivo&#039;, nomeArquivoImagem2)\n" +
    "imagem2 = makePicture(nomeArquivoImagem2)\n" +
    "show(imagem2)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
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


[Exercício anterior](./exercise1.html)
[Próximo exercício](./exercise3.html)
