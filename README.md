# html-and-css-vision-board- 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Welcome to 2026 – Space</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:"Poppins",sans-serif;
}

/* 🌌 Space Background */
body{
    height:100vh;
    background:
        radial-gradient(circle at top, #2b1055, #0b0c2a 50%, #000 85%);
    display:flex;
    justify-content:center;
    align-items:center;
    overflow:hidden;
    color:white;
}

/* ⭐ Blinking stars */
.stars{
    position:absolute;
    inset:0;
    background-image:
        radial-gradient(1px 1px at 10% 20%, white, transparent),
        radial-gradient(2px 2px at 30% 70%, white, transparent),
        radial-gradient(1px 1px at 50% 40%, white, transparent),
        radial-gradient(2px 2px at 70% 60%, white, transparent),
        radial-gradient(1px 1px at 90% 30%, white, transparent),
        radial-gradient(2px 2px at 20% 85%, white, transparent);
    background-size:250px 250px;
    animation: blink 6s infinite alternate;
    opacity:0.8;
}

/* star blinking */
@keyframes blink{
    from{opacity:0.4;}
    to{opacity:1;}
}

/* 🧊 Glass Card */
.glass{
    width:560px;
    height:350px;
    background:rgba(255,255,255,0.12);
    backdrop-filter:blur(25px);
    border-radius:35px;
    border:1px solid rgba(255,255,255,0.25);
    box-shadow:0 35px 80px rgba(0,0,0,0.7);
    display:flex;
    justify-content:center;
    align-items:center;
    text-align:center;
    z-index:2;
}

/* ✨ Slowly floating text */
.text{
    position:relative;
    animation: slowFloat 30s ease-in-out infinite;
}

@keyframes slowFloat{
    0%{transform:translateY(0);}
    50%{transform:translateY(-12px);}
    100%{transform:translateY(0);}
}

/* Text style */
.title{
    font-size:36px;
    text-shadow:0 0 20px rgba(255,255,255,0.7);
}

.year{
    font-size:96px;
    font-weight:800;
    background:linear-gradient(90deg,#7fdbff,#c77dff,#ff9de2);
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
    text-shadow:0 0 45px rgba(255,255,255,0.9);
}

/* ⭐ Small blinking stars between text */
.star{
    position:absolute;
    border-radius:50%;
    background:white;
    box-shadow:0 0 8px white, 0 0 16px #9ad9ff;
    animation: twinkle 4s infinite ease-in-out;
}

.s1{width:5px;height:5px;top:55px;left:35%;}
.s2{width:4px;height:4px;top:65px;left:50%;animation-delay:1.5s;}
.s3{width:3px;height:3px;top:50px;left:65%;animation-delay:3s;}

@keyframes twinkle{
    0%{opacity:0.2; transform:scale(0.8);}
    50%{opacity:1; transform:scale(1.5);}
    100%{opacity:0.2; transform:scale(0.8);}
}

/* 🎵 Music control (hidden) */
audio{
    display:none;
}
</style>
</head>

<body>

<!-- background stars -->
<div class="stars"></div>

<!-- 🎵 Background Music -->
<audio autoplay loop>
    <source src="space-music.mp3" type="audio/mpeg">
</audio>

<!-- glass card -->
<div class="glass">
    <div class="text">
        <div class="title">Welcome to</div>

        <!-- blinking stars between text -->
        <div class="star s1"></div>
        <div class="star s2"></div>
        <div class="star s3"></div>

        <div class="year">2026</div>
    </div>
</div>

</body>
</html>
