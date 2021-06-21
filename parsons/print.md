### 1.2 printing
<div id="hello_world-sortableTrash" class="sortable-code"></div> 
<div id="hello_world-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="hello_world-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="hello_world-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "course = &#039;Chemistry&#039;\n" +
    "print(f&quot;What is after {course}?&quot;)\n" +
    "course = Chemistry #distractor\n" +
    "&#039;Chemistry&#039; = course #distractor\n" +
    "print(&quot;What is after {course}?&quot;) #distractor\n" +
    "print f&#039;What is after {course}?&#039; #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "hello_world-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "trashId": "hello_world-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#hello_world-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#hello_world-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
