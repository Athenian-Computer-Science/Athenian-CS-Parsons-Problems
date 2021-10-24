## Lists 1
Define a list and print selected elements.
* Be sure to define `third_animal` before `last_animal` (becuase the checker expects it, not because it matters otherwise!)

<div id="lists1-sortableTrash" class="sortable-code"></div> 
<div id="lists1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="lists1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="lists1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "animals = [&quot;cat&quot;, &quot;rabbit&quot;, &quot;iguana&quot;, &quot;buffalo&quot;, &quot;emu&quot;]\n" +
    "third_animal = animals[2]\n" +
    "last_animal = animals[-1]\n" +
    "print(third_animal, last_animal)\n" +
    "third_animal = animals[3] #distractor\n" +
    "last_animal = [5] #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "lists1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "lists1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#lists1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#lists1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
