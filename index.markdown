---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Parsons Practice
## Maximum ##
<div id="maximum-sortableTrash" class="sortable-code"></div> 
<div id="maximum-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="maximum-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="maximum-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "int maximum = array[0];\n" +
    "for (int i = 0; i&lt;array.length) {\n" +
    "	if (array[i] &gt; maximum) {\n" +
    "		maximum = array[i];\n" +
    "	}\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "maximum-sortable",
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
  $("#maximum-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#maximum-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



### Example Next Link
[Next](./parsons/example1.html)
