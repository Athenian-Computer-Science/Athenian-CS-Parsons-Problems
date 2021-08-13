# Rearrange the blocks to create and run a function that returns "Hello World!" Pay attention to indentation and be aware of distractor blocks.

<div id="basic_function_1-sortableTrash" class="sortable-code"></div> 
<div id="basic_function_1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="basic_function_1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="basic_function_1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "def greeting():\n" +
    "	hello = &quot;Hello World!&quot;\n" +
    "	return hello\n" +
    "print(greeting())\n" +
    "greeting() #distractor\n" +
    "greeting(&quot;Hello World!&quot;) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "basic_function_1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "basic_function_1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#basic_function_1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#basic_function_1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
