# Long Scrolling Website Resources
The long scrolling website is a way to tell stories and explore what can be donw with a little javascript and a lot of creativity.  Much of the code below is based on a great site created by Linda Dong called the Dangers of Fracking which is archived here https://web.archive.org/web/20160610065039/http://www.dangersoffracking.com/


```
	<div id="wrapper">
```	
The wrapper creates a large "canvass" area that allows you to layout your images. 
```
html, body {
margin: 0;
padding: 0;
}
```
The body and html have margins and padding - in this case you want to turn them off so you don't have the default gap.

```

body {
background: #eaecea;
font-family: helvetica;
}
body a {
	text-rendering: optimizeLegibility;
	}
```
`body` gets a default color and font and the anchor tags get better [text-rendering](https://developer.mozilla.org/en-US/docs/Web/CSS/text-rendering).
```
#wrapper {
overflow: hidden;
min-width: 800px;
}
```
Now the `#wrapper` hides everything that sits outside the container.  It also sets a minimum width.  You could also specify a max-width to keep things aligned. Find all the [details here](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference).

```	
	<!-- Sky -->
	<section id="sky">
			<h2>What goes in and out of</h2>
			<h1>Hydraulic<br> Fracturing</h1>
			<h3 id="title">Dive Down</h3>
		</a>
		<figure id="drop">
			<img src="Fracking/drop.png" alt=""/>
		</figure>
		
		<article id="description">
			<h3>So What is it?</h3>
			<p>Hydraulic fracturing, or <em>“fracking”</em>, is the process of drilling and 
			   injecting fluid into the ground at a high pressure in order to fracture shale 
			   rocks to release natural gas inside. 
			</p>
			<aside id="red">
				<p><em>There are more than 500,000 active natural gas wells in the US.</em></p>
			</aside>
		</article>
		
		<img id="cloud1" src="Fracking/clouds.png" alt=""  />
		<img id="cloud2" src="Fracking/clouds4.png" alt="" />
		<img id="cloud3" src="Fracking/clouds2.png" alt=""  />
		<img id="cloud4" src="Fracking/clouds3.png" alt=""  />
		<img id="cloud5" src="Fracking/clouds4.png" alt=""  />
	</section>
	<!-- Highway -->
	<section id="highway">

```
Here is a sample of some great markup that is semantic (article and sections tags) and well structured.  You can imagine what it migt look like.

Now let's look at the javascript ...
```

/*
     FILE ARCHIVED ON 18:08:11 Jun 10, 2016 AND RETRIEVED FROM THE
     INTERNET ARCHIVE ON 15:42:20 Nov 8, 2016.
     JAVASCRIPT APPENDED BY WAYBACK MACHINE, COPYRIGHT INTERNET ARCHIVE.

     ALL OTHER CONTENT MAY ALSO BE PROTECTED BY COPYRIGHT (17 U.S.C.
     SECTION 108(a)(3)).
*/
/*FRACKING JS - Linda Dong */

$(document).ready(function() {
```
The `$(document).ready(function(){ ` is a call for [JQuery](https://jquery.com/) which is needed to run this.  The `$()` is a universal selector. `$(document)` means select the document. `.ready()` asks "is the document fully loaded into the browser?". `function(){ }` is an anonymous function that runs the entire script once. 

After the document has loaded. Here is the [explanation on JQuery's site](https://learn.jquery.com/using-jquery-core/document-ready/)

```
/*Icon Collection*/

$(window).scroll(function() {

```
`$(window).scroll(function() {` This selects the window, and waits until the user starts to scroll and then runs an anonymous function. You must balance all the parenthesis and braces to make sure it can run!!!! `});` closes this block.
```	
JAVASCRIPT
	/*Droplet*/
	if ($(this).scrollTop() > 7500) { 
	    $("#toxin").css({ "position": "fixed", "top": "460px"});
	} else {
	    $("#toxin").css({ "position": "absolute", "top": "7500px" });
	}   
```
Working with JS and CSS
```
CSS
	#toxin {
	width: 36px;
	height: 46px;
	background: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/toxin.png);
	position: absolute;
	top: 7500px;
	z-index: 202;
	left: 50%;
	margin-left: -18px;
	}
```
Together with the CSS, `$(this)` selects the window which was selected above you could also write `$(window)`. `.scrollTop()` is a method for the window which tells us how far from the top of the document the beginning of the selected window is. It can do this for any selected element!.  The Documentation is here for [scrollTop](https://api.jquery.com/scrollTop/) and here for [scrollLeft](https://api.jquery.com/scrollleft/).

The `$("#toxin").css({ "position": "absolute", "top": "7500px" });` changes the CSS of the element with the id #toxin to `position: absolute` and  `top: 7500px`

The [If/Else statement](http://www.w3schools.com/js/js_if_else.asp) uses a [greater than comparison operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators#Greater_than_operator_(>)) to determine if one number is greater than another number.  in this case `scrollTop` 
aginsts the fixed value of 7500.  Because this whole thing is sitting INSIDE the `$(window).scroll()` function, the number of `.scrollTop()` is updated everytime the user scrolls the page.

So what you see above then, is an if statement that uses the vertical position as a number input and checks to see if you have scrolled more than 7500 pixels. While you are LESS than 7500 pixels (the else statement) the element with the id 

```	
	if ($(this).scrollTop() > 22320) { 
	    $("#icongas").css({ "position": "fixed", "top": "0px", "opacity": "1"});
	} else {
	    $("#icongas").css({ "position": "absolute", "top": "22320px", "opacity": "1"  });
	}  
```
Above is another example of chjanging the CSS.  This time also the opacity is changed. More [info on the .css() method](http://www.w3schools.com/jquery/jquery_css.asp) is here.

***Here is a demo on JS Bin that creates a long box and a counter which tells you the scroll top position https://jsbin.com/fajuxe/edit?html,output***

***Here is a demo on JS Bin that uses scrolling and if/else to write into the console https://jsbin.com/eraNuNA/edit?js,console,output***

***Here is a demo on JS Bin that uses scrolling to hide an object https://jsbin.com/rijomu/2/edit?html,css,output***

```
/* Parallax*/
$(window).scroll(function(){
	
	/*Clouds*/
	$("#cloud1").css({
  		top: function(index, value) {
    		return 350 - $(window).scrollTop() * 1.3;
  		}
  	});	
	
	$("#cloud2").css({
  		top: function(index, value) {
    		return 500 - $(window).scrollTop() * 1.5;
  		}
	});		
	$("#cloud3").css({
  		top: function(index, value) {
    		return 590- $(window).scrollTop() * .2;
  		}
	});
	

	$("#bubbles4").css({
  		top: function(index, value) {
    		return 15900- $(window).scrollTop() * .9;
  		}
	})
	
```

***Here is a sample of how to make things scroll at different speeds on the danger of fracking https://web.archive.org/web/20160610065039/http://www.dangersoffracking.com/***

***Here is a demo on JS Bin that uses scrolling to move a bunch of stuff  https://jsbin.com/Avipihan/edit?html,console,output***

***Here is a demo of clicking on the counter and moving the view https://jsbin.com/IVUYorU/edit?html,js,console,output***

	
```
			
	function isScrolledIntoView(elem) {
	    var docViewTop = $(window).scrollTop();
	    var docViewBottom = docViewTop + $(window).height();
	
	    var elemTop = $(elem).offset().top;
	    var elemBottom = elemTop + $(elem).height();
	
	    return ((elemBottom >= docViewTop) && (elemTop <= docViewBottom));
		}  
		
		var myelement = $('#cloud6');
		var mymessage = $('#description');
		$(window).scroll(function() {
		    if(isScrolledIntoView(myelement)) {
		        mymessage.fadeIn('500'); 
		    }
		     else {
		        mymessage.fadeOut('200')
		    }
```
Above is an example of how you can see if something has scrolled into view. Essentially you are measuring the location of the window from the top of the document start with `$(window).scrollTop();` and the height of the window with `$(window).height()` to determine the bottom location of the window. 

You now have a top and bottom cordinate, which you can test the location of an object on the page with `((elemBottom >= docViewTop) && (elemTop <= docViewBottom))`.  If the item I am concerned with is visible to the user, do something cool ` if(isScrolledIntoView(myelement)) {mymessage.fadeIn('500');`.

***Here is a JSBin here to show the version in action.https://jsbin.com/qoxeni/edit?html,js,console,output***

```
section#ground9 {
position: relative;
background-image: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks.png), -webkit-linear-gradient(top,#7a5c35, #9f8750);
background-image: #7a5c35 url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks.png);
background-image: url(/web/20160610180812/http://dangersoffracking.com/Fracking/rocks.png), url(/web/20160610180812/http://www.dangersoffracking.com/svg/ground9.svg); /* added */
height: 1000px;
width: 100%;
}	
```
One last cool thing is the way you can build the content of each "frame".  You can use `position:relative/fixed/absolute; and z-index:1...1000` to stack elements on top of each other  - [more about z-index](http://www.w3schools.com/cssref/tryit.asp?filename=trycss_zindex) is here. 

You can also [layer backgound images ontop of each other and position them all in one box!](http://www.w3schools.com/css/css3_backgrounds.asp)  here is a demo of that. using backgound-repeat and [using SVG(vector graphics)](https://css-tricks.com/using-svg/)  you can save a lot of space on big graphics and make them all move independent of each other.

***Here is a nice video from the folks at TreeHouse https://teamtreehouse.com/library/multiple-background-images-with-css***

***You can even [animate SVG](https://www.smashingmagazine.com/2014/11/styling-and-animating-svgs-with-css/) files***
