# Long Scrolling Website Resources
The long scrolling website is a way to tell stories and explore what can be donw with a little javascript and a lot of creativity.  The code below is based on a great site created by Linda Dong called the Dangers of Fracking which is archived here https://web.archive.org/web/20160610065039/http://www.dangersoffracking.com/


```
	<div id="wrapper">
````	
	The wrapper creates a large "canvass" area that allows you to layout your images. 
````
html, body {
margin: 0;
padding: 0;
}

body {
background: #eaecea;
font-family: helvetica;
}

	body a {
	text-rendering: optimizeLegibility;
	}

#wrapper {
overflow: hidden;
min-width: 800px;
}
````



````	
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
	
	<figure id ="mrtruck" class="truckleft"><img src="Fracking/truck.png" alt="" /></figure>
	
	<!-- Highway -->
	<section id="highway">
	</div>
```	
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

/*Icon Collection*/

$(window).scroll(function() {
	
	/*Droplet*/
	if ($(this).scrollTop() > 7500) { 
	    $("#toxin").css({ "position": "fixed", "top": "460px"});
	} else {
	    $("#toxin").css({ "position": "absolute", "top": "7500px" });
	}      
	if ($(this).scrollTop() > 15200) { 
	    $("#gas").css({ "position": "fixed", "top": "335px"});
	} else {
	    $("#gas").css({ "position": "absolute", "top": "15180px" });
	}   
	
	/* Tokens */
	if ($(this).scrollTop() > 3850) { 
	    $("#icontruck").css({ "position": "fixed", "top": "0px", "opacity": "1"});
	} else {
	    $("#icontruck").css({ "position": "absolute", "top": "3850px", "opacity": ".4" });
	}     
	if ($(this).scrollTop() > 4720) { 
	    $("#iconwater").css({ "position": "fixed", "top": "0px", "opacity": "1"});
	} else {
	    $("#iconwater").css({ "position": "absolute", "top": "4720px", "opacity": ".4"  });
	}     
	if ($(this).scrollTop() > 7610) { 
	    $("#icontoxic").css({ "position": "fixed", "top": "0px", "opacity": "1"});
	} else {
	    $("#icontoxic").css({ "position": "absolute", "top": "7610px", "opacity": ".4"  });
	}
	if ($(this).scrollTop() > 6250) { 
	    $("#iconfluid2").css({ "position": "fixed", "top": "0px", "opacity": "1"});
	} else {
	    $("#iconfluid2").css({ "position": "absolute", "top": "6250px", "opacity": ".4"  });
	}  
	if ($(this).scrollTop() > 17100) { 
	    $("#iconmethane").css({ "position": "fixed", "top": "0px", "opacity": "1"});
	} else {
	    $("#iconmethane").css({ "position": "absolute", "top": "17100px", "opacity": ".4"  });
	}  
	if ($(this).scrollTop() > 18640) { 
	    $("#iconnowater").css({ "position": "fixed", "top": "0px", "opacity": "1"});
	} else {
	    $("#iconnowater").css({ "position": "absolute", "top": "18640px", "opacity": ".4"  });
	}  
	if ($(this).scrollTop() > 18640) { 
	    $("#iconhealth").css({ "position": "fixed", "top": "0px", "opacity": "1"});
	} else {
	    $("#iconhealth").css({ "position": "absolute", "top": "18640px", "opacity": ".4"  });
	}  
	if ($(this).scrollTop() > 20600) { 
	    $("#iconfluid").css({ "position": "fixed", "top": "0px", "opacity": "1"});
	} else {
	    $("#iconfluid").css({ "position": "absolute", "top": "20600px", "opacity": ".4"  });
	}  
	if ($(this).scrollTop() > 21600) { 
	    $("#iconair").css({ "position": "fixed", "top": "0px", "opacity": "1"});
	} else {
	    $("#iconair").css({ "position": "absolute", "top": "21600px", "opacity": ".4"  });
	} 
	if ($(this).scrollTop() > 22320) { 
	    $("#icongas").css({ "position": "fixed", "top": "0px", "opacity": "1"});
	} else {
	    $("#icongas").css({ "position": "absolute", "top": "22320px", "opacity": "1"  });
	}  
	                   
});


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
	$("#cloud4").css({
  		top: function(index, value) {
    		return 420- $(window).scrollTop() * .5;
  		}
	});	
	$("#cloud5").css({
  		top: function(index, value) {
    		return 775- $(window).scrollTop() * 1.7;
  		}
	});	
	$("#cloud6").css({
  		top: function(index, value) {
    		return 1550- $(window).scrollTop() * .6;
  		}
	});	
	$("#cloud7").css({
  		top: function(index, value) {
    		return 1050- $(window).scrollTop() * .4;
  		}
	});	
	$("#cloud8").css({
  		top: function(index, value) {
    		return 1800- $(window).scrollTop() * 1.3;
  		}
	});	
	$("#cloud9").css({
  		top: function(index, value) {
    		return 2500- $(window).scrollTop() * 1.1;
  		}
	});
	
	/*Road*/
	$("#house").css({
  		top: function(index, value) {
    		return 4500- $(window).scrollTop() * 1.1;
  		}
	});
	$("#house2").css({
  		top: function(index, value) {
    		return 7000- $(window).scrollTop() * 1.1;
  		}
	});
	$("#house3").css({
  		top: function(index, value) {
    		return 8600- $(window).scrollTop() * 1.1;
  		}
	});
	
	/*Rig*/
	$("#clouda").css({
  		top: function(index, value) {
    		return 3400- $(window).scrollTop() * .4;
  		}
	});
	$("#cloudb").css({
  		top: function(index, value) {
    		return 9400- $(window).scrollTop() * 1.3;
  		}
	});
	$("#cloudc").css({
  		top: function(index, value) {
    		return 2500- $(window).scrollTop() * .3;
  		}
	});
	$("#cloudc2").css({
  		top: function(index, value) {
    		return 10500- $(window).scrollTop() * 1.3;
  		}
	});
	
	/*Aquifer*/
	$("#bubbles").css({
  		top: function(index, value) {
    		return 10400- $(window).scrollTop() * .6;
  		}
	});
	$("#bubbles2").css({
  		top: function(index, value) {
    		return 5200- $(window).scrollTop() * .3;
  		}
	});
	$("#bubbles3").css({
  		top: function(index, value) {
    		return 6100- $(window).scrollTop() * .3;
  		}
	});
	$("#bubbles4").css({
  		top: function(index, value) {
    		return 15900- $(window).scrollTop() * .9;
  		}
	})
	$("#cloudd").css({
  		top: function(index, value) {
    		return 7200- $(window).scrollTop() * .3;
  		}
	});
	$("#cloude").css({
  		top: function(index, value) {
    		return 22200- $(window).scrollTop() * 1.0;
  		}
	});
	$("#cloudf").css({
  		top: function(index, value) {
    		return 17400- $(window).scrollTop() * .8;
  		}
	});
		
});	
	
				
/*Disappear*/ 
			
	$(window).scroll(function() {
		if(isScrolledIntoView('#road')) {
			$("#drop").css({"display": "none"});
			}
		else {
			$("#drop").css({"display": ""});
			}

		if(isScrolledIntoView('#pipe')) {
			$("#mrtruck").css({"display": "none"});
			}
		else {
			$("#mrtruck").css({"display": ""});
			}
	
		if(isScrolledIntoView('#pipe')) {
			$("#meter").css({"-webkit-transform": "rotate(0deg)"});
			}
		else {
			$("#meter").css({"-webkit-transform": "rotate(-180deg)"});
			}
	});


