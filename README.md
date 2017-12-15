<script>

        var num = 0;  // 定义第一个输入的数据

        function jsq(num) {

            //获取当前输入

            if(num=="%"){

                document.getElementById('screenName').value=Math.round(document.getElementById('screenName').value)/100;

            }else{

                document.getElementById('screenName').value += document.getElementById(num).value;

            }

        }

        function eva() {

            //计算输入结果

            document.getElementById("screenName").value = eval(document.getElementById("screenName").value);

        }

        function clearNum() {

            //清0

            document.getElementById("screenName").value = null;

            document.getElementById("screenName").focus();

        }

        function tuiGe() {

            //退格

            var arr = document.getElementById("screenName");

            arr.value = arr.value.substring(0, arr.value.length - 1);

        }

    </script>

<!DOCTYPE html>
<html>
<head>
<title></title>

<body>
<div id="calculator">
    <div class="LOGO">
        <span class="name">简单的计算器</span>
       
    </div>
    <div id="shuRu">
     
        <div class="screen">
            <input type="text" id="screenName" name="screenName" class="screen">
        </div>
    </div>
    <div id="keys">
     
   
        <input type="button" id="7" onclick="jsq(this.id)" value="7" class="buttons">
        <input type="button" id="8" onclick="jsq(this.id)" value="8" class="buttons">
        <input type="button" id="9" onclick="jsq(this.id)" value="9" class="buttons">
        <input type="button" id="Back" onclick="tuiGe()" value="Back" class="buttons">
        <input type="button" id="C" onclick="clearNum()" value="C" class="buttons" style="margin-right:0px">
   
        <input type="button" id="4" onclick="jsq(this.id)" value="4" class="buttons">
        <input type="button" id="5" onclick="jsq(this.id)" value="5" class="buttons">
        <input type="button" id="6" onclick="jsq(this.id)" value="6" class="buttons">
        <input type="button" id="00" onclick="jsq(this.id)" value="00" class="buttons">
        <input type="button" id="0" onclick="jsq(this.id)" value="0" class="buttons" style="margin-right:0px">

        <input type="button" id="1" onclick="jsq(this.id)" value="1" class="buttons">
        <input type="button" id="2" onclick="jsq(this.id)" value="2" class="buttons">
        <input type="button" id="3" onclick="jsq(this.id)" value="3" class="buttons">
        <input type="button" id="+" onclick="jsq(this.id)" value="+" class="buttons">
        <input type="button" id="-" onclick="jsq(this.id)" value="-" class="buttons" style="margin-right:0px">
  
        <input type="button" id="*" onclick="jsq(this.id)" value="*" class="buttons">
        <input type="button" id="/" onclick="jsq(this.id)" value="/" class="buttons"> 
        <input type="button" id="." onclick="jsq(this.id)" value="." class="buttons">
        <input type="button" id="%" onclick="jsq(this.id)" value="%" class="buttons">
        <input type="button" id="eva" onclick="eva()" value="=" class="buttons" style="margin-right:0px">
       
    </div>
    <div class="footer">
        <span class="aside">欢迎使用计算器</span>
            </span>
    </div>
</div>

</body>