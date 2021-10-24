## Lists: Checking contents

Use the `in` keyword to check if a value is in a list.
<div id="list_check_contents-sortableTrash" class="sortable-code"></div> 
<div id="list_check_contents-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="list_check_contents-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="list_check_contents-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "names = [&quot;Anji&quot;, &quot;Briana&quot;, &quot;Carlos&quot;, &quot;Donna&quot;, &quot;Elisa&quot;]\n" +
    "get_name = input(&quot;Enter a name: &quot;)\n" +
    "if get_name in names:\n" +
    "    print(f&quot;Yes, {get_name} is in the list!&quot;)\n" +
    "else:\n" +
    "    print(f&quot;Sorry, {get_name} is not in the list.&quot;)\n" +
    "if get_name is in names: #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "list_check_contents-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "list_check_contents-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#list_check_contents-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#list_check_contents-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
