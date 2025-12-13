# eshwar
living my best life
<!DOCTYPE html>   
<html lang="en">   
<head>   
<meta charset="UTF-8">   
<title>Advanced Internet Speed Test</title>   
<style>     
body {   
font-family: Arial, sans-serif;        
background: #0f172a;         color: 
white;         display: flex;         justify
content: center;         
alignitems: center;         
height: 100vh;
column;         gap:  
20px;   
}   
         flex-direction: 
.card{    
background: #1e293b;         
padding: 30px;         border
radius: 20px;         width: 
350px;         textalign: center;   
box-shadow: 0 0 25px rgba(255,255,255,0.1);   
}   
#speedValue {       
size: 55px;      
font
font-weight: 
bold;
20px;   
margin-top: 
   
}   
button {          
top: 20px;         
margin
padding: 
12px 25px;  font-size: 
18px;  border: none;    
border-radius: 12px;         
cursor: pointer;         
background-color: 
#3b82f6;        color: white;          
transition: 0.25s;   
}   
button:hover {          
color: #60a5fa;   
}   
</style>   
</head>   
<body>   
background
<div class="card">   
<h1>Internet Speed Test</h1>   
<div id="speedValue">-- Mbps</div>   
<button onclick="startTest()">Start Test</button>   
</div>   
<script> function 
startTest() {
     const 
testImage = 
"https://upload.wikimedia.org/wikipedia 
/commons/3/3f/Fron 
alpstock_big.jpg";     
const 
fileSizeInBytes = 
5450000; // 5.45 MB 
image   
let startTime, endTime;   
document.getElementById("speedValue").innerText = "Testing...";   
startTime = new Date().getTime();   
fetch(testImage)   
.then(response => response.blob())   
.then(() => {  
endTime = new Date().getTime();   
let duration = (endTime - startTime) / 1000;         
let bitsLoaded = fileSizeInBytes * 8;   
let speedMbps = (bitsLoaded / duration / (1024 * 1024)).toFixed(2);   
document.getElementById("speedValue").innerText = speedMbps + " Mbps";   
})   
.catch(err => {  
document.getElementById("speedValue").innerText = "Error!";         
console.log(err);   
});   
}   
</script>   
</body>   
</html>  
