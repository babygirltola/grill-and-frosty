# grill-and-frosty
a website to order sweet delicacies
<!-- Created by Favour -->

<!-- Created by Favour -->


<!-- Created by Favour -->

<html>
	<head>
   
  <meta name="viewport" content="width=device-width, initial-scale=1" />
		
  <link href="https://fonts.googleapis.com/css?family=Quicksand" rel="stylesheet">

<script crossorigin="anonymous" src="https://kit.fontawesome.com/3c5be74ba6.js"></script>
	
<script src="https://cdn.jsdelivr.net/npm/sweetalert2@9"></script>
	
<link href="https://cdn.rawgit.com/michalsnik/aos/2.1.1/dist/aos.css" rel="stylesheet">
	
<script src="https://cdn.rawgit.com/michalsnik/aos/2.1.1/dist/aos.js"></script>   
	   
 <title>GRILL AND FROSTY</title>
   
	</head>
   
	<body>

<!--Bar-->
<div id="header-bar">
<h1>GRILL AND FROSTY<b>.</b></h1>	
<h1 onclick="on()" class="fas fa-bars"></h1> 
</div>

<!--Slider-->
<div id="slider">
<div id="close" onclick="off()"></div>
<div id="nav-bar"><ul>
<li><h3>ABOUT US<b>.</b></h3></li>
<li><a href="#logo" onclick="off()">HOME</a></li>
<li><a href="#product" onclick="off()">GRILLS</a></li>
<li><a href="#product" onclick="off()">FROSTY</a></li>
<li><a href="#mail list" onclick="off()">MAIL LIST</a></li>
<li><a href="#reviews" onclick="off()">ABOUT US</a></li>

<!--Switch--><li style="display:flex;align-items:center;justify-content:space-between;">
<h5>NIGHT MODE</h5>  
<div id="switch" onclick="swch()">
<div id="swch" onclick="off()"></div></div><h5>LIGHT MODE</h5></li>
</ul></div></div>

<!--Logo--> 
<div id="logo"><ul data-aos="zoom-in-up">
 <li><h1>DESIRED CRAVINGS</h1></li>
 <li><h2>BON APPETITE </h2></li>
 <li><a href="#product"><button>
 ORDER NOW</button></a></li>
</ul></div>

<!--Products-->
<div id="product"></div>  
<div id="info"></div>  

<!--About-->
<div id="about"><ul><li>
<h1>SUBSCRIBE TO OUR NEWS LETTER<b>.</b></h1></li> 
<li><form>
	
<input type="email" name="Email" placeholder="Add Email" required>
	
<button type="reset">Subscribe</button></form></li>

<li style="display:flex;
justify-content:space-between;"><img src="https://i.imgur.com/bsOt1YR.png">
<img src="https://i.imgur.com/xViirw3.png">
<img src="https://i.imgur.com/La9Dayf.png">
<img src="https://i.imgur.com/OlrBYev.png">	
</li>
</ul></div>

<!--Creator-->
<div id="creator"></div>

 <script>

