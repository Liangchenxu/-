## Lucifer
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <select onchange="change_back()" id="change">
        <option value="a">春天</option>
        <option value="b">夏天</option>
        <option value="c">秋天</option>
        <option value="d">冬天</option>

    </select>


    <script>
        document.body.style.background = 'url(001.jpg)';
        function change_back() {
            hand = document.getElementById('change');
//            console.log(hand.value);
//            console.log(typeof hand.value);  // string
            switch (hand.value){
                case 'a':
                    document.body.style.background = 'url(002.jpg)';
                    break;
                case 'b':
                    document.body.style.background = 'url(003.jpg)';
                    break;
                case 'c':
                    document.body.style.background = 'url(004.jpg)';
                    break;
                case 'd':
                    document.body.style.background = 'url(005.jpg)';
                    break;
            }
        }
    </script>
</body>
</html>