/*Articles*/
			
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

		var myelement1 = $('#hill');
		var mymessage1 = $('#red');
		    if(isScrolledIntoView(myelement1)) {
		        mymessage1.fadeIn('500'); 
		    }
		     else {
		        mymessage1.fadeOut('200')
		    }

		var myelement2 = $('#targettruck');
		var mymessage2 = $('#texttrucks');
		    if(isScrolledIntoView(myelement2)) {
		        mymessage2.fadeIn('500'); 
		    }
		     else {
		        mymessage2.fadeOut('200')
		    }

		var myelement3 = $('#targettruck2');
		var mymessage3 = $('#texttrucks2');
		    if(isScrolledIntoView(myelement3)) {
		        mymessage3.fadeIn('500'); 
		    }
		     else {
		        mymessage3.fadeOut('200')
		    }

		var myelement5 = $('#targetchemical');
		var mymessage5 = $('#chemicals');
		    if(isScrolledIntoView(myelement5)) {
		        mymessage5.fadeIn('500'); 
		    }
		     else {
		        mymessage5.fadeOut('200')
		    }

		var myelement7 = $('#chemicaltrigger');
		var mymessage7 = $('#chemicals2');
		    if(isScrolledIntoView(myelement7)) {
		        mymessage7.fadeIn('500'); 
		    }
		     else {
		        mymessage7.fadeOut('200')
		    }
		    
		var myelement4 = $('#pipe');
		var mymessage4 = $('#chemicals2wrapper');
		    if(isScrolledIntoView(myelement4)) {
		        mymessage4.fadeIn('500'); 
		    }
		     else {
		        mymessage4.fadeOut('200')
		    }

		var myelement8 = $('#ground3');
		var mymessage8 = $('#chemicals3');
		    if(isScrolledIntoView(myelement8)) {
		        mymessage8.fadeIn('500'); 
		    }
		     else {
		        mymessage8.fadeOut('200')
		    }
		
		var myelement9 = $('#trigger1');
		var mymessage9 = $('#chemicals4');
		    if(isScrolledIntoView(myelement9)) {
		        mymessage9.fadeIn('500'); 
		    }
		     else {
		        mymessage9.fadeOut('200')
		    }
		
		var myelement10 = $('#trigger2');
		var mymessage10 = $('#math');
		    if(isScrolledIntoView(myelement10)) {
		        mymessage10.fadeIn('500'); 
		    }
		     else {
		        mymessage10.fadeOut('200')
		    }
		var myelement11 = $('#pipecurve');
		var mymessage11 = $('#methane');
		    if(isScrolledIntoView(myelement11)) {
		        mymessage11.fadeIn('500'); 
		    }
		     else {
		        mymessage11.fadeOut('200')
		    }
		    
		var myelement12 = $('#meter');
		var mymessage12 = $('#cracks');
		    if(isScrolledIntoView(myelement12)) {
		        mymessage12.fadeIn('500'); 
		    }
		     else {
		        mymessage12.fadeOut('200')
		    }
		    
		var myelement13 = $('#trigger3');
		var mymessage13 = $('#cracks3');
		    if(isScrolledIntoView(myelement13)) {
		        mymessage13.fadeIn('500'); 
		    }
		     else {
		        mymessage13.fadeOut('200')
		    }

		var myelement14 = $('#tox2');
		var mymessage14 = $('#methane2');
		    if(isScrolledIntoView(myelement14)) {
		        mymessage14.fadeIn('500'); 
		    }
		     else {
		        mymessage14.fadeOut('200')
		    }

		var myelement15 = $('#citypipe');
		var mymessage15 = $('#citywater');
		    if(isScrolledIntoView(myelement15)) {
		        mymessage15.fadeIn('500'); 
		    }
		     else {
		        mymessage15.fadeOut('200')
		    }
		    
		var myelement16 = $('#pit1');
		var mymessage16 = $('#recovered');
		    if(isScrolledIntoView(myelement16)) {
		        mymessage16.fadeIn('500'); 
		    }
		     else {
		        mymessage16.fadeOut('200')
		    }
		var myelement17 = $('#cloudf');
		var mymessage17 = $('#voc');
		    if(isScrolledIntoView(myelement17)) {
		        mymessage17.fadeIn('500'); 
		    }
		     else {
		        mymessage17.fadeOut('200')
		    }
	});




});







