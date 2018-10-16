PROJECT 1 - RED ACADEMY - DONE BY EIRIAN LYNN TA - ABOUT 20 HOURS

A. HTML + CSS:

1. General:
- For accessibility reason (some screen readers might read capitalized text letter-by-letter), text decoration is all done with css instead of HTML.
- Responsively designed using a mobile-first approach
- Optimized for 3 screen sizes: mobile, min-width: 600px and min-width: 1240px
- Shortcut icon is done using favicon.

2. Header:
- Flex. Change order of the 2nd and 3rd item when the screen is smaller than 600px
- Use "Position" to keep it at the top of the page always

3. Banner:
- Use two background images. The "flower-bkgd" is designed to be repeated horizontally, not vertically.

4. Categories:
- Flex + border + margin (minus)
- Will try Grid next time

5. Footer:
- Flex




B. JS/jQuery:

1. Incorporate “smooth scrolling” into the menu that navigates to specific headings in the page:

<script src="jquery.smooth-scroll.js"></script>


2. Incorporate an image slider using a jQuery plugin for the featured product area:

<script src="https://unpkg.com/flickity@2/dist/flickity.pkgd.min.js"></script>


3. Display an alert box that says “Thanks for subscribing!” whenever a user successfully submits the newsletter form with valid email address, otherwise they should see a message in the alert box that asks them to enter a valid email address:

$('#contact-form').submit(function() {
	var sEmail = $('#email').val();
	if (validateEmail(sEmail)) {                             
		alert('Thanks for subscribing!');
		e.preventDefault();
        } 
        else {
                alert('Please enter a valid email address');
                e.preventDefault();
        }
});
               
function validateEmail(sEmail) {
         var expr = /^(([^<>()[\]\\.,;:\s@\"]+(\.[^<>()[\]\\.,;:\s@\"]+)*)|(\".+\"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
         return expr.test(sEmail);
}

=> blank -> Please fill out this field
   does not include @ -> Please include an @ in the email address
   include @ but not a valid email adress -> Please enter a valid email adress
   a valid email address -> Thanks for subscribing!



4. Cart:
var itemCount = 0;

$('.add').click(function (){
	itemCount ++;
	$('#itemCount').html(itemCount).css('display', 'block');
}); 

$('.clear').click(function() {
	itemCount = 0;
	$('#itemCount').html('').css('display', 'none');
	$('#cartItems').html('');
}); 





