
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Index</title>
</head>
<body>
     
    <div class="main">
    <div class="img"></div>
    <div class="sec"></div>
    <div class="hour"></div>
    <div class="minute"></div>
    <div class="circle"></div>
    </div>
</body>
</html>
<style>
*{margin:0; padding:0;bos-sizing:border-box;}


body{display:flex;
      align-items:center;
      justify-content:center;
      }

.main{
    height:500px;
    width:500px;
    }
.sec{ 
    opacity:0;
    width:150px;
    height:1px;
    background:black;
    transform-origin: left;
    transform:rotate(-90deg);
    
}


.hour,.minute,.sec,.circle{
  border-radius:;
   position:absolute;
   left:200px;
   top:197px;
   transform:translate(-50%);

    margin:auto;
}


    .hour{
    
    
    width:26px;
    height:7px;
    background:#28b571;
    transform-origin: left;
    transform:rotate(-90deg);
	border-radius:0px 100px 100px 0px;

    
    }
    .minute{

    width:39px;
    height:4px;
    background:#28b571;
    transform-origin: left;
    transform:rotate(-90deg);
    border-radius:0px 100px 100px 0px;

    
    
    }
    
    .circle{
    top:191px;
    width:17px;
    height:17px;
    background:#f3951a;
    border-radius:50%;
    
    }
    .img{
    background:url("./clock.jpg");
    background-size:100% 100%;
    background-repeat:no-repeat;
    position:absolute;
    transform:translate(-50%);
    top:100px;
    left:200px;
    width:356px;
    height:200px;
    
    background-position:center;
    
   
    }
	
	
	
body {
    background: #28abe3;
}
</style>


<script>

det = new Date();
s = det.getSeconds()*6-90;
sc=  det.getSeconds();
ml=det.getMilliseconds()*.006+s;
m = .1*sc+det.getMinutes()*6-90;
mn=det.getMinutes();

h=.5*mn+det.getHours()*30-90;


document.querySelector(".sec").style.transform = "rotate("+ml+"deg)";

document.querySelector(".hour").style.transform = "rotate("+h+"deg)";


document.querySelector(".hour").style.transform = "rotate("+m+"deg)";


function sec (){

  det = new Date();     
  s= det.getSeconds()*6-90;
  ml=det.getMilliseconds()*.006+s;
 sc=  det.getSeconds();
  m = .1*sc+det.getMinutes()*6-90;
  mn=det.getMinutes();
  h=.5*mn+det.getHours()*30-90;
  
document.querySelector(".sec").style.transform = "rotate("+ml+"deg)";



document.querySelector(".hour").style.transform = "rotate("+h+"deg)";

document.querySelector(".minute").style.transform = "rotate("+m+"deg)";




};


setInterval(sec,10)

</script>
