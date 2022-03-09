---
layout: default
title: Mostrar uma imagem (Jpg) a ser escolhida
---

Construa um programa que mostre uma imagem JPEG (arquivo com extensão <code>.jpg</code>). 

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
    "nomeArquivoImagem = pickAFile()\n" +
    "print(‘Olá! Você escolheu um arquivo’, nomeArquivoImagem)\n" +
    "imagem = makePicture(nomeArquivoImagem)\n" +
    "show(imagem)";
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


[Próximo exercício](./exercise2.html)
