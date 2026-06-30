<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday bhai</title>

    <style>
        @keyframes twinkle {
            0% {
                opacity: 0.2;
            }

            50% {
                opacity: 1;
            }

            100% {
                opacity: 0.2;
            }
        }

        @keyframes glowPulse {

            0%,
            100% {
                text-shadow: 0 0 30px rgba(255, 215, 0, 0.4),
                    0 0 80px rgba(255, 215, 0, 0.2);
            }

            50% {
                text-shadow: 0 0 60px rgba(255, 215, 0, 1),
                    0 0 120px rgba(255, 215, 0, 0.6),
                    0 0 200px rgba(255, 215, 0, 0.3);

            }
        }

        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes shoot {
            0% {
                transform: translateX(0px) translateY(0px) rotate(45deg);
                opacity: 1;
            }

            70% {
                opacity: 1;
            }

            100% {
                transform: translateX(300px) translateY(300px) rotate(45deg);
                opacity: 0;

            }
        }

        @keyframes cardGlow {

            0%,
            100% {
                box-shadow: 0 0 10px rgba(255, 215, 0, 0.1),
                    0 0 20px rgba(255, 215, 0, 0.05);
                border-color: rgba(255, 215, 0, 0.25);
            }

            50% {
                box-shadow: 0 0 30px rgba(255, 215, 0, 0.05),
                    0 0 60px rgba(255, 215, 0, 0.3),
                    0 0 100px rgba(255, 215, 0, 0.1);

                border-color: rgba(255, 215, 0, 0.8);
            }
        }

        body {
            background-color: #0a0a0f;
            color: #FFD700;
            text-align: center;
            font-family: Georgia, serif;
            padding: 0;
            margin: 0;
        }

        h1 {
            font-size: 20px;
            color: #444444;
            letter-spacing: 6px;
            margin-top: 80px;

        }

        h2 {
            font-size: 80px;
            color: #FFD700;
            letter-spacing: 10px;
            margin: 0;
            animation: glowPulse 2.5s ease-in-out infinite;

        }

        .msg {
            font-size: 16px;
            color: #aaa;
            margin-top: 40px;
            line-height: 2;
            letter-spacing: 1px;
            max-width: 480px;
            border: 1px solid rgba(255, 215, 0, 0.25);
            border-radius: 16px;
            padding: 28px 32px;
            margin: 40px auto;
            animation: fadeUp 1s ease forwards, cardGlow 2.5s ease-in-out 1s infinite;
            cursor: pointer;
        }

        .msg2 {
            font-size: 16px;
            color: #aaa;
            margin-top: 40px;
            line-height: 2;
            letter-spacing: 1px;
            max-width: 480px;
            border: 1px solid rgba(255, 215, 0, 0.25);
            border-radius: 16px;
            padding: 28px 32px;
            margin: 20px auto;
            animation: fadeUp 1s ease forwards, cardGlow 2.5s ease-in-out 1.4s infinite;
            animation-delay: 0.4s;
            opacity: 0;
            cursor: pointer;
        }

        .msg3 {
            font-size: 16px;
            color: #aaa;
            margin-top: 40px;
            line-height: 2;
            letter-spacing: 1px;
            max-width: 480px;
            border: 1px solid rgba(255, 215, 0, 0.25);
            border-radius: 16px;
            padding: 28px 32px;
            margin: 20px auto 60px;
            animation: fadeUp 1s ease forwards, cardGlow 2.5s ease-in-out 1.8s infinite;
            animation-delay: 0.8s;
            opacity: 0;
            cursor: pointer;
        }

        .date {
            font-size: 15px;
            color: #555;
            letter-spacing: 5px;
            margin: 8px 0 0;
            text-transform: uppercase;
        }

        @keyframes bounce {

            0%,
            100% {
                transform: translateY(0px);
            }

            50% {
                transform: translateY(-10px);
            }
        }

        .cake {
            font-size: 60px;
            margin-top: 20px;
            animation: bounce 2s ease-in-out infinite;
            display: inline-block;
        }


        @media (max-width: 600px) {
            h1 {
                font-size: 18px;
                letter-spacing: 3px;
                margin-top: 40px;
            }

            h2 {
                font-size: 38px;
                letter-spacing: 4px;
            }

            .date {
                font-size: 11px;
                letter-spacing: 3px;
            }

            .cake {
                font-size: 40px;
            }

            .msg,
            .msg2,
            .msg3 {
                font-size: 13px;
                padding: 18px 16px;
                margin: 12px auto;
                line-height: 1.8;
                letter-spacing: 0.5px;
                max-width: 90%;
            }

            .msg3 {
                word-break: break-word;
                overflow-wrap: break-word;
            }

            #welcome #glass {
                padding: 35px 30px !important;
                width: 85% !important;
            }

            .welcome-name {
                font-size: 10px;
                letter-spacing: 6px;
            }

            .welcome-date {
                font-size: 11px;
                letter-spacing: 3px;
            }

            .welcome-sub {
                font-size: 11px;
                letter-spacing: 2px;
                margin-top: 14px;
            }


        }

        .msg:hover,
        .msg2:hover,
        .msg3:hover {
            transform: translateY(-6px);
            border-color: rgba(255, 215, 0, 0.7);
        }

        #welcome {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #0a0a0f;
            z-index: 999;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;

        }

        #glass {
            border: 1px solid rgba(255, 215, 0, 0.3);
            border-radius: 24px;
            padding: 60px 80px;
            text-align: center;
            background: rgba(255, 215, 0, 0.03);
            box-shadow: 0 0 60px rgba(255, 215, 0, 0.1),
                inset 0 0 40px rgba(255, 215, 0, 0.05);

            backdrop-filter: blur(10px);
        }

        .welcome-date {
            font-size: 13px;
            letter-spacing: 6px;
            color: #555;
            text-transform: uppercase;
            margin: 0 0 16px;
        }

        .welcome-name {
            font-size: 70px;
            letter-spacing: 12px;
            color: #FFD700;
            margin: 0;
            animation: glowPulse 2.5s ease-in-out infinite;
        }

        .welcome-sub {
            font-size: 13px;
            letter-spacing: 4px;
            color: #444;
            text-transform: uppercase;
            margin: 20px 0 0;
        }
    </style>