/*
     FILE ARCHIVED ON 18:08:12 Jun 10, 2016 AND RETRIEVED FROM THE
     INTERNET ARCHIVE ON 15:53:47 Nov 8, 2016.
     JAVASCRIPT APPENDED BY WAYBACK MACHINE, COPYRIGHT INTERNET ARCHIVE.

     ALL OTHER CONTENT MAY ALSO BE PROTECTED BY COPYRIGHT (17 U.S.C.
     SECTION 108(a)(3)).
*/
@charset "utf-8";

/* FRACKING CSS - LINDA DONG */

/* General */

html, body {
margin: 0;
padding: 0;
}

body {
background: #eaecea;
font-family: helvetica;
}

	body a {
	text-rendering: optimizeLegibility;
	}

#wrapper {
overflow: hidden;
min-width: 800px;
}



a:link, a:visited {
text-decoration: none;
color: #ec3d2f;
padding: 0;
margin: 0;
}

	a:hover { 
	color: #fff;
	}
	
	ul a:link, ul a:visited {
	color: #fff;}
	
	ul a:hover {
	color: #ec3d2f; }
	
em {
color: #ec3d2f;
font-weight: bold;
font-style: normal;
}

ul {
list-style-type: none;
padding: 0;
margin: 0;
text-align: center;
}

hr {
border: 0px; 
height: 1px; 
background: #000;
padding: 0;
margin: 0;
}

img {
border: none;
}


h1, h2, h3, h4, h5 {
padding: 0; 
margin: 0;
text-decoration: none;
text-transform: uppercase;
-webkit-font-smoothing: antialiased;
}

hgroup {z-index: 10;}

		h1 {
		text-align: center;
		font-family: adrianna-extended-1,adrianna-extended-2, sans-serif;
		font-size: 72px;
		color: #fff;
		font-weight: 500;
		letter-spacing: 5px;
		line-height: 72px;
		}
			
		h2 {
		text-align: center;
		font-family:baskerville, caslon, serif;
		color: #111;
		text-transform: none;
		font-weight: 100;
		font-size: 26px; 
		font-style: italic;
		margin: 0 0 10px 0;
		}
	
		h3 {
		position:relative;
		text-align: center;
		font-family: adrianna-extended-1,adrianna-extended-2, sans-serif;
		font-size: 20px;
		color: #111;
		font-weight: 500;
		letter-spacing: 1px;
		}
			
			h3#title {
			font-size: 20px;
			color: #111;
			margin: 70px 0 0 0;
			z-index: 1000;
			}
			
			h3.white {color: #fff;}
		
		h4 {
		text-align: center;
		font-family: adrianna-extended-1,adrianna-extended-2, sans-serif;
		font-size: 20px;
		color: #111;
		font-weight: 500;
		letter-spacing: 1px;
		background: #ec3d2f;
		padding: 10px 20px;
		}
		
section {
padding: 10px 0;
margin: 0;
}

article {
position: absolute;
background: #fff;
padding: 30px;
left: 50%;
text-align: center;
z-index: 900;
}

p { 
font-size: 19px; 
line-height: 26px;
font-family: "ff-tisa-web-pro-1","ff-tisa-web-pro-2", Georgia, Times; 
font-weight: normal;
text-rendering: optimizeLegibility;
-webkit-font-smoothing: antialiased;
}

/*Tokens*/

.icon {
position: absolute;
z-index: 1000;
margin-top:15px;
}

	#icontruck {right: 40px; }
	
	#iconwater {right: 80px; }
	
	#icontoxic {right: 160px; }
	
	#iconfluid2 {right: 120px; }
	
	#iconmethane {left: 40px; }
	
	#iconnowater {left: 80px; }
	
	#iconhealth{left: 120px;}
	
	#iconfluid {left: 160px; }
	
	#iconair {left: 200px; }
	
	#icongas {left: 50%; margin-left: -14px;  }


figure#drop {
position: fixed;
top: 380px;
left: 50%;
margin-left:-36px;
z-index:201;
}

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

/* 1. Sky */

section#sky {
background:url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/noise.png) #79c5ce;
height: 1600px;
width: 100%;
padding: 200px 0 0 0;
position: relative; 
z-index:200;
}

	article#description {
	margin: 400px 0 0 -242px;
	width: 425px;
	border: 1px #fff solid;
	outline: 10px #222 solid;
	background: #222;
	color: #fff;
	}
	
		article#description h3 {color: #fff;}
		
		aside {
		position: relative;
		margin: 50px auto 30px;
		height: 42px;
		width: 350px;
		text-align: center;
		z-index:10;
		}	

	#cloud1 {
	position: absolute;
	top: 350px; 
	right: -20px;
	}
	
	#cloud2 {
	position: absolute;
	top: 500px;
	left: -400px;
	}
	
	#cloud3 {
	position: absolute;
	top: 590px;
	left: -130px;
	-webkit-transform: rotate(180deg);
	-ms-transform: rotate(180deg);
	-moz-transform: rotate(180deg);
	transform: rotate(180deg);}
	
	#cloud4 {
	position: absolute;
	top: 420px;
	right: 50px;}
	
	#cloud5 {
	position: absolute;
	top: 775px;
	right: -300px;}
	
	#cloud6 {
	position: absolute;
	top: 1550px;
	left: 150px;}
	
	#cloud7 {
	position: absolute;
	top: 1050px;
	right: 20px;
	-webkit-transform: rotate(-5deg);
	-ms-transform: rotate(-5deg);
	-moz-transform: rotate(-5deg);
	transform: rotate(-5deg);}
	
	#cloud8 {
	position: absolute;
	top: 1800px;
	left: 350px;}
	
	#cloud9 {
	position: absolute;
	top: 2500px;
	right: 10px;}

