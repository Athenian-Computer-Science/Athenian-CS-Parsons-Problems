## List Slicing

Given the list of names, print the last 3 entries.

<div id="list_slicing-sortableTrash" class="sortable-code"></div> 
<div id="list_slicing-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="list_slicing-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="list_slicing-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "names = [&quot;Anji&quot;, &quot;Briana&quot;, &quot;Carlos&quot;, &quot;Donna&quot;, &quot;Elisa&quot;]\n" +
    "last_three = names[2:5]\n" +
    "print(last_three)\n" +
    "last_three = names[2:4] #distractor\n" +
    "last_three = names[3:5] #distractor\n" +
    "last_three = names[2:6] #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "list_slicing-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "list_slicing-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#list_slicing-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#list_slicing-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
