# Digital-Clock
<!DOCTYPE html>
<html lang="en" dir="ltr">
<hea d>
<meta charset="utf-8">
<ti tle>Digital Clock with Glowing Effect</title>
<s tyle> body {
margin: 0; padding: 0;
background-color: #011627; color: #fdfffc;
text-align: center;
background-position: center;
background-repeat: no-repeat; background-size: cover;
height: 100vh; display: fl ex;
justify-content: center; align-items: center;
flex-direction: column;
}


.wrapper {
position: relative; width: 200px;
 
height: 100px;
background: #011627; display: fl ex;
justify-content: center; align-items: center;
border-radius: 20px;
box-shadow: 0 0 30px rgba(255, 255, 255, 0.2);
}


.di splay {
font-size: 40px; font-weight: bold;
}


span {
position: absolute; width: 10px;
height: 10px;
background: #fdfffc; border-radius: 50%;
box-shadow: 0 0 30px #fdfffc;
}


span:nth-child(2) { top: -20px;
left: 50%;
transform: translateX(-50%);
}


span:nth-child(3) { bottom: -20px;
left: 50%;
transform: translateX(-50%);
 
}


h1 {
font-size: 45px; margin-top: 20px;
}


input {
width: 75px; height: 50px;
font-size: 45px;
border-radius: 10px; margin: 10px;
background-color: white; color: black;
border-style: none;
}


.btn:hover {
background-color: yellow; cursor: pointer;
}
</s tyle>
</hea d>
<body>
<di v class="wrapper">
<di v class="display">
<di v id="time"></div>
</di v>
<s pan></span>
<s pan></span>
</di v>
<s cript>
 
setInterval(() => {
const time = document.querySelector(".display #time"); let date = new Date();
let hours = date.getHours();
let minutes = date.getMinutes(); let seconds = date.getSeconds(); let day_night = "AM";
i f (hours > 12) {
day_night = "PM"; hours = hours - 12;
}
i f (seconds < 10) {
seconds = "0" + seconds;
}
i f (minutes < 10) {
minutes = "0" + minutes;
}
if (hours < 10) {
hours = "0" + hours;
}
time.textContent = hours + ":" + minutes + ":" + seconds + " " + day_ni ght;
});
</s cript>
</body>
</html >
