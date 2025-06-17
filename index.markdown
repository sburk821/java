# Übungen zu Arrays
## Charts ausgeben ##
Möchte man die ersten 100 (200, ...) Titel der aktuellen Charts ausgeben, wären entsprechend viele print-Anweisungen aus verschiedensten Gründen keine gute Lösung.

<div id="charts-sortableTrash" class="sortable-code"></div> 
<div id="charts-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="charts-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="charts-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "for (int i = 0; i < charts.length; i++) {\n" +
    "	System.out.print(\"Platz \"+i+1+\": \");\n" +
    "	System.out.print(charts[i]);\n" +
    "	System.out.println(\"\");\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "charts-sortable",
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
  $("#charts-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#charts-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
## Sudoku ##
Es soll ein zweidimensionales Array ausgegeben werden, sodass ein vollständiges Bild des im Array gespeicherten Sudoku entsteht.
Wir nutzen die Top-Down-Methode, um uns schrittweise einer konkreten Lösung zu nähern.
### Variante 1 ###
<div id="sudoku1-sortableTrash" class="sortable-code"></div> 
<div id="sudoku1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="sudoku1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="sudoku1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "Wiederhole für alle Zeilen\n" +
    "	gib alle Elemente der aktuellen Zeile aus";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sudoku1-sortable",
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
  $("#sudoku1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#sudoku1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
### Variante 2 ###
<div id="sudoku2-sortableTrash" class="sortable-code"></div> 
<div id="sudoku2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="sudoku2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="sudoku2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "Wiederhole für alle Zeilen i\n" +
    "	Wiederhole für alle Elemente j\n" +
    "    	gib Element an Stelle i, j aus";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sudoku2-sortable",
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
  $("#sudoku2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#sudoku2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
### Variante 3 ###
<div id="sudoku3-sortableTrash" class="sortable-code"></div> 
<div id="sudoku3-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="sudoku3-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="sudoku3-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "for (int i = 0; i<sudoku.length; i++) {\n" +
    "	for (int j = 0;j<sudoku[0].length; j++ ) {\n" +
    "		System.out.print(sudoku[i][j]+\" \");\n" +
    "	}\n" +
    "	System.out.println(\"\");\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sudoku3-sortable",
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
  $("#sudoku3-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#sudoku3-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
