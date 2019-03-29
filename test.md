<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
    <title>欢迎来，Mr.ning博客</title>
    <link rel="shortcut icon" href="img/iocn.jpg">
    <link rel="stylesheet" href="css/style.css">    
    <style type="text/css">
    html,body{width: 100%;height: 100%;}
    *{padding: 0;margin: 0;}
	.box{
		width: 100%;
		height: 100%;
		background:url(img/bgGitHub.jpg) no-repeat;
		background-size: cover;
        position: relative;
        overflow: hidden;
        font-family: 'Microsoft YaHei';
        cursor: pointer;
	}
	.box h1{font-size: 32px;color: #fff;width: 100%;text-align: center;font-weight: 400;position: absolute;top: 20%;}
	.box p{font-size: 20px;color: #fff;width: 100%;text-align: center;font-weight: 400;position: absolute;top: 35%;}
	em{font-style: normal;}
	#tab{
            width: 500px;
            height: 200px;
            /*background:-webkit-gradient(linear,center top,center bottom,from(blue), to(white));*/
            background:rgba(193,193,193,.2);/*css3设置渐变*/
            margin-bottom: 100px;
            position: absolute;
            right:2%;
            top: 2%
        }
        #aTime{
            color: #fff;
            /*text-align: center;
            /*line-height: 200px;*/
            float: left;
        }
        #Tradion{
            width: 100px;
            height: 100px;
            border: 2px solid #fff;
            border-radius: 100px;
            float: left;
            margin: 50px 50px;
        }
        #hours{
            width: 30px;
            height: 2px;
            margin:50px 50px;
            background: #fff;
            transform-origin: left bottom;
        }
        #minutes{
            width: 38px;
            height: 2px;
            background: #fff;
            margin:-50px 50px;
            transform-origin: left bottom;
            transform:rotate(0deg);
        }
        #seconds{
            width: 45px;
            height: 1px;
            background: #fff;
            margin:50px 50px;
            transform-origin: left bottom;
            transform:rotate(0deg);

        }
        .tran{
            transform: rotate(-90deg);/*这里测试了一下旋转角*/
        }
        #dian{
            width:6px;
            height: 6px;
            border-radius: 6px;
            background: #fff;
            margin:-55px 46px;
        }
        #aDate{
        	color: #fff;
            padding-top:88px;
        }
        #week{
            color: #fff;
            padding-top:10px;
        }
        .box>h2{font-weight: 400;font-size:20px;color: #fff;width: 80%;position: absolute;left: 12%;top: 28%;}
        .box h2 em{font-weight: 400;font-size:16px;color: #fff;}
    </style>
</head>
<body>
    <div class="box">
        <h1>您是第<em class="num">1</em>位，欢迎来到Mr.zhaoni的网页</h1>
        <h2>个人签名：<em>一辈子很短，努力的做好两件事就好；第一件事是热爱生活，好好的去爱身边的人；第二件事是努力学习，在工作中取得不一样的成绩，实现自己的价值，而不是仅仅为了赚钱；</em></h2>        
        <p>更多功能还在开发中，敬请期待。。。</p>
	    <div id="tab">
		    <div id="Tradion">
		        <div id="hours" class="tran"></div>
		        <div id="minutes" class="tran"></div>
		        <div id="seconds" class="tran"></div>
		        <div id="dian"></div>
		        
		    </div>
		    <h1 id="aTime"></h1>
		    <h3 id="aDate"></h3>
		    <h2 id="week"></h2>
	    </div>
  </div>

  <div class="night">
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
  </div>
  <div class="night1">
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
    <div class="shooting_star"></div>
  </div>
</body>
<script type="text/javascript" src="jquery-2.1.1.min.js"></script>
<script type="text/javascript">
 window.onload=function(){
            function addzero(num){
                if(num>=10)
                {
                    return ""+num;
                }
                else
                {
                    return "0"+num;
                }
            }
            
            function times(){
                var date=new Date();
                var aTime=document.getElementById('aTime');
                var str= addzero(date.getHours())+":"+ addzero(date.getMinutes())+":"+ addzero(date.getSeconds());
                aTime.innerHTML=str;
            }
            setInterval(times,1000);
            times();
            function Ttranform(){
                var date=new Date();
                var hours=document.getElementById('hours');
                var minutes=document.getElementById('minutes');
                var seconds=document.getElementById('seconds');
                var num=date.getHours();
                var num2=date.getMinutes();
                var num3=date.getSeconds();
                hours.style.transform="rotate("+(num*30-90)+"deg)";
                minutes.style.transform="rotate("+(num2*6-90)+"deg)";
                seconds.style.transform="rotate("+(num3*6-90)+"deg)";

            }
            setInterval(Ttranform,1000);
            Ttranform();

             function Adate(){
                var date=new Date();
                var aDate=document.getElementById("aDate");
                var week=document.getElementById('week');
                var weekList=["星期天","星期一","星期二","星期三","星期四","星期五","星期六"];
                var str= date.getFullYear()+"-"+(date.getMonth()+1)+"-"+ date.getDate();
                aDate.innerHTML=str;
                var westr=weekList[date.getDay()];
                week.innerHTML=westr;
            }
            Adate();


            document.addEventListener('visibilitychange', function () {
                if (document.visibilityState == 'hidden') {
                    normal_title = document.title;
                    document.title = '怎么离开了呢，快回来(灬ꈍ ꈍ灬)';
                } else document.title = normal_title;
            });
}
</script>
</html>