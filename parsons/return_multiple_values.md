### Returning multiple values from a function
Arrange the blocks to calculate the two values, return them both from the function and the print the results.

<div id="return_multiple_values-sortableTrash" class="sortable-code"></div> 
<div id="return_multiple_values-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="return_multiple_values-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="return_multiple_values-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "def powers(x, y):\n" +
    "    pow1 = x ** y\n" +
    "    pow2 = y ** x\n" +
    "    return pow1, pow2\n" +
    "ans1, ans2 = powers(4, 3)\n" +
    "print(f&quot;x^y is {ans1}&quot;)print(f&quot;y^x is {ans2}&quot;)\n" +
    "return pow1 #distractor\n" +
    "return pow2 #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "return_multiple_values-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "return_multiple_values-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#return_multiple_values-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#return_multiple_values-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
