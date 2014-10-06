
assignment:

create your own site with css, html, javascript from scratch no bootstping

form  with send button 
on click event  displays data on alert(‘ ‘)

form validation 
-takes phone number 
-email
-date
cursor shows up on number form and you can tab to the next input area   (use the FOCUS method or blur method can do it also)






HTML pages may include forms, which allow user to fill out information and send it to the server.

<form method="GET" action="example/message.html">
	<p>Name: <input type="text" name="name"></p>
	<p>Message:<br><textarea name="message"></textarea></p>
	<p><button type="submit" >Send</button></p>
</form>

the code has a form with 2 fields one asking for name, and other for message, when you press send those fields are encoded into a query string, that is tacked onto the action URL, and the browser makes a GET request to that URL. 

	GET /example/message.html?name=Jean&message=Yes%3F HTTP/1.1

The start of the query is marked by a question mark. after that there are pairs of names and values corresponding to the attributes on the form field elements.  The '&' is used to seperate the pairs.

----------------------------------------------------
<input type="text"?
<script>
	document.querySelector("input").focus();
	console.log(documen.activeElement.tagName);
	// -> INPUT
	document.querySelector("input").blur();
	console.log(document.activeElement.tagName);
	//->BODY
</script>

for some pages user is expected to interact with a form immediately, using js we can focus the field when documents loaded, but HTML provides the autofocus attribute that does the same thing but lets the browser know to disable the behavior when its not appropriate like when the user has focused on someting else

<input type="text" autofocus>

you can move the focus using tab key, and using tabindex attribute.  lets focus jump from one input to another.. in ex below it goes to ok button instead of help first

<input type="text" tabindex=1><a href=".">(help)</a>
<button onclick="console.log('ok')" tabindex=2>OK</button>

by default most html elements cant be focused but use the tabindex attribute to any element to make it focusable



===============================================================
<form onsubmit="myFunction()">
	Enter name: <input type="text" id="me" name="fname" >
	<input type="submit" value="submit">
</form>


<script>
	function myFunction(){
		var data = document.getElementById("me").value();
		alert(data);
	}

</script>


















