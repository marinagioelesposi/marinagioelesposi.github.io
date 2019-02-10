+++
title = "Contact us"
weight = 6
menuname = "Contact us / RSVP"
draft = false
+++

<form id="contactform" method="post" action="https://formspree.io/marinagioelesposi@gmail.com">
	<div class="field half first">
		<input type="text" name="name" id="name" placeholder="Name"/>
	</div>
	<div class="field half">
		<input type="email" id="email" name="email" placeholder="Email">
	</div>
	<div class="field">
		<textarea name="message" id="message" rows="4" placeholder="Message"></textarea>
	</div>
	<ul class="actions">
		<li><input type="submit" value="Send message" class="special" /></li>
		<li><input type="reset" value="Reset" /></li>
	</ul>
	<input type="hidden" name="_next" value="?sent#formspree" />
	<input type="hidden" name="_subject" value="Subject for your mail like new message" />
	<input type="text" name="_gotcha" style="display:none" />
</form>
<span id="contactformsent">Sent succesffully! <br>
Thank you for getting in touch!<br>
</span>
<form id="contactform2">
	<ul class="actions">
		<li><input type="submit" value="Send a new mesage" class="special" /></li>
	</ul>
	<input type="hidden" name="_next" value="#formspree" />
	<input type="text" name="_gotcha" style="display:none" />
</form>




<script>
$(document).ready(function($) { 
    $(function(){
        if (window.location.search == "?sent") {
        	$('#contactform').hide();
			$('#contactformsent').show();
			$('#contactform2').show();
        } else {
			$('#contactformsent').hide();
			$('#contactform').show();
			$('#contactform2').hide();
        }
    });
});
</script>
