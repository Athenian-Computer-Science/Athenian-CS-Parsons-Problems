### Basic Functions 2
Rearrange the blocks to create and run a function that accepts and adds two numbers. Pay attention to indentation and be aware of distractor blocks.

<div id="basic_function_2-sortableTrash" class="sortable-code"></div> 
<div id="basic_function_2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="basic_function_2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="basic_function_2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "def add_it(num1, num2):\n" +
    "	result = num1 + num2\n" +
    "	return result\n" +
    "user1 = int(input(&quot;First number: &quot;))<br\>user2 = int(input(&quot;Second number: &quot;))\n" +
    "answer = (add_it(user1, user2))\n" +
    "print(f&quot;{user1} + {user2} = {answer}&quot;)\n" +
    "def add_it(user1, user2): #distractor\n" +
    "user1 = input(&quot;First number: &quot;) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "basic_function_2-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "basic_function_2-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#basic_function_2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#basic_function_2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
