<div id="stars"></div>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
height:100vh;
overflow:hidden;
display:flex;
justify-content:center;
align-items:center;
background:linear-gradient(135deg,#0f172a,#1e3a8a,#7c3aed);
color:white;
}

#stars{
position:fixed;
width:100%;
height:100%;
top:0;
left:0;
background-image:
radial-gradient(white 1px,transparent 1px),
radial-gradient(white 1px,transparent 1px);
background-size:50px 50px,100px 100px;
animation:moveStars 30s linear infinite;
opacity:.4;
}

@keyframes moveStars{
from{transform:translateY(0);}
to{transform:translateY(-300px);}
}

.card{
position:relative;
width:90%;
max-width:420px;
padding:30px;
border-radius:25px;
background:rgba(255,255,255,.12);
backdrop-filter:blur(18px);
text-align:center;
box-shadow:0 0 30px rgba(255,255,255,.15);
z-index:2;
}

h1{
font-size:32px;
margin-bottom:15px;
}

#countdown{
font-size:26px;
font-weight:bold;
margin:20px 0;
}

button{
padding:14px 25px;
border:none;
border-radius:12px;
font-size:18px;
cursor:pointer;
background:#ff4d6d;
color:white;
transition:.3s;
}

button:hover{
transform:scale(1.05);
}

.heart{
position:fixed;
font-size:20px;
animation:float 8s linear infinite;
}

@keyframes float{
0%{
transform:translateY(100vh);
opacity:0;
}
20%{opacity:1;}
100%{
transform:translateY(-120vh);
opacity:0;
}
}
