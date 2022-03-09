---
layout: default
title: Tocar uma música MP3
---

Construa um programa que toque uma música MPEG-1 Layer 3 (vulgo MP3, arquivo com extensão
<code>.mp3</code>).

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
    "from pydub import AudioSegment\n" +
    "nomeArquivoMp3 = pickAFile()\n" +
    "print(&#039;Olá! Você escolheu um arquivo&#039;, nomeArquivoMp3)\n" +
    "nomeArquivoWav = nomeArquivoMp3 + &quot;.wav&quot;\n" +
    "somMp3 = AudioSegment.from_mp3(nomeArquivoMp3)\n" +
    "somMp3.export(nomeArquivoWav, format=&quot;wav&quot;)\n" +
    "somWav = makeSound(nomeArquivoWav)\n" +
    "play(somWav)";
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


[Exercício anterior](./exercise3.html)
[Próximo exercício](./exercise5.html)