/* 2. Highway */
	
section#highway {
position: relative;
background: #8ba341 url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/noise.png);
height: 3400px;
width: 100%;
padding-top: 800px;
}

	article#texttrucks {
	margin: 1175px 0 0 90px;
	width: 310px;
	opacity: .9;
	border: 1px #111 solid;
	outline: 10px #fff solid;
	}
	
	article#texttrucks2 {
	margin: 2100px 0 0 290px;
	width: 320px;
	opacity: .9;
	padding: 20px 15px;
	border: 1px #111 solid;
	outline: 10px #fff solid;
	}
	
		#city {
		position: absolute;
		top:0;
		left: 50%;
		margin: -275px 0 0 -373px;
		z-index:201;
		}
	
		#hill {
		position: absolute;
		top: 0;
		background: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/hill.png) repeat-x;
		margin: -150px 0 0 0;
		width: inherit;
		height: 130px;
		z-index:200;
		}
		
		#hill2 {
		position: absolute;
		top: 0;
		left: 50%;
		margin: -100px 0 0 -1050px;
		z-index: 1;
		z-index:201;
		}
		
		#hill3 {
		position: absolute;
		top: 0;
		left: 50%;
		margin: -100px 0 0 250px;
		z-index: 1;
		z-index:201;
		}
		

	#mrtruck {
	position: fixed;
	top: 200px;
	z-index: 101;
	width: 221px;
	height: 470px;
	left: 50%;
	margin-left: -200px;
	}

	
		.truckright {
		position: relative;
		width: 221px;
		height: 470px;
		left: 50%;
		z-index: 110;
		margin: 0 0 100px 35px;
		}
	
		#targettruck {margin: 400px 0 50px 35px;}
		
	#roadstart {
	position:absolute;
	top:0;
	left: 50%;
	margin-left: -250px;
	z-index:200;
	background: #8ba341 url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/noise.png);
	}
	
		#bridge {
		position: absolute;
		width: 100%;
		height: 300px;
		top:280px;
		z-index: 201;
		background:url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/noise.png) #7d9338;
		}
		
		#tunneltop {
		position: absolute;
		top:240px;
		z-index: 202;
		left: 50%;
		margin-left: -408px;
		}
		
		#tunnel {
		position: absolute;
		top: 520px;
		z-index:202;
		left: 50%;
		margin-left: -373px;}
		
		
		#tunnel2 {
		position: absolute;
		top: 565px;
		z-index: 0;
		background:url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/noise.png) #7d9338;
		width: 100%;
		height: 100px;
		}
	
	#road {
	position: absolute;
	top: 550px;
	left: 50%;
	margin-left: -250px;
	background: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/road.png) repeat;
	height:5000px;
	width: 500px;
	z-index:100;
	}
	
		#house {
		position: absolute;
		top: 1000px;
		left: 50%;
		margin-left: 400px;
		z-index: 200;
		}
		
		#house2 {
		position: absolute;
		top: 2000px;
		width: 100px;
		left:50%;
		margin-left: -650px; 
		height: 100px;
		z-index: 200;
		}
		
		#house3 {
		position: absolute;
		top: 3400px;
		width: 100px;
		left:50%;
		margin-left: -650px; 
		height: 100px;
		z-index: 200;
		}
		
	#dirtroad {
	position:absolute;
	top: 3950px;
	left: 50%;
	margin-left: -250px;
	background:url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/dirtroad.png) repeat;
	height: 500px;
	width: 500px;
	z-index: 100;
	}
	
/* 3. Fracking Site */
				
