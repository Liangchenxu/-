## Lucifer
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    输入密码：<input type="password" id="password">
    <input type="button" onclick="func()" value="校验"><br/><br/>
    <span id="flag">此处显示密码设置结果</span><br/>   <!--输出结果和判断密码的格式是否错误-->
    <script type="text/javascript">
        function func(){
            passwd = document.getElementById('password').value;
            flag_head = document.getElementById('flag');         // 获取flag的操作句柄
            // var i = 0；
            // flag_head.innerHTML = 'sdfkskdjfk';
            
            var result = 0;    // 判断密码中是否同时具有字母和数字，如果在下面的判断中发现有数字则加一，并且还有字母的时候再加一
            while(1){
                if (passwd.length<8) {                       // 判断密码是否够8位，否则直接退出循环
                    flag_head.innerHTML = '密码不能少于8位';
                    break;
                }

                var i = 0;      //  用于遍历用户输入的字符串中的字符是否含有大写或者小写的字母                 
                while(i<passwd.length){
                    if(passwd[i].charCodeAt()>=65 && passwd[i].charCodeAt()<= 90 || passwd[i].charCodeAt()>=97 && passwd[i].charCodeAt()<= 122){
                        result += 1;
                        break;    
                    }
                    else{
                        i++;
                    }
                    
                }
                var j = 0;            // 循环查看是否有数字
                while(j<passwd.length){
                    if (passwd[j].charCodeAt()>=48 && passwd[j].charCodeAt()<= 57) {
                        result += 1;   // 有数字就result加一，然后跳出循环
                        break;    
                    }
                    else{
                        j++;      // 如果查找到数字就下标加一，循环遍历
                    }
                }
                                
                if(result == 2){
                    flag_head.innerHTML = '密码设置成功';       // 如果result等于2，那么就说明密码中同时含有数字和字母
                    break;
                }
                else{
                    flag_head.innerHTML = '密码中必须包含数字和字符';
                }
                break;
            }
            
            
        }

    </script>
</body>
</html>
