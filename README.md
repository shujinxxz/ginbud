<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>uy engineer yohoo!</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            background: hotpink;
            color: #fff;
            font-family: Georgia, "Times New Roman", serif;
            min-height: 100vh;
            overflow-x: hidden;
        }

        /* =========================
           FLOATING BASKETBALLS
        ========================= */

        .basketball {
            position: fixed;
            bottom: -40px;
            font-size: 24px;
            animation: floatBasketball linear infinite;
            pointer-events: none;
            z-index: 0;
            opacity: 0.65;
        }

        .basketball:nth-child(1) {
            left: 5%;
            animation-duration: 12s;
            animation-delay: 0s;
        }

        .basketball:nth-child(2) {
            left: 15%;
            animation-duration: 15s;
            animation-delay: 3s;
        }

        .basketball:nth-child(3) {
            left: 28%;
            animation-duration: 11s;
            animation-delay: 2s;
        }

        .basketball:nth-child(4) {
            left: 42%;
            animation-duration: 16s;
            animation-delay: 5s;
        }

        .basketball:nth-child(5) {
            left: 58%;
            animation-duration: 13s;
            animation-delay: 1s;
        }

        .basketball:nth-child(6) {
            left: 70%;
            animation-duration: 17s;
            animation-delay: 4s;
        }

        .basketball:nth-child(7) {
            left: 82%;
            animation-duration: 12s;
            animation-delay: 2s;
        }

        .basketball:nth-child(8) {
            left: 93%;
            animation-duration: 15s;
            animation-delay: 6s;
        }

        @keyframes floatBasketball {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0;
            }

            10% {
                opacity: 0.65;
            }

            90% {
                opacity: 0.65;
            }

            100% {
                transform: translateY(-110vh) rotate(720deg);
                opacity: 0;
            }
        }

        /* =========================
           OPENING SCREEN
        ========================= */

        #openingScreen {
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 25px;
            position: relative;
            z-index: 1;
        }

        .card {
            width: 100%;
            max-width: 600px;
            text-align: center;
            padding: 50px 30px;
            border: 1px solid rgba(255, 255, 255, 0.35);
            border-radius: 25px;
            background: rgba(255, 255, 255, 0.12);
            backdrop-filter: blur(10px);
            box-shadow: 0 0 40px rgba(255, 255, 255, 0.12);
        }

        .opening-title {
            font-size: clamp(2rem, 6vw, 4rem);
            margin-bottom: 15px;
            letter-spacing: 1px;
        }

        .opening-text {
            font-size: 1.2rem;
            color: #fff;
            margin-bottom: 35px;
        }

        /* =========================
           BUTTON
        ========================= */

        .main-button {
            border: none;
            outline: none;
            background: #fff;
            color: #ff1493;
            padding: 14px 28px;
            border-radius: 30px;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .main-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255, 255, 255, 0.3);
        }

        .main-button:active {
            transform: scale(0.97);
        }

        /* =========================
           PASSWORD SCREEN
        ========================= */

        #passwordScreen {
            min-height: 100vh;
            display: none;
            justify-content: center;
            align-items: center;
            padding: 25px;
            position: relative;
            z-index: 1;
        }

        .password-card {
            width: 100%;
            max-width: 500px;
            text-align: center;
            padding: 45px 30px;
            border: 1px solid rgba(255, 255, 255, 0.35);
            border-radius: 25px;
            background: rgba(255, 255, 255, 0.12);
            backdrop-filter: blur(10px);
            box-shadow: 0 0 40px rgba(255, 255, 255, 0.12);
        }

        .password-card h1 {
            font-size: 2rem;
            margin-bottom: 15px;
        }

        .password-card > p {
            color: #fff;
            margin-bottom: 15px;
            line-height: 1.6;
        }

        .clue {
            font-size: 0.9rem;
            font-style: italic;
            color: #fff !important;
            margin-top: 20px;
            margin-bottom: 20px !important;
        }

        #passwordInput {
            width: 100%;
            padding: 14px 18px;
            margin-bottom: 15px;
            border-radius: 25px;
            border: 1px solid rgba(255, 255, 255, 0.5);
            background: rgba(255, 255, 255, 0.15);
            color: #fff;
            font-size: 1rem;
            text-align: center;
            outline: none;
        }

        #passwordInput::placeholder {
            color: rgba(255, 255, 255, 0.7);
        }

        #passwordInput:focus {
            border-color: #fff;
            background: rgba(255, 255, 255, 0.2);
        }

        #errorMessage {
            display: none;
            color: #fff !important;
            font-size: 0.9rem;
            margin-top: 15px;
        }

        /* =========================
           LETTER SECTION
        ========================= */

        #letterSection {
            display: none;
            min-height: 100vh;
            padding: 30px 20px 70px;
            position: relative;
            z-index: 1;
        }

        .letter-container {
            width: 100%;
            max-width: 850px;
            margin: 0 auto;
        }

        /* =========================
           LETTER
        ========================= */

        .letter-card {
            background: #f5f5f5;
            color: #111;
            border-radius: 18px;
            padding: 55px 60px;
            box-shadow: 0 15px 50px rgba(0, 0, 0, 0.3);
            line-height: 1.8;
        }

        .letter-card p {
            margin-bottom: 22px;
            font-size: 1rem;
        }

        .letter-card p:first-child {
            margin-bottom: 30px;
        }

        /* =========================
           SIGNATURE
        ========================= */

        .signature {
            margin-top: 35px;
            margin-bottom: 0 !important;
            font-family: Georgia, "Times New Roman", serif;
            font-size: 1rem !important;
            font-style: italic;
            text-align: right;
        }

        /* =========================
           FADE ANIMATION
        ========================= */

        .fade {
            animation: fadeIn 1.2s ease forwards;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(15px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* =========================
           MOBILE
        ========================= */

        @media (max-width: 600px) {

            #openingScreen,
            #passwordScreen {
                padding: 18px;
            }

            .card,
            .password-card {
                padding: 40px 22px;
                border-radius: 20px;
            }

            .opening-title {
                font-size: 2.2rem;
            }

            .opening-text {
                font-size: 1rem;
            }

            .password-card h1 {
                font-size: 1.6rem;
            }

            #letterSection {
                padding: 20px 12px 50px;
            }

            .letter-card {
                padding: 35px 24px;
                border-radius: 14px;
            }

            .letter-card p {
                font-size: 0.95rem;
                line-height: 1.75;
            }

            .signature {
                font-size: 0.95rem !important;
            }
        }
    </style>