section#fracksite {
position: relative;
background: #8ba341 url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/noise.png);
height: 1110px;
width: 100%;
}

	article#chemicals {
	background: #111;
	margin: 300px 0 0 -225px;
	width: 400px;
	opacity: .9;
	text-align: center;
	border: 1px #fff solid;
	outline: 10px #111 solid;
	color: #fff;
	}
	
	#site {
	position: absolute; 
	top: 0px;
	z-index: 200;
	left: 50%;
	margin-left: -665px;
	padding-top: 20px;
	}
	
		#sitecontain {
		background:url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/dirtroad.png) repeat;
		position: absolute;
		top: 0;
		width: 1420px;
		height: 1110px;
		left: 50%;
		margin-left: -690px;
		z-index: 100;
		}
		
		#targetchemical {
		position: relative; 
		top:800px;}

/* 4. Rig */

section#ground {
position: relative;
background: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/noise.png) #92cbd3;
height: 1100px;
width: 100%;
z-index: 200;
top: -25px;
margin-bottom: -25px;
}

	article#chemicals2 {
	margin: 550px 0 0 -195px;
	width: 330px;
	text-align: center;
	opacity: .9;
	border: 1px #111 solid;
	outline: 10px #fff solid;
	}
	
	#arrow {
	position: absolute;
	top: 0;
	left: 50%;
	margin-left: -121px;
	z-index:210;
	}

	#rig {
	position: absolute;
	left: 50%;
	margin-left: -255px;
	top: 306px;
	z-index: 350;
	}
		
		#clouda {
		position: absolute;
		top: 500px; 
		left: 50%;
		margin-left: 300px;
		z-index: 300;
		}
		
		#cloudb {
		position: absolute;
		top: 650px;
		left: 50%;
		margin-left: -300px;
		z-index:300;
		}
		
		#cloudc {
		position: absolute;
		top: 250px;
		left: 50%;
		margin-left: -900px;
		z-index: 300;
		}
		
		#cloudc2 {
		position: absolute;
		top: 700px;
		left: 50%;
		margin-left: -50px;
		z-index: 300;
		}
	
	hgroup#toxinlist1 {
	position: absolute; 
	left: 50%;
	z-index: 400;
	margin-top: 525px;
	width: 300px;
	margin-left: -550px;
	}
	
	hgroup#toxinlist2 {
	position: absolute; 
	left: 50%;
	z-index: 400;
	margin-top: 525px;
	width: 350px;
	margin-left: 250px;
	}
		.redleft {
		position: relative;
		text-align: left;
		clear: both;
		float: left;
		margin-bottom: 30px;}
		
		.redright {
		position: relative;
		text-align: right;
		clear: both;
		float: right;
		margin-bottom: 30px;
		}
		
		#chemicaltrigger {
		position: absolute;
		top: 600px;
		}

/* 5. Ground Levels*/
		
section#ground2 {
position: relative;
background-image: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks.png), -webkit-linear-gradient(top, #9f8750, #7a5c35);
background-image: #9f8750, url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks.png);
background-image: url(/web/20160610180812/http://dangersoffracking.com/Fracking/rocks.png), url(/web/20160610180812/http://www.dangersoffracking.com/svg/ground2.svg); /* added */
height: 1050px;
width: 100%;
z-index: 199;
}
	article#chemicals3 {
	margin: 525px 0 0 -200px;
	width: 380px;
	padding: 20px 25px;
	text-align: center;
	opacity: 1;
	border: 1px #111 solid;
	outline: 10px #fff solid;}
		
	figure#pipe {
	position: relative;
	left: 50%;
	margin:-10px 0 0 -55px;
	width: 90px; 
	height: 14000px;
	background: -webkit-linear-gradient(right,#333, #111);
	background: url(/web/20160610180812/http://www.dangersoffracking.com/svg/pipe2.svg); /* added */
	z-index: 199;
	border-left: 10px #cfc9be solid;
	border-right: 10px #cfc9be solid;
	}

	#trigger3 {
	position:absolute;
	left: 50%;
	height: 500px;
	top: 6200px;
	margin: 0 0 0 95px ;
	z-index: 200;
	}


section#ground3 {
position: relative;
background-image: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks.png), -webkit-linear-gradient(top, #7a5c35, #564229);
background-image: #7a5c35, url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks.png);
background-image: url(/web/20160610180812/http://dangersoffracking.com/Fracking/rocks.png), url(/web/20160610180812/http://www.dangersoffracking.com/svg/ground3.svg); /* added */
height: 1220px;
width: 100%;

}

section#ground4 {
position: relative;
background-image: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks.png), -webkit-linear-gradient(top,#564229, #41311c);
background-image: #564229 url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks.png);
background-image: url(/web/20160610180812/http://dangersoffracking.com/Fracking/rocks.png), url(/web/20160610180812/http://www.dangersoffracking.com/svg/ground4.svg); /* added */
height: 1500px;
width: 100%;
}
	
	article#chemicals4 {
	margin: 425px 0 0 -270px;
	width: 480px;
	text-align: center;
	opacity: .9;
	border: 1px #111 solid;
	outline: 10px #fff solid;
	}
	
		aside#math {
		margin: 20px 0 30px 0;
		width: 480px;
		height: 130px;
		}
		
		#chemicals4 b {
		font-size: 32px;
		}
		
		#chemicals4 em {
		font-size: 30px;
		line-height: 36px;}
		
	#trigger1 {
	position: absolute; 
	top: 950px;
	}
	
	#trigger2 {
	position: absolute;
	top: 1200px;
	}

