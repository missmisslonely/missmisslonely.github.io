---
layout:     post
title:      恋爱计时器
subtitle:   
date:       2020-02-14
author:     Sissi
header-img: img/post1-img-love.jpg
catalog: true
tags:
---

<body>
    <div class="content">
        <h2>佳佳，我们已经在一起了</h2>
        <div class="timer">
            <b id="d">0</b> Days <b id="h">0</b> Hours <b id="m">0</b> Minutes <b id="s">0</b> Seconds
        </div>
    </div>
    
<script>
        function timer() {
            var start = new Date(2020, 1, 22); // 2020.1.22
            var t = new Date() - start;
            var h = ~~(t / 1000 / 60 / 60 % 24);
            if (h < 10) {
                h = "0" + h;
            }
            var m = ~~(t / 1000 / 60 % 60);
            if (m < 10) {
                m = "0" + m;
            }

            var s = ~~(t / 1000 % 60);
            if (s < 10) {
                s = "0" + s;
            }
            document.getElementById('d').innerHTML = ~~(t / 1000 / 60 / 60 / 24);
            document.getElementById('h').innerHTML = h;
            document.getElementById('m').innerHTML = m;
            document.getElementById('s').innerHTML = s;
        }
        timer();
        setInterval(timer, 1000);
    </script>

</body>
<img src="img/post1-bg.jpeg" style="transform:rotate(90deg);">