<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>扔骰子遊戲</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }
        button {
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
        }
        .result {
            font-size: 24px;
            margin-top: 20px;
        }
        .score {
            font-size: 20px;
            margin-top: 10px;
        }
        .intro {
            margin-bottom: 30px;
            font-size: 18px;
        }
    </style>
</head>
<body>
    <h1>扔骰子遊戲</h1>
    
    <div class="intro">
        <p>歡迎來到扔骰子遊戲！</p>
        <p>在這個遊戲中，你可以隨機擲骰子，並將每次擲出的數字累加到你的總分中。</p>
        <p>每次擲骰子會顯示結果，並更新你的總分。</p>
        <p>祝你好運！</p>
    </div>

    <button id="rollButton">擲骰子</button>
    <div class="result" id="result">結果: 0</div>
    <div class="score" id="score">總分: 0</div>

    <script>
        let totalScore = 0;

        document.getElementById("rollButton").addEventListener("click", function() {
            // 隨機生成一個 1 到 6 的數字
            const rollResult = Math.floor(Math.random() * 6) + 1;

            // 更新結果和總分
            totalScore += rollResult;
            document.getElementById("result").textContent = "結果: " + rollResult;
            document.getElementById("score").textContent = "總分: " + totalScore;
        });
    </script>
</body>
</html>