section#aquifer {
position: relative;
background: #30747e url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/curve.png);
height: 1400px;
width: 100%;
}

section#ground5 {
position: relative;
background-image: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks2.png), -webkit-linear-gradient(top,#41311c, #322515);
background-image: #41311c url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks2.png);
background-image: url(/web/20160610180812/http://dangersoffracking.com/Fracking/rocks2.png), url(/web/20160610180812/http://www.dangersoffracking.com/svg/ground5.svg); /* added */
height: 850px;
width: 100%;
}

	article#methane {
	margin: 400px 0 0 -265px;
	width: 470px;
	text-align: center;
	opacity: .9;
	border: 1px #111 solid;
	outline: 10px #fff solid;
	}

/* 6. Center of Gravity  */
	
section#ground6 {
position: relative;
background-image:  url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks2.png), -webkit-gradient(linear, 0% 0%, 0% 100%, from(#322515), to(#41311c), color-stop(.5,#322515));
background-image: #322515 url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks2.png);
background-image: url(/web/20160610180812/http://dangersoffracking.com/Fracking/rocks2.png), url(/web/20160610180812/http://www.dangersoffracking.com/svg/ground6.svg); /* added */
height: 1300px;
width: 100%;
top: -20px;
z-index: 200;
padding-bottom: 0;
}

	figure#pipecurve {
	position: absolute;
	left: 50%;
	top:0px;
	margin: -30px 0 0 -55px; 
	z-index: 202;
	}
		
		#cracks {
		position:absolute;
		left: 50%;
		top: 110px;
		margin: -4px 0 0 -5px ;
		z-index: 201;}
		
		#cracks2 {
		position:absolute;
		left: 50%;
		top: 660px;
		margin-left:-625px;
		z-index: 201;
		-webkit-transform: rotate(-180deg);
		-ms-transform: rotate(-180deg);
		-moz-transform: rotate(-180deg);
		transform: rotate(-180deg);}
		
		#cracks3 {
		position:absolute;
		left: 50%;
		top: 5570px;
		margin: 0 0 0 100px ;
		z-index:202;
		-webkit-transform: rotate(-180deg);
		-ms-transform: rotate(-180deg);
		-moz-transform: rotate(-180deg);
		transform: rotate(-180deg);
		}
		
		#cracks4 {
		position:absolute;
		left: 50%;
		top: 1290px;
		margin-left:-725px;
		z-index: 201;
		}

	#meter {
	position: absolute;
	z-index: 201;
	left: 50%;
	margin-left: -80px;
	width: 160px;
	height: 160px;
	top: 600px;
	background:url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/meter.png); 
	}
	
		#ground6 h3 {margin-top: 70px;}
		
	figure#pipecurve2 {
	position: absolute;
	left: 50%;
	top: 1170px;
	margin-left: -665px; 
	z-index: 500;
	-webkit-transform: rotate(-180deg);
	-ms-transform: rotate(-180deg);
	-moz-transform: rotate(-180deg);
	transform: rotate(-180deg);
	}
	
/* 7. Going up */
	
section#ground7 {
position: relative;
background-image: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks2.png), -webkit-linear-gradient(top,#41311c, #564229);
background-image: #41311c url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks2.png);
background-image: url(/web/20160610180812/http://dangersoffracking.com/Fracking/rocks2.png), url(/web/20160610180812/http://www.dangersoffracking.com/svg/ground7.svg); /* added */
height: 1000px;
width: 100%;
top: -20px;
}
	
	#gas {
	position: absolute;
	left: 50%;
	margin-left: -35px;
	}
	
/* 8. Aquifer */

section#aquifer2 {
position: relative;
background: #30747e url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/curve.png);
height: 1300px;
width: 100%;
top: -20px;
}

	article#methane2 {
	margin: 400px 0 0 -265px;
	width: 470px;
	text-align: center;
	opacity: .9;
	border: 1px #111 solid;
	outline: 10px #fff solid;
	}
	
		#tox {
		position: absolute; 
		left: 50%;
		top: 150px;
		margin-left: 320px;
		-webkit-transform: rotate(-20deg);
		-ms-transform: rotate(-20deg);
		-moz-transform: rotate(-20deg);
		transform: rotate(-20deg);
		}
		
		#tox2 {
		position: absolute; 
		left: 50%;
		top: 450px;
		margin-left: -500px;
		-webkit-transform: rotate(45deg);
		-ms-transform: rotate(45deg);
		-moz-transform: rotate(45deg);
		transform: rotate(45deg);
		}
		
		#tox3 {
		position: absolute; 
		left: 50%;
		top: 1000px;
		margin-left: 420px;
		-webkit-transform: rotate(60deg);
		-ms-transform: rotate(60deg);
		-moz-transform: rotate(60deg);
		transform: rotate(60deg);
		}
		
		#bubbles {
		position: absolute; 
		left: 50%;
		top: 170px;
		margin-left: -550px;
		-webkit-transform: rotate(-30deg);
		-ms-transform: rotate(-30deg);
		-moz-transform: rotate(-30deg);
		transform: rotate(-30deg);
		}
		
		#bubbles2 {
		position: absolute; 
		left: 50%;
		top: 500px;
		margin-left: 450px;
		}
		
		#bubbles3 {
		position: absolute; 
		left: 50%;
		top: 800px;
		margin-left: -600px;
		-webkit-transform: rotate(180deg);
		-ms-transform: rotate(180deg);
		-moz-transform: rotate(180deg);
		transform: rotate(180deg);
		}
		
		#bubbles4 {
		position: absolute; 
		left: 50%;
		top: 900px;
		margin-left: 550px;
		-webkit-transform: rotate(60deg);
		-ms-transform: rotate(60deg);
		-moz-transform: rotate(60deg);
		transform: rotate(60deg);
		}