</head>

<body>

    <!-- FLOATING BASKETBALLS -->

    <div class="basketball">🏀</div>
    <div class="basketball">🏀</div>
    <div class="basketball">🏀</div>
    <div class="basketball">🏀</div>
    <div class="basketball">🏀</div>
    <div class="basketball">🏀</div>
    <div class="basketball">🏀</div>
    <div class="basketball">🏀</div>


    <!-- =========================
         OPENING SCREEN
    ========================== -->

    <section id="openingScreen">

        <div class="card fade">

            <h1 class="opening-title">
                uy engineer yohoo!
            </h1>

            <p class="opening-text">
                tara, inom?
            </p>

            <button
                class="main-button"
                onclick="showPassword()"
            >
                palag ta lablab baga an
            </button>

        </div>

    </section>


    <!-- =========================
         PASSWORD SCREEN
    ========================== -->

    <section id="passwordScreen">

        <div class="password-card fade">

            <h1>
                mag isip ka muna
            </h1>

            <p>
                basic lang an ta maurag ka baga
            </p>

            <p class="clue">
                Clue: go to store for ice cream 
            </p>

            <input
                type="password"
                id="passwordInput"
                placeholder="Enter the password"
                onkeydown="handleEnter(event)"
            >

            <button
                class="main-button"
                onclick="checkPassword()"
            >
                balbali! 
            </button>

            <p id="errorMessage">
                bule, uliton mo ('s)
            </p>

        </div>

    </section>


    <!-- =========================
         LETTER SECTION
    ========================== -->

    <section id="letterSection">

        <div class="letter-container">

            <!-- LETTER -->

            <div class="letter-card fade">

                <p>
                   <i><b>To my beloved ginbuddy,</b></i>
                </p>

                <p>
                    Kumusta? Hope u doing good there, kung sain na lupalop ka man. Di man natin nakuha ang result na pinagdarasal natin, please know na proud na proud ako saimo, boi. Ika na baga an. Katibay mo ta u bravely took that exam kahit na kinakabahan ka and full of doubts sa sadiri mo. Duman pa sana, panalo na ta dai ka nagsuko. Congrats, engineer!
                </p>

                <p>
                    Gusto ko din pala i-take ang moment na ini na magpasalamat saimo. Review szn wouldn’t be bearable kung wara kamo (u &amp; Mics). Salamat ta G na G ka whenever naga-aya ako magluwas, mag-ice cream to be specific, kahit ata naga-review ka. Sorry kung ano man kasalan ko saimo, and sorry ta siguro kung dai kita sigeng luwas and pinili ta mag-review, baka pasado gayod kita (aya ng aya kasi ang oat na e2 hahaha).
                </p>

                <p>
                    Yaon lang ako digdi pag need mo ako. Feel free to call/message me pag need mo help (bako lang muna sa kwarta ta zero days pa hahahahahaha). Bawi kita next year. Ma-top kita sa boards next year. RGE 2027 TOPNOTCHERS! Pahuway na muna, ner. Next year ta makibakbakan kita (final bakbakan ba hahahah).
                </p>

                <p>
                    P.S. Ano, ice cream o inom? Lisensya!!!
                </p>
                
                 <p>
                    P.P.S. Grabe effort ko 'no? Swerte talaga magiging jowa ko HAHAHAHAHAHA
                </p>

                <p class="signature">
                    <b>engr. bogs :)</b>
                </p>

            </div>

        </div>

    </section>


    <!-- =========================
         JAVASCRIPT
    ========================= -->

    <script>

        const correctPassword = "uncle john's";


        function showPassword() {

            document.getElementById("openingScreen").style.display = "none";

            document.getElementById("passwordScreen").style.display = "flex";

            document.getElementById("passwordInput").focus();

        }


        function handleEnter(event) {

            if (event.key === "Enter") {

                checkPassword();

            }

        }


        function checkPassword() {

            const input =
                document.getElementById("passwordInput");

            const error =
                document.getElementById("errorMessage");


            if (input.value === correctPassword) {

                document.getElementById("passwordScreen").style.display = "none";

                document.getElementById("letterSection").style.display = "block";

                window.scrollTo({
                    top: 0,
                    behavior: "smooth"
                });

            } else {

                error.style.display = "block";

                input.value = "";

                input.focus();

            }

        }

    </script>

</body>
</html>
