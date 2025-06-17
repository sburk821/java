---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Lösungen für gänige Probleme rund um Arrays
---
# Übungen zu Arrays
## Charts ausgeben ##
Möchte man die ersten 100 (200, ...) Titel der aktuellen Charts ausgeben, wären entsprechend viele print-Anweisungen aus verschiedensten Gründen keine gute Lösung.

## Maximum ##
<div id="maximum-sortableTrash" class="sortable-code"></div> 
<div id="maximum-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="maximum-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="maximum-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
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
    "    System.out.print(charts[i])\n" +
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



### Example Next Link
[Next](./parsons/example1.html)
