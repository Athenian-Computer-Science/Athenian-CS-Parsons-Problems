### 1.3 input and print
Arrange the appropriate blocks to construct a program that prompts the user for their name and prints a greeting in response. Check your answer when you think you are done.
<div id="input-print-sortableTrash" class="sortable-code"></div> 
<div id="input-print-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="input-print-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="input-print-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "name = input(&quot;Name: &quot;)\n" +
    "print(f&quot;Welcome to CS, {name}!&quot;)\n" +
    "print(f&quot;Welcome to CS, name!&quot;) #distractor\n" +
    "print(&quot;Welcome to CS, {name}!&quot;) #distractor\n" +
    "name = print(input(&quot;Name: &quot;)) #distractor\n" +
    "name = print(&quot;Name: &quot;) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "input-print-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "trashId": "input-print-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#input-print-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#input-print-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

