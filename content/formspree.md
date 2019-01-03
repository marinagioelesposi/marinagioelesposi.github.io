+++
title = "Contattaci / RSVP"
weight = 60
menuname = "Contattaci / RSVP"
draft = false
+++

<form id="contactform" method="post" action="https://formspree.io/marinagioelesposi@gmail.com">
	<div class="field half first">
		<input type="text" name="name" id="name" placeholder="Nome"/>
	</div>
	<div class="field half">
		<input type="email" id="email" name="email" placeholder="Tua email">
	</div>
	<div class="field">
		<textarea name="message" id="message" rows="6" placeholder="Messaggio"></textarea>
	</div>
	<ul class="actions">
		<li><input type="submit" value="Invia messaggio" class="special" /></li>
		<li><input type="reset" value="Cancella" /></li>
	</ul>
	<input type="hidden" name="_next" value="?sent#formspree" />
	<input type="hidden" name="_subject" value="Messaggio dal sito" />
	<input type="text" name="_gotcha" style="display:none" />
</form>

<span id="contactformsent">Inviato con successo! <br>
Ti ringraziamo per il messaggio.<br>
</span>
<form id="contactform2">
	<ul class="actions">
		<li><input type="submit" value="Invia nuovo messaggio" class="special" /></li>
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
