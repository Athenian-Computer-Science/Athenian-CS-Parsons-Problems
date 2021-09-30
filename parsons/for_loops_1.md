### For loops
Use a for loop to count the number of times the letter "a" occurs in "capybara".

<div id="for_loops_1-sortableTrash" class="sortable-code"></div> 
<div id="for_loops_1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="for_loops_1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="for_loops_1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "count = 0\n" +
    "for i in &quot;capybara&quot;:\n" +
    "    if i == &quot;a&quot;:\n" +
    "        count += 1\n" +
    "print(count)\n" +
    "print(i) #distractor\n" +
    "count += i #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "for_loops_1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "for_loops_1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#for_loops_1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#for_loops_1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