</head>

<body>

    <div id="welcome">
        <div id="glass">
            <p class="welcome-date">30 june</p>
            <h1 class="welcome-name">AZAN</h1>
            <p class="welcome-sub">Tap to open ✨</p>
        </div>
    </div>


    <h1>＼(^o^)／<br>-Happy Birthday-</h1>
    <h2>B H A I</h2>
    <p class="date">-30 JUNE-</p>
    <p class="cake">🎂</p>



    <p class="msg"> "Not by blood, but by heart." <br>
        Happy birthday bhai (♡˘▽˘) ma na jaha tak tumhay jana hay tum aik bohat acha insan ho ♡〜٩(^▿^)۶〜♡ tum jasa dost
        milna meri
        khushkismati hay ma na kabhi socha bhi nai tha ka mujha itna acha dost mil sakta hay lakin phir tum ay or
        mujha
        bohat zyada khushi hui (ﾉ◕ヮ◕)ﾉ*:･ﾟ✧ mujha aik partner mil gaya dhair sari batay karna ka liya yar aik time ho
        gaya
        hamari
        dosti ko or ab agar tum sa kuch chupana ke koshish bhi karun na nai chupaya jata bhai you are the best ma
        na
        pehla insan dekha hay jo itna mukhlis or acha hay or wo tum ho 🖤 </p>

    <p class="msg2">Ma apna pura dil sa dua karti hun ka ab tumhari zindigi ma koi bhi mushkil na ay sirf or sirf
        khushiya he khushiya ho (＾▽＾) or aik pyari se zoja jo tum sa be intiha mohabat karay or tum bhi us sa ba intiha
        mohabat karo wasa to ya kaam (¬‿¬)ง tumhay bohat acha sa ata hay (〃▽〃) tum dono ke love story aik dam
        story ke tarha ho
        asi
        mohabat ho jo dunya ma kisi na bhi na ke ho waii yar kitna pyara lago ka tum log aik sath ☆*:.｡.o(≧▽≦)o.｡.:*☆
        Mashallah
        Mashallah <br> (≧∀≦)ノ
    </p>

    <p class="msg3">yar aik baat dil sa bolti hun (￫‿￩) tum ho to bohat acha insan but pata nai ku lagta hay ka tum
        jitna
        bahar sa khush ho na utna he andar sa uljha hua ho ma dua karti hun ka tum jitna bahar sa khush dikhta ho
        utna he andar sa bhi ho jao, a galla lag ja yara (っ◔◡◔)っ ♥ allah paak tumhari har jaiz dua kabool karay <br>
        ameeeeeeeeeeeeeeeeeeeeeeeeen <br>
        suma <br>
        ameeeeeeeeeeeeeeeeeeeeeeeeen
    </p>
    <script>
        const welcome = document.getElementById('welcome');
        welcome.addEventListener('click', function () {
            const audio = new Audio('leberch-motivation-517463.mp3');
            audio.loop = true;
            audio.play();

            welcome.style.transition = 'opacity 0.8s ease';
            welcome.style.opacity = '0';
            setTimeout(function () {
                welcome.style.display = 'none';
            }, 800);
        });



        for (let i = 0; i < 80; i++) {
            const star = document.createElement('div');

            star.style.position = 'fixed';
            star.style.borderRadius = '50%';
            star.style.background = 'white';

            const size = Math.random() * 2.5 + 0.5 + 'px';
            star.style.width = size;
            star.style.height = size;

            star.style.top = Math.random() * 100 + '%';
            star.style.left = Math.random() * 100 + '%';

            star.style.animation = 'twinkle ' + (2 + Math.random() * 3) + 's ease-in-out infinite';

            document.body.appendChild(star);
        }

        for (let i = 0; i < 5; i++) {
            const shoot = document.createElement('div');

            shoot.style.position = 'fixed';
            shoot.style.width = '120px';
            shoot.style.height = '1.5px';
            shoot.style.background = 'linear-gradient(to right,transparent,white)';
            shoot.style.top = Math.random() * 40 + '%';
            shoot.style.left = Math.random() * 60 + '%';
            shoot.style.opacity = '0';
            shoot.style.animation = 'shoot ' + (2 + Math.random() * 2) + 's ease-in-out ' + (i * 2 + Math.random() * 3) + 's infinite';
            document.body.appendChild(shoot);

        }
    </script>
</body>


</html>
