<!DOCTYPE html>
<html>
<head>
<title>Sorry Shravani ❤️</title>

<style>
body{
    margin:0;
    padding:0;
    font-family: 'Comic Sans MS', cursive;
    text-align:center;
    background: linear-gradient(45deg,#ff9a9e,#fad0c4,#fbc2eb);
    overflow:hidden;
}

/* Floating hearts */
.heart{
    position:absolute;
    color:red;
    animation: float 6s linear infinite;
}

@keyframes float{
    0%{transform:translateY(100vh);opacity:1;}
    100%{transform:translateY(-10vh);opacity:0;}
}

/* Sorry text */
#sorryText{
    height:150px;
    overflow:auto;
    font-size:18px;
    margin-top:20px;
    color:#fff;
}

/* Middle Message */
#mainMessage{
    font-size:28px;
    margin:20px;
    color:white;
    font-weight:bold;
    animation: pulse 2s infinite;
}

@keyframes pulse{
    0%{transform:scale(1);}
    50%{transform:scale(1.1);}
    100%{transform:scale(1);}
}

/* Buttons */
button{
    padding:15px 30px;
    font-size:20px;
    border:none;
    border-radius:30px;
    cursor:pointer;
    margin:20px;
    transition:0.3s;
}

#yesBtn{
    background-color:#00ff88;
}

#noBtn{
    background-color:#ff4d4d;
    color:white;
}

button:hover{
    transform:scale(1.1);
}

#finalMessage{
    display:none;
    font-size:35px;
    color:white;
    margin-top:20px;
    animation: pulse 1s infinite;
}
</style>
</head>

<body>

<h1 style="color:white;">💖 Sorry Shravani 💖</h1>

<div id="sorryText"></div>

<div id="mainMessage">
Sorry for my mistake 😔 <br>
Please forgive me Shravani ❤️
</div>

<button id="yesBtn" onclick="forgive()">YES 💕</button>
<button id="noBtn" onclick="growYes()">NO 😢</button>

<div id="finalMessage">
Yayyy!!! 🎉💖<br>
Shravani Forgave Me 😭❤️<br>
Thank You So Much!!!
</div>

<script>

// Print "Sorry Shravani" 100 times
let text="";
for(let i=1;i<=100;i++){
    text += i + ". Sorry Shravani ❤️<br>";
}
document.getElementById("sorryText").innerHTML = text;

let yesSize = 20;

function growYes(){
    yesSize += 10;
    document.getElementById("yesBtn").style.fontSize = yesSize + "px";
}

function forgive(){
    document.getElementById("finalMessage").style.display="block";
    document.getElementById("yesBtn").style.display="none";
    document.getElementById("noBtn").style.display="none";
    document.getElementById("mainMessage").innerHTML="You are the best person in my life ❤️";
}

// Create floating hearts
setInterval(function(){
    let heart=document.createElement("div");
    heart.className="heart";
    heart.style.left=Math.random()*100+"vw";
    heart.style.fontSize=(Math.random()*20+10)+"px";
    heart.innerHTML="❤️";
    document.body.appendChild(heart);
    setTimeout(()=>{heart.remove();},6000);
},500);

</script>

</body>
</html>
