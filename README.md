<html xmlns="http://www.w3.org/1999/xhtml" >
<head>
    <title>Start and Stop a Timer using JavaScript by DevCurry.com</title>
    <script type="text/javascript">
        var check = null;

        function printDuration() {
            if (check == null) {
                var cnt = 0;

                check = setInterval(function () {
                    cnt += 1;
                    document.getElementById("para").innerHTML = cnt;
                }, 1000);
            }
        }

        function stop() {
            clearInterval(check);
            check = null;
            document.getElementById("para").innerHTML = '0';
        }
    </script>
</head>
<body>
<div>
    <p id="para">0</p>
    <input id="btnStart" type="button" value="Start"
        onclick="printDuration();" />
    <input id="btnStop" type="button" value="Stop"
        onclick="stop();" />
</div>
</body>
</html>