/* 9. Going Up Again */

section#ground8 {
position: relative;
background-image: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks.png), -webkit-linear-gradient(top,#564229, #7a5c35);
background-image: #564229 url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks.png);
background-image: url(/web/20160610180812/http://dangersoffracking.com/Fracking/rocks.png), url(/web/20160610180812/http://www.dangersoffracking.com/svg/ground8.svg); /* added */
height: 1200px;
width: 100%;
margin-top: -20px;
}

	article#citywater {
	margin: 300px 0 0 -265px;
	width: 470px;
	text-align: center;
	opacity: .9;
	border: 1px #111 solid;
	outline: 10px #fff solid;
	}
	
	#citypipe {
	position: absolute; 
	left: 0;
	top: 0;
	}
	
		#tothecity {
		background:#ec3d2f;
		position: absolute;
		left: 200px;
		top: 425px;
		padding: 5px 10px;
		opacity: .9;
		}

section#ground9 {
position: relative;
background-image: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks.png), -webkit-linear-gradient(top,#7a5c35, #9f8750);
background-image: #7a5c35 url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks.png);
background-image: url(/web/20160610180812/http://dangersoffracking.com/Fracking/rocks.png), url(/web/20160610180812/http://www.dangersoffracking.com/svg/ground9.svg); /* added */
height: 1000px;
width: 100%;
}

section#ground10 {
position: relative;
background: #9f8750 url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/rocks.png);
height: 900px;
width: 100%;
}
	
	article#recovered {
	margin: 300px 0 0 -245px;
	width: 430px;
	text-align: center;
	opacity: .9;
	border: 1px #111 solid;
	outline: 10px #fff solid;
	}

/* Resurfacing */

section#ground11 {
position: relative;
background: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/noise.png) #92cbd3;
height: 1100px;
width: 100%;
z-index: 200;
top: -25px;
margin-bottom: -25px;
}

	article#voc {
	margin: 400px 0 0 -265px;
	width: 450px;
	text-align: center;
	opacity: .9;
	border: 1px #111 solid;
	outline: 10px #fff solid;
	}


	#rig2 {
	position: absolute;
	left: 50%;
	margin-left: -255px;
	top: -21px;
	z-index: 350;
	-webkit-transform: rotate(-180deg);
	-ms-transform: rotate(-180deg);
	-moz-transform: rotate(-180deg);
	transform: rotate(-180deg);
	}
		
		#pit1 {
		position: absolute; 
		top: -78px; 
		left: 60px;
		opacity: .9;
		}
		
		#pit2 {
		position: absolute; 
		top: -78px; 
		right: 60px;
		-webkit-transform: scaleX(-1);
		-ms-transform: scaleX(-1);
		-moz-transform: scaleX(-1);
		transform: scaleX(-1);
		opacity: .9;
		}
			
		#cloudd{
		position: absolute;
		top: 500px; 
		left: 50%;
		margin-left: 300px;
		z-index: 300;
		-webkit-transform: rotate(-180deg);
		-ms-transform: rotate(-180deg);
		-moz-transform: rotate(-180deg);
		transform: rotate(-180deg);
		}
		
		#cloude {
		position: absolute;
		top: 650px;
		left: 50%;
		margin-left: -300px;
		z-index:300;
		-webkit-transform: rotate(-180deg);
		-ms-transform: rotate(-180deg);
		-moz-transform: rotate(-180deg);
		transform: rotate(-180deg);
		}
		
		#cloudf {
		position: absolute;
		top: 250px;
		left: 50%;
		margin-left: -900px;
		z-index: 300;
		-webkit-transform: rotate(-180deg);
		-ms-transform: rotate(-180deg);
		-moz-transform: rotate(-180deg);
		transform: rotate(-180deg);
		}
	
	#tox4 {
	position: absolute; 
	left: 50%;
	top: 150px;
	margin-left: 320px;
	-webkit-transform: rotate(-20deg);
	-ms-transform: rotate(-20deg);
	-moz-transform: rotate(-20deg);
	transform: rotate(-20deg);
	}
	
	#tox5 {
	position: absolute; 
	left: 50%;
	top: 450px;
	margin-left: -500px;
	-webkit-transform: rotate(45deg);
	-ms-transform: rotate(45deg);
	-moz-transform: rotate(45deg);
	transform: rotate(45deg);
	}
	
	#tox6 {
	position: absolute; 
	left: 50%;
	top: 700px;
	margin-left: 420px;
	-webkit-transform: rotate(60deg);
	-ms-transform: rotate(60deg);
	-moz-transform: rotate(60deg);
	transform: rotate(60deg);
	}

/* Footer */