var products = [
{
	name: "Chicken and Chips",
	price: "4000",
	about:"Package contains:   1/3 cup ketchup	  Chicken	  Chips",
	src: "MFGhkQj"
},{
	name: "Chilled Mojito",
	price: "2500",
	about:"Package contains: 1 chilled mojito",
	src: "JlXI28K",
},{	
	name: "Sea Food Boil",
	price: "15,000",
	about:"A platter of sea food(this package contains different tyoe of sea food)",
	src: "xC4ZMtW" 
},{
	name: "Hot Dog",
	price: "3500",
	about:"This Packagecontains 3 pcs of hot dog ",
	src: "kdXHxVs" 
},{
	name: "Grilled Fish",
	price: "4000",
	about:"A whole Grilled Fish",
	src: "UczFibw" 
},{
	name: "Grilled chicken",
	price: "2500",
	about:"A whole grilled chicken",
	src: "JkTcsTp"
},{
	name: "Ocean Grill",
	price: "10500",
	about:"This platter mainly contains grilled food",
	src: "IsuoxTs"
},{
	name: "The Frosty Box",
	price: "17,000",
	about:"This package contains desserts",
	src: "q8FIKya"
},{
	name:"Steamed Buns",
	price:"3000",
	about:"This package contains buns that are steamed",
	src:"mjjN4hb"
},{
	name:"The Breakfast Tray",
	price:"10,000",
	about:"This package is a breakfast package",
	src:"YE2Zxlw"
	},{
		name:"Pasta",
		price:"6,500",
		about:"This package contains a plate of pasta",
		src:"Fr6S3l0"
	},{
		name:"Fruit Filled Smoothie",
		price:"5,000",
		about:"This package contains a bowl of fruit filled smoothie",
		src:"ZSluj3S"
		},{
		name:"Skillet Potatoes",
		price:"5,500",
		about:"This package contains a plate of skillet potatoes",
		src:"ZU3wxxY"
		},{
			name:"Toasted Bread with jam",
			price:"5,000",
			about:"This package contains Toasted bread with jam",
			src:"ZS052VV"
		},{
			name:"Coffee",
			price:"3,000",
			about:"A cup of coffee",
			src:"nC6soOl"
			},{
				name:"Ice cream",
				price:"1000",
				about:"This package comtains ice cream. It goes for N1000 per scoop",
src:"8N9oVZZ"
}
]		  


for(var p=0;p<products.length;p++){
var product =
document.getElementById("product");
product.innerHTML+=`<div class="product" 
style="background:url('https://i.imgur.com/${products[p].src}.jpg');
background-size:cover;"
onclick="info(${p})"data-aos="zoom-in-up">
<div id="info-p"><h2>${products[p].name}</h2>
<button id="order">Order ₦${products[p].price}</button></div>
</div>`  
} 

function info(num){
var info =
document.getElementById("info");
setTimeout(() => {
info.style.display="block";  
},1000);
info.innerHTML=`<div class="img-box">
<h1 class="fas fa-arrow-circle-left" onclick="back_home()"></h1><img src="https://i.imgur.com/${products[num].src}.jpg">	
</div>

<div class="info"><ul>
 
 <li><h2>Info this Product</h2></li>
 
 <li>${products[num].about}</li>
</ul></div>`	 
} 

Swal.fire({
icon: 'success',
title: 'Welcome !',
text: 'Bon apettite!.',
footer: 'Grill and Frosty'
}); 
AOS.init({duration: 1500,}) 

 </script>	
   
	</body>

</html>







<!— CSS—>




/* Created by Favour */

/* Created by Favour */


/* Created by Favour */

*{
	margin:0;
	padding:0;
	box-sizing:border-box ;
	font-family:"Quicksand";
}

b{color:#ff0055;}
a{text-decoration:none;color:#fff;}
#header-bar.active{color:#000;
background:rgba(255,255,255,.9);}
#header-bar{
	position:fixed;top:0;
	padding:2vh;
	height:9vh;
	width:100vw;
	display:flex;
	align-items:center ;
	justify-content:space-between;
	background:transparent ;
	color:#fff;
	z-index:3;
	transition-duration:1s;
}

ul li{
	padding:2vh;
	text-align:center ;
	list-style:none;
	font-weight:700;
}

#slider{
	position:fixed ;
	top:0;left:0;
	height:100vh;
	display:none;
	align-items:center ;
	justify-content:center ;
	z-index:4;color:#fff;
}

#nav-bar{
	padding:2vh;
	font-size:1.5em;
	height:100vh;width:70vw;
	background:#222;
}

#close{height:100vh;width:30vw;}

#logo{
	height:100vh;width:100vw;
	display:flex;
	align-items:center ;
	justify-content:flex-start ;   background:url("https://i.imgur.com/tkg69Zc.jpg"); 
	background-size:cover;
}

