## If Statements
Arrange the blocks to give the user directions depending on the outside temperature.

<div id="if_elif_else-sortableTrash" class="sortable-code"></div> 
<div id="if_elif_else-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="if_elif_else-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="if_elif_else-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "temp = input(&quot;Is it cold outside?&quot;)\n" +
    "if temp == &quot;Yes&quot;:\n" +
    "	print(&quot;Grab a coat!&quot;)\n" +
    "elif temp == &quot;Maybe&quot;:\n" +
    "	print(&quot;Check the temp!&quot;)\n" +
    "else:\n" +
    "	print(&quot;No coat needed.&quot;)\n" +
    "elif: #distractor\n" +
    "else temp == &quot;No&quot;: #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "if_elif_else-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "if_elif_else-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#if_elif_else-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#if_elif_else-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
