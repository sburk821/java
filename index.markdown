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