#logo li{
	color:#fff;text-align:left;
	margin:3vh;padding:0;
}

#logo button{
	height:30px;width:120px;
	font-size:1em;
	font-weight:700;
	background:#fff;	
	border:none ;outline:none;
}

#logo a{color:#000;}

#product{
	width:100vw;
	padding:10px;display:grid;	  grid-template-columns:repeat(2,1fr);  
	grid-gap:2vh;
	align-self:center;
	justify-content:center;
	background:#111;color:#fff;
	overflow:hidden ;
	text-align:center ;	
}

#product .product{
	height:40vh;
	display:flex;
	align-items:flex-end;
	justify-content:center ;
	color:#fff;
	box-shadow:0 0 2px 4px rgba(0,169,255,.35);
	transition:0.5s;
}

#product .product:hover{box-shadow:0 0 2px 2px rgba(0,169,255,.35);}
#product .product #info-p{
	width:100%;padding:1vh;
	background:rgba(0,0,0,.6);
}

#product h2{padding:5px;}

#buy{
	height:40px;width:130px;
	color:#000;
	font-weight:700;
	font-size:1.2em;
	background:#fff;
	border:none;outline:none;
	border-radius:100px;
}

#switch{
	height:5vh;width:10vh;
	display:flex;padding:1vh;
	align-items:center ;
	justify-content:flex-start;
	border-radius:50px;
	border:3px solid #fff;
}

#swch{
	height:2vh;width:2vh;
	border-radius:50%;
	box-shadow:0 0 0 3px #fff;
}

#info{
	position:fixed ;
	top:0;left:0;
	height:100vh;width:100vw;
	color:#fff;background:#222;
	z-index:5;
	display:none;
}

.img-box{
	height:40vh;width:100vw;
	display:flex;
	align-items:center ;
	justify-content:center ;
	background:#fff;color:#000;
}

#info img{
	height:40vh;width:auto ;
	background-size:cover;
}

#info h1{
	position:absolute ;
	top:2vh;left:2vh;
	background:#fff;
	border-radius:50%;
}

#about{
	width:100vw;color:#fff;
	background:#222;
	overflow:hidden ;
}

#about img{
	height:auto;width:20vw;
	background-size:cover;
	filter:invert(1);
}

#about input{
	outline:none;border:none;
	box-shadow:0 0 2px 2px #00adff;
	padding:0.5vh;font-weight:bold;	  
}

#about button{
	padding:0.5vh;
	margin-left:2vw;
	outline:none;border:none;
	background:#ff0055;
	box-shadow:0 0 2px 2px #ff0055;
	color:#fff;
	font-weight:700;
	text-transform:uppercase ;
}

/*Night Mode*/
body.swch #switch{justify-content:flex-end;}
body.swch #slider{filter:invert(1);}
body.swch #product{background:#fff;}
body.swch #product .product{
	box-shadow:0 0 4px 4px rgba(0,0,0,.35);
	transition-duration:0.5s;}body.swch #product .product:hover{
	box-shadow:0 0 1px 1px rgba(0,0,0,.35);}
body.swch #about{
	background:#fff;color:#000;}
body.swch #info{
	background:#fff;color:#000;}
body.swch #logo{
background:url("https://i.imgur.com/x1l1Cfk.jpg"); 
background-size:cover;}
body.swch #logo button{background:#ff0055;}
body.swch #logo li{color:#000;}
body.swch #about img{filter:invert(0)}
body.swch #header-bar{color:#000;}


<!— Javascript—>

// Created by Favour

// Created by Favour


// Created by Favour //

window.addEventListener("scroll",function(){var nav = 
document.getElementById("header-bar");
nav.classList.toggle("active",window.scrollY > 0);
})
function back_home(){
document.getElementById("info").style.display="none";}  
function on(){
document.getElementById("slider").style.display="flex";}
function off(){
document.getElementById("slider").style.display="none";}
function swch(){var swch= document.querySelector("body");
swch.classList.toggle("swch");}




