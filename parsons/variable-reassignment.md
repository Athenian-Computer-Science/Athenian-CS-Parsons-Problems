### Variable reassignment
The goal of this exercise is to switch the values of two variables: `parrot` and `badger`. Start by assigning `8` to `parrot` and `5` to `badger`. Then arrange the other blocks to switch the values of the variables. 

<div id="reassign-sortableTrash" class="sortable-code"></div> 
<div id="reassign-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="reassign-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="reassign-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "parrot = 8<br\>badger = 5\n" +
    "temp = badger\n" +
    "badger = parrot\n" +
    "parrot = temp\n" +
    "parrot = badger #distractor\n" +
    "badger = temp #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "reassign-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "trashId": "reassign-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#reassign-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#reassign-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
