### 1.3 input and print
This exercise should prompt the user for their name and print a greeting. Arrange the appropriate blocks and check your answer when you think you are done.

<div id="input_print-sortableTrash" class="sortable-code"></div> 
<div id="input_print-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="input_print-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="input_print-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "name = input(&#039;Please enter your name: &#039;)\n" +
    "print(f&quot;It&#039;s nice to meet you, {name}!&quot;)\n" +
    "name = print(&#039;Please enter your name: &#039;) #distractor\n" +
    "name = print(input(&#039;Please enter your name: &#039;)) #distractor\n" +
    "print(f&#039;It&#039;s nice to meet you, {name}!&#039;) #distractor\n" +
    "print(&quot;It&#039;s nice to meet you, {name}!&quot;) #distractor\n" +
    "print(f&quot;It&#039;s nice to meet you, name!&quot;) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "input_print-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "input_print-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#input_print-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#input_print-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
