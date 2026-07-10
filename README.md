<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Birthday Surprise 🎂</title>

<style>
body{
margin:0;
font-family:Arial,sans-serif;
background:linear-gradient(135deg,#ff4d6d,#6a5acd);
display:flex;
justify-content:center;
align-items:center;
height:100vh;
color:white;
text-align:center;
}
.box{
background:rgba(255,255,255,.15);
padding:25px;
border-radius:20px;
backdrop-filter:blur(10px);
max-width:350px;
}
#countdown{
font-size:30px;
font-weight:bold;
margin:20px 0;
}
button{
padding:12px 25px;
border:none;
border-radius:10px;
background:#fff;
color:#ff4d6d;
font-size:18px;
cursor:pointer;
display:none;
}
</style>

</head>
<body>

<div class="box">
<h1>🎁 Surprise for Shivani</h1>
<div id="countdown"></div>

<div id="msg" style="display:none;">
<h2>🎉 Happy Birthday Shivani! 🎂</h2>
<p>
Happy Birthday, Bestie! 🎉<br>
Tu hamesha khush, successful aur pagal hi rehna.<br>
Party mat bhoolna, warna dosti temporary suspend! 😂❤️
</p>
</div>

<button id="btn">❤️ Open Gift ❤️</button>
</div>

<script>
const target=new Date("July 21, 2026 00:00:00").getTime();

setInterval(()=>{
let now=new Date().getTime();
let diff=target-now;

if(diff<=0){
document.getElementById("countdown").style.display="none";
document.getElementById("msg").style.display="block";
document.getElementById("btn").style.display="inline-block";
return;
}

let d=Math.floor(diff/(1000*60*60*24));
let h=Math.floor((diff%(1000*60*60*24))/(1000*60*60));
let m=Math.floor((diff%(1000*60*60))/(1000*60));
let s=Math.floor((diff%(1000*60))/1000);

document.getElementById("countdown").innerHTML=
`${d}d ${h}h ${m}m ${s}s`;
},1000);

document.getElementById("btn").onclick=function(){
alert("🎂 Best Gift: Stay Happy Forever ❤️");
}
</script>

</body>
</html>