footer {
position:relative;
background: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/noise.png) #92cbd3; 
height: 1600px; 
z-index:900;}
	
	#end {
	margin: 70px 0 0 -280px;
	width: 500px; 
	border: 1px #fff solid;
	outline: 10px #222 solid;
	background: #222;
	z-index: 300;
	color: #fff;
	padding-top: 40px;
	}
	
	#footer {
	margin: 200px 0 0 -350px;
	background: none;}

	#contact {
	margin-top: 530px; 
	width: 750px; 
	clear: both; 
	margin-left: -125px; 
	border: #fff 1px solid; 
	padding: 50px 80px 170px 80px;
	}
	
		.big {font-size: 28px;}
		
		h6 {
		bottom:10px; 
		position: absolute;
		left: 50%;
		width: 260px; 
		margin-left: -100px;
		font-weight: normal;
		}
		
		span {font-size: 12px;}
	
	ul {
	bottom: 0px; 
	position: absolute;
	width: 550px;
	left: 50%;
	margin-left:-270px; 
	margin-bottom: 90px;
	
	}
	
		li {
		font-family: helvetica, adrianna-extended-1,adrianna-extended-2, sans-serif;
		font-size: 13px;
		margin: 5px;
		}
		
		ul li a:link, ul li a:visited {color: #356169;}
		
		ul li a:hover{color: #fff;}
		
		ul h3 {font-size: 18px;}
		
	#list { 
	width: 500px; 
	position: relative; 
	margin-top: 40px;
	}
	
		#list li {margin: 10px 0;}
		
		ul#right {
		font-size: 13px; 
		position: relative;
		width: 400px;
		float: right; 
		text-align: right;  
		margin: 30px 0 0 20px;
		}
		
		ul#left {
		font-size: 13px; 
		position: relative;
		width: 400px;
		float: left; 
		text-align: left; 
		margin: 30px 0 0 -340px; 
		}
	
	#tweet a{
	margin-top: 10px;
    display: block;
    width: 300px;
    background: url(/web/20160610180812/http://www.dangersoffracking.com/Fracking/drop.png) no-repeat;
    height: 200px;
    position: absolute;
    left: 50%; 
    margin-left: -105px;
  }
  		h3#twitter:hover {
  		color: #000; }
  
  		h3#share {
  		top: 100px;
  		z-index: 100;
  		margin-left: -32px;
  		font-size: 12px;
  		width: 20px;
  		left: 50%;
  		}
  		
	  	h3#twitter {
	  	position: absolute;
	  	text-align: center;
	  	top: 75px;
	  	margin-left: -130px;
	  	width: 100px; 
	  	color: #356169;
	  	font-size: 18px;
	  	height: 50px;
	  	}
	  	
	  	h3#facebook {
	  	position: absolute;
	  	text-align: center;
	  	top: 1049px;
	  	margin-left: 400px;
	  	width: 100px; 
	  	color: #356169;
	  	font-size: 18px;
	  	height: 18px;
	  	}
	  	
	  	.fb-like {
	  	position: absolute;
	  	left: 325px;
	  	opacity: 1;
	  	z-index: 100;
	  	top: 117px;
	  	}
	  	
	.act {
	margin: 50px 0 -10px 0;
	}
  	
  	
  	#tiptip_holder {
	display: none;
	position: absolute;
	top: 0;
	left: 0;
	z-index: 99999;
}

#tiptip_holder.tip_top {
	padding-bottom: 5px;
}

#tiptip_holder.tip_bottom {
	padding-top: 5px;
}

#tiptip_holder.tip_right {
	padding-left: 5px;
}

#tiptip_holder.tip_left {
	padding-right: 5px;
}

#tiptip_content {
	font-size: 15px;
	color: #fff;
	padding: 15px 15px;
	background-color: #222;
	border-radius: 3px;
	-webkit-border-radius: 3px;
	-moz-border-radius: 3px;
	text-align: center;
}

#tiptip_arrow, #tiptip_arrow_inner {
	position: absolute;
	border-color: transparent;
	border-style: solid;
	border-width: 6px;
	height: 0;
	width: 0;
}

#tiptip_holder.tip_top #tiptip_arrow {
	border-top-color: #222;
}

#tiptip_holder.tip_bottom #tiptip_arrow {
	border-bottom-color: #222;
}

#tiptip_holder.tip_right #tiptip_arrow {
	border-right-color: #222;
}

#tiptip_holder.tip_left #tiptip_arrow {
	border-left-color: #222;
}

#tiptip_holder.tip_top #tiptip_arrow_inner {
	margin-top: -7px;
	margin-left: -6px;
	border-top-color: #222;
}

#tiptip_holder.tip_bottom #tiptip_arrow_inner {
	margin-top: -5px;
	margin-left: -6px;
	border-bottom-color: #222;
}

#tiptip_holder.tip_right #tiptip_arrow_inner {
	margin-top: -6px;
	margin-left: -5px;
	border-right-color: #222;
}

#tiptip_holder.tip_left #tiptip_arrow_inner {
	margin-top: -6px;
	margin-left: -7px;
	border-left-color: #222;
}

/* Webkit Hacks  */
@media screen and (-webkit-min-device-pixel-ratio:0) {	
	#tiptip_content {
		padding: 4px 8px 5px 8px;
		background-color: #222;
	}
	#tiptip_holder.tip_bottom #tiptip_arrow_inner { 
		border-bottom-color: #222;
	}
	#tiptip_holder.tip_top #tiptip_arrow_inner { 
		border-top-color: #222;
	}
}

#thumb {display: none;}

</style>



```
