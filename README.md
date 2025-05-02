# My-project-1-calculator
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="main">
        <div class="display ">
    <input type="text" placeholder="Welcome to Shami's Calculator !">
        </div>
        <div class="btns">
            <button class="btn" >Clear</button>
            <button class="btn d" >Delete</button>
            <button class="btn" >%</button>
            <button class="btn" >/</button>
            <button class="btn" >7</button>
            <button class="btn" >8</button>
            <button class="btn" >9</button>
            <button class="btn" >*</button>
            <button class="btn" >4</button>
            <button class="btn" >5</button>
            <button class="btn" >6</button>
            <button class="btn" >-</button>
            <button class="btn" >1</button>
            <button class="btn" >2</button>
            <button class="btn" >3</button>
            <button class="btn" >+</button>
            <button class="btn" >0</button>
            <button class="btn" >00</button>
            <button class="btn" >.</button>
            <button class="btn" >=</button>
        </div>
    </div>
</body>
<script src="one.js"></script>
</html>
---------------------=====================================-------------------------------
body{
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    background-color:#337598;
}
.main {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 500px;
    width: 40vw;
    background-color: #00080e;
    border-radius: 50px;
    position: absolute;
    top: 15px;
    position: relative;
}
button {
    height: 70px;
    width: 20vmin;
    font-size: 1.3rem;
    margin: 1px;
    border-radius: 30px;
    background-color: #142F44;
    color: #A2BBCF;
    cursor: pointer;
    

}
.btns{
    position: absolute;
    top: 130px;
    left: 7px;

    
}
input{
    height:19vmin;
    width: 83vmin;
    background-color: #142F44;
    position: absolute;
    top: 8px;
    left: 3px;
    border-top-left-radius: 50px;
    border-top-right-radius: 50px;
    font-size: xx-large;
    color: #c2e3ff;
    
    

    
}
h1{
    position: absolute;
    color: #A2BBCF;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    bottom: 0px;
    left: 10px;
    
    
}
.blink{
    animation: blink 0.8s   infinite  ;
}

@keyframes blink{
   from{
    opacity: 0%;
   }
    to{
        opacity:100%;
    }
}


---------------------------------============================-----------------------------
let str = "";
const btns = document.querySelectorAll(".btn");
const input = document.querySelector("input")

Array.from(btns).forEach((btn)=>{
btn.addEventListener("click",(e)=>{
if (e.target.innerHTML == "="){
    str=eval(str);
    input.value = str;
}
else if (e.target.innerHTML == "Delete"){
    str = str.slice(0,-1);
    input.value = str;}
else if (e.target.innerHTML == "Clear"){
        str = "";
        input.value = str;}
else{

    str  = str + e.target.innerHTML;
    input.value = str;
}
})
})


