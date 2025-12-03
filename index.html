
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Happy Birthday Laraib — Card</title>
<script async src="https://www.googletagmanager.com/gtag/js?id=G-WC8VS102L1"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-WC8VS102L1');
</script>
<style>
    /* UPDATED COLOR THEME (Brighter Pink/Gold for Birthday) */
    :root{
        --accent-1: #ff69b4; /* Brighter Pink (Hot Pink) */
        --accent-2: #800080; /* Purple */
        --card-bg: #fff7ff;
        --gold: #FFD700;
        --envelope-bg-color: #f7eaf0; /* Pale background for the body */
    }

    html,body{
        height:100%;
        margin:0;
        font-family: "Segoe UI", Roboto, Arial, sans-serif;
        /* Changed background to light, warm gradient */
        background: linear-gradient(180deg,#fff0f5 0%, #fff 60%); 
        -webkit-font-smoothing:antialiased;
        -moz-osx-font-smoothing:grayscale;
        color:#222;
        overflow:hidden;
    }
    
    /* Confetti Styles */
    .confetti {
        position: absolute;
        width: 10px;
        height: 10px;
        opacity: 0;
        pointer-events: none;
        z-index: 9999;
    }

    /* Layout for scrolling on mobile (Applied to active sections) */
    .section {
        position:absolute;
        inset:0;
        display:flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-start;
        padding:20px;
        box-sizing:border-box;
        opacity:0;
        transform: translateY(24px);
        transition: opacity .45s ease, transform .45s ease;
        pointer-events:none;
        overflow-y: auto;
        -webkit-overflow-scrolling: touch;
        z-index: 1;
    }
    
    /* Center Section 9 (Cake) and INTRO Section */
    #sec9.section, #intro.section {
        justify-content: center;
    }

    .section.active{
        opacity:1;
        transform: translateY(0);
        pointer-events:auto;
        z-index:5;
    }

    /* ------------------------------------------------ */
    /* INTRO DOOR STYLES (Kept for the opening screen) */
    /* ------------------------------------------------ */
    #intro {
        background: linear-gradient(180deg, #ffd9eb 0%, #ffffff 100%);
        transition: opacity 1.5s ease;
        z-index: 10;
    }
    
    .door-container {
        position: relative;
        width: 90%;
        max-width: 500px;
        height: 60vh;
        display: flex;
        justify-content: center;
        align-items: center;
        margin: auto;
    }

    .door {
        position: absolute;
        top: 0;
        width: 50%;
        height: 100%;
        background: linear-gradient(180deg, #800080, #c458c4); /* Purple Door */
        transform-origin: center center;
        transition: transform 1.5s cubic-bezier(0.86, 0, 0.07, 1);
        box-shadow: 0 10px 30px rgba(0,0,0,0.4);
        border-radius: 8px;
    }

    .door.left {
        left: 0;
        transform: translateX(-50%) rotateY(0deg); 
    }

    .door.right {
        right: 0;
        transform: translateX(50%) rotateY(0deg); 
    }

    /* FIX: Corrected class for door animation */
    #intro.door-open .door.left {
        transform: translateX(-100%) rotateY(-130deg);
    }

    #intro.door-open .door.right {
        transform: translateX(100%) rotateY(130deg);
    }

    .greeting-text {
        position: absolute;
        font-size: 2.5rem;
        font-weight: bold;
        color: var(--accent-1);
        text-shadow: 0 0 10px rgba(255, 255, 255, 0.8);
        opacity: 0;
        transition: opacity 0.8s ease 0.5s;
        text-align: center;
        z-index: 5;
    }
    #intro.door-open .greeting-text {
        opacity: 1;
    }


    /* ------------------------------------------------ */
    /* GENERAL CARD STYLES (ENVELOPE - NEW DESIGN) */
    /* ------------------------------------------------ */
    .card-wrap{
        width:100%;
        max-width:920px;
        display:flex;
        flex-direction:column;
        align-items:center;
        gap:18px;
        position: relative;
        margin: auto;
        padding-bottom: 40px;
        padding-top: 40px; /* Add padding for better spacing */
    }

    .envelope {
        width: 720px;
        max-width: 94%;
        height: 420px;
        position: relative;
        perspective: 1400px;
    }

    .envelope .body {
        position:absolute;
        inset:0;
        border-radius:12px;
        background: var(--envelope-bg-color); /* Pale Pink Body */
        box-shadow: 0 18px 60px rgba(20,10,60,0.16);
        overflow:visible;
        display:flex;
        align-items:center;
        justify-content:center;
        padding:28px;
        box-sizing:border-box;
    }

    /* NEW FLAP STYLE (Solid Pink, covers entire body, rotates fully) */
    .envelope .flap {
        position:absolute;
        top:0;
        left:0;
        width:100%;
        height:100%; /* Height is now 100% to fill the body */
        transform-origin: top center;
        background: var(--accent-1); /* Solid Pink Flap */
        border-radius:12px;
        box-shadow: 0 12px 40px rgba(255, 105, 180, 0.4);
        transform-style: preserve-3d;
        transition: transform .8s cubic-bezier(.2,.9,.3,1);
        backface-visibility: hidden;
        z-index:8;
        display:flex;
        align-items:center; /* Center content vertically */
        justify-content:center;
    }
    
    /* NEW: Flap content/decoration removed, instead we show a static greeting */
    .envelope .flap::after{
        content: "Tap to Open Card";
        display:block;
        font-size: 24px;
        font-weight: bold;
        color: white;
        text-shadow: 0 2px 4px rgba(0,0,0,0.3);
    }
    
    /* LETTER STYLE (Sits inside the envelope body) */
    .envelope .letter {
        position:absolute;
        left:6%;
        width:88%;
        height:80%; /* Increased height for content */
        top:10%;
        background: white;
        border-radius:8px;
        box-shadow: 0 8px 30px rgba(30,10,60,0.06);
        transform-origin: bottom center;
        transform: translateY(28px) scale(.98);
        opacity:0;
        transition: transform .8s cubic-bezier(.2,.9,.3,1), opacity .6s;
        padding:22px;
        box-sizing:border-box;
        z-index:6;
        display:flex;
        flex-direction:column;
        justify-content:flex-start;
        align-items:flex-start;
        overflow-y:auto; /* Crucial for scrolling long messages */
        scrollbar-width: thin;
        -webkit-overflow-scrolling: touch;
    }

    .envelope.opened .flap {
        transform: rotateX(-180deg); /* Full rotation to expose the letter */
    }
    .envelope.opened .letter {
        transform: translateY(0) scale(1);
        opacity:1;
    }
    
    .card-content{
        width:100%;
        color:var(--accent-2);
        text-align:left;
    }
    .card-content h1,
    .card-content h2 {
        margin:0 0 8px 0;
        font-size:22px;
        color:var(--accent-2);
        text-align:center;
        width:100%;
    }
    .card-content p{
        margin:0 0 12px 0;
        font-size:18px;
        line-height:1.55;
        color:#222;
        white-space: pre-wrap;
    }
    .quote{
        margin-top:8px;
        font-style:italic;
        color:#333;
        text-align:left;
    }
    
    .controls{
        display:flex;
        gap:12px;
        margin-top:8px;
        z-index: 10;
    }
    .btn{
        appearance:none;
        border:0;
        padding:12px 22px; 
        border-radius:12px; 
        background:linear-gradient(90deg,var(--accent-1), #800080);
        color:#fff;
        cursor:pointer;
        font-size:18px; 
        box-shadow: 0 6px 18px rgba(255, 105, 180, 0.3);
    }
    .btn.secondary{
        background:transparent;
        color:var(--accent-2);
        box-shadow:none;
        border:2px solid rgba(75,46,131,0.2); 
    }
    .btn:disabled {
        opacity: 0.5;
        cursor: not-allowed;
    }
    
    /* ------------------------------------------------ */
    /* CAKE STYLES (Guaranteed Centering) */
    /* ------------------------------------------------ */
    #cake-container {
        position: relative;
        max-width: 500px;
        margin: 20px auto; 
        display: flex;
        justify-content: center; 
        align-items: center;
        height: 450px; 
    }
    #cake { 
        max-width:100%; 
        width:500px; 
        transition: transform .2s ease; 
        border-radius:14px; 
        z-index: 2;
    }
    
    /* Celebration Text (ONLY GLOW EFFECT - Removed opaque background) */
    @keyframes pulseGlow {
        from { text-shadow: 0 0 10px var(--accent-1), 0 0 20px var(--accent-1); }
        to { text-shadow: 0 0 20px var(--accent-1), 0 0 30px #fff; }
    }
    #celebrationText {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%); 
        width: 100%;
        text-align: center;
        font-size: 3.5rem; 
        font-weight: bold;
        color: var(--accent-1); 
        text-shadow: 0px 0px 20px rgba(255, 255, 255, 0.9), 0px 4px 12px rgba(139,46,255,0.3);
        opacity: 0;
        z-index: 10;
        pointer-events: none;
        transition: opacity 1.5s ease-in-out;
        animation: pulseGlow 1.5s infinite alternate; 
    }


    @media (max-width:900px){
        .envelope { width: 92%; height: 420px; }
        .envelope .letter { height:80%; top:10%; padding:16px; }
        .card-content p{ font-size:16px; }
        #cake { width:380px; } 
        #cake-container { height: 400px; max-width: 380px; } 
        #celebrationText { font-size: 2.5rem; }
        .btn { padding: 10px 18px; font-size: 16px; }
    }

    @media (max-width:520px){
        .envelope{ height:360px; }
        .envelope .letter { height:80%; top:10%; }
        .card-content h1{ font-size:20px; }
        .card-content p{ font-size:15px; }
        #celebrationText { font-size: 2rem; }
        #cake { width: 280px; } 
        #cake-container { height: 300px; max-width: 280px; } 
        .btn { padding: 10px 18px; font-size: 16px; }
    }
</style>
</head>
<body>

<section id="intro" class="section active" aria-label="Introduction Screen">
    <div class="door-container">
        <div class="door left"></div>
        <div class="door right"></div>
        <h1 class="greeting-text">Welcome, Laraib!</h1>
    </div>
</section>

<section id="sec2" class="section" aria-label="Section 2">
    <div class="card-wrap">
        <div class="envelope" data-index="2" onclick="openEnvelope(2)">
            <div class="flap"></div>
            <div class="letter" role="article" aria-labelledby="title2">
                <div class="card-content">
                    <h1 id="title2">✨ **Happy Birthday, Laraib!** ✨</h1>
                    <p>آج کا دن آپ کے لیے روشنیوں سے بھرا ہوا ہے، Laraib—</p>
                    <div class="quote">"Aaj ka din waqai bohot khaas hai."</div>
                </div>
            </div>
            <div class="body"></div>
        </div>

        <div class="controls">
            <button class="btn" onclick="openEnvelope(2)">Open Card</button>
            <button class="btn secondary" onclick="skipOpen(2)">Skip</button>
        </div>
    </div>
</section>

<section id="sec3" class="section" aria-label="Section 3">
    <div class="card-wrap">
        <div class="envelope" data-index="3" onclick="openEnvelope(3)">
            <div class="flap"></div>
            <div class="letter" role="article" aria-labelledby="title3">
                <div class="card-content">
                    <h2 id="title3">Aap Jaisi Khoobsurat Insaan</h2>
                    <p>آپ کے اخلاق، آپ کی سچائی، آپ کی نرمی اور آپ کی باریک حسِ جمال-آپ اُن چند لوگوں میں سے ہیں جو چہرے سے زیادہ دل کے خوبصورت ہوتے ہیں۔</p>
                    <div class="quote">"Aap jaisi achi, pyari, seedhi aur sachi insaan ko hamesha duniya ki sab se behtareen cheezein milni chahiye. Aapka ikhlaq, lehja aur soch aap ko sab se alag banati hain"</div>
                    <p>یہ سچ ہے کہ وقت بدل جاتا ہے، لیکن کچھ رشتے اور کچھ خوبصورت یادیں ہمیشہ دل میں محفوظ رہتی ہیں۔ آپ کی معصومیت اور وہ خلوص جو آپ کی باتوں میں ہمیشہ نظر آیا، وہ ایک ایسا سرمایہ ہے جو بہت کم لوگوں کے پاس ہوتا ہے۔ اللہ کرے آپ کے ہر قدم پر آسانیاں ہوں اور آپ کے تمام ارمان پورے ہوں۔ میری دعا ہے کہ آپ کی زندگی کا یہ سال خوشیوں، کامیابیوں اور ڈھیر ساری محبتوں سے بھر پور ہو۔</p>
                </div>
            </div>
            <div class="body"></div>
        </div>

        <div class="controls">
            <button class="btn" onclick="openEnvelope(3)">Open Card</button>
            <button class="btn secondary" onclick="skipOpen(3)">Skip</button>
        </div>
    </div>
</section>

<section id="sec4" class="section" aria-label="Section 4">
    <div class="card-wrap">
        <div class="envelope" data-index="4" onclick="openEnvelope(4)">
            <div class="flap"></div>
            <div class="letter" role="article" aria-labelledby="title4">
                <div class="card-content">
                    <h2 id="title4">Yaadein Jo Reh Gayi</h2>
                    <p>آپ ہمیشہ سب کے لیے اچھا سوچنے والی، ہر ایک کے کام آنے والی، اور دوسروں کی خوشی میں خوش ہونے والی لڑکی ہیں، اور ایسے لوگ واقعی کم ہوتے ہیں۔ 

"Mujhe abhi tak woh din yaad hai jab hum shed se wapis aa rahe thay aur barish ho rahi thi… aur mere mana karne ke bawajood ap ne pani me jump kiya."
"Aur phir aap ke haath ka banaya hua pulao aur custard — abhi tak uski khushboo yaad aati hai."</p>
                    <p>کاش یہ وقت واپس آ جائے، وہ سب معصوم باتیں، وہ سب ہنسی مذاق اور وہ بے فکری کے دن۔ لیکن اب بھی جہاں کہیں بھی آپ ہوں، میری دعا ہے کہ آپ وہاں مکمل خوش اور پرسکون رہیں۔ یہ یادیں ہماری دوستی کی بنیاد ہیں، اور مجھے فخر ہے کہ میں آپ کو جانتا ہوں۔</p>
                </div>
            </div>
            <div class="body"></div>
        </div>

        <div class="controls">
            <button class="btn" onclick="openEnvelope(4)">Open Card</button>
            <button class="btn secondary" onclick="skipOpen(4)">Skip</button>
        </div>
    </div>
</section>

<section id="sec5" class="section" aria-label="Section 5">
    <div class="card-wrap">
        <div class="envelope" data-index="5" onclick="openEnvelope(5)">
            <div class="flap"></div>
            <div class="letter" role="article" aria-labelledby="title5">
                <div class="card-content">
                    <h2 id="title5">Aap Ki Aankhein</h2>
                    <p>آپ کی آنکھیں—وہ گہرا سیاہ رنگ جو عام نہیں، ایک ایسے راز کی طرح ہے جو صرف خوبصورتی نہیں… گہرائی بھی رکھتا ہے۔ 

"Aap ki aankhein woh gehra kaala rang jo na sirf khoobsurat hain balkay puri kainat in ma samai hoi ha."
"Aap ki aankhon me koi ajeeb si khamosh chamak hai jo dekhne wale ko rok leti hai."</p>
                    <p style="text-align: center; font-style: italic; font-weight: 600;">نور ہی نور سے مکھڑے پہ وہ نوری آنکھیں
    
اس کے انجیل سے چہرے پہ زبوری آنکھیں</p>
                    <p>یہ نظم صرف آپ کے لیے لکھی گئی ہے، آپ کی خوبصورتی اس بات کا ثبوت ہے کہ اللہ نے بہت فرصت میں دنیا بنائی ہے۔ ہمیشہ اپنی اس منفرد پہچان کو برقرار رکھیے گا۔</p>
                </div>
            </div>
            <div class="body"></div>
        </div>

        <div class="controls">
            <button class="btn" onclick="openEnvelope(5)">Open Card</button>
            <button class="btn secondary" onclick="skipOpen(5)">Skip</button>
        </div>
    </div>
</section>

<section id="sec6" class="section" aria-label="Section 6">
    <div class="card-wrap">
        <div class="envelope" data-index="6" onclick="openEnvelope(6)">
            <div class="flap"></div>
            <div class="letter" role="article" aria-labelledby="title6">
                <div class="card-content">
                    <h2 id="title6">Duaen & Motivation</h2>
                    <p>میں دعا کرتا ہوں کہ اللہ تعالیٰ آپ کی زندگی کو آسانیوں سے بھر دے۔</p>
                    <div class="quote">"Main dua karta hoon ke Allah aap ke tamam goals aasaan kar de."
"Aap jahan bhi jaayein, izzat, mohabbat aur achi niyat wale log milain.Aapka dil hamesha halka aur khush rahe.Laraib… aap intelligent aur sincere hain.
“Jahan niyat saaf hoti hai, wahan raasta ban hi jaata hai.”
“Aap kamzor nahi — bas nazuk dil ki hain. Aur nazuk dil wale hi asli strong hote hain.”"</div>
                    <p>آپ کی محنت اور سچائی کو کوئی نہیں روک سکتا۔ بس یقین رکھیں اور آگے بڑھیں۔</p>
                </div>
            </div>
            <div class="body"></div>
        </div>

        <div class="controls">
            <button class="btn" onclick="openEnvelope(6)">Open Card</button>
            <button class="btn secondary" onclick="skipOpen(6)">Skip</button>
        </div>
    </div>
</section>

<section id="sec7" class="section" aria-label="Section 7">
    <div class="card-wrap">
        <div class="envelope" data-index="7" onclick="openEnvelope(7)">
            <div class="flap"></div>
            <div class="letter" role="article" aria-labelledby="title7">
                <div class="card-content">
                    <h2 id="title7">End Note</h2>
                    <p> اللہ آپ کو خوشیوں، مسکراہٹوں، کامیابیوں اور محبتوں سے نوازے۔ 

Happy Birthday once again, Laraib! Allah kare yeh saal aap ki zindagi ka sab se behtareen saal ho. Aap hamesha muskurayein, chamkain aur khush rahein.</p>
                </div>
            </div>
            <div class="body"></div>
        </div>

        <div class="controls">
            <button class="btn" onclick="openEnvelope(7)">Open Card</button>
            <button class="btn secondary" onclick="skipOpen(7)">Skip</button>
        </div>

        <audio id="bgMusic" src="assets/ma_agar_kahon_tum_sa_haseen.mp3" loop preload="auto" aria-hidden="true"></audio>
    </div>
</section>

<section id="sec8" class="section" aria-label="Section 8">
    <div class="card-wrap" style="align-items:center">
        <div class="envelope" data-index="8" onclick="openEnvelope(8)">
            <div class="flap"></div>
            <div class="letter" role="article" aria-labelledby="title8">
                <div class="card-content">
                    <h2 id="title8">🎂 Surprise & Celebration</h2>
                    <p>Happy Birthday once again, Laraib! Press "**Next**" to cut the cake 🎉</p>
                </div>
            </div>
            <div class="body"></div>
        </div>

        <div class="controls" style="margin-bottom:14px;">
            <button class="btn" onclick="openEnvelope(8)">Open Card</button>
            <button class="btn secondary" onclick="skipOpen(8)">Skip</button>
        </div>
    </div>
</section>

<section id="sec9" class="section" aria-label="Section 9 - Cake Cutting">
    <div class="card-wrap" style="align-items:center; justify-content: center;">
        <h2 style="color:var(--accent-2); margin-bottom:10px;">Let's Cut the Cake!</h2>

        <div id="cake-container">
            <img id="cake" src="assets/cake.png" alt="Birthday cake" />
            </div>
    
        <div style="margin-top:20px; padding-bottom: 20px;">
            <button id="cutBtn" class="btn" onclick="cutCake()">**Cut Cake 🎂**</button>
        </div>
    
        <audio id="finalMusic" src="assets/happy_birthday_song.mp3" preload="auto" aria-hidden="true"></audio>
        <audio id="sliceSound" src="assets/cake_cut.mp3" preload="auto" aria-hidden="true"></audio>
    </div>
</section>

<h1 id="celebrationText">Happy Birthday Laraib!</h1>

<script>
    const totalSections = 9;
    let current = 1; 
    let bgStarted = false;
    let confettiLoopTimer = null; 
    const CELEBRATION_DURATION = 14000; 

    function showSection(i){
        // Ensure all sections are checked, including the intro
        const allSections = document.querySelectorAll('.section');
        allSections.forEach((el, index) => {
            const sectionIndex = (el.id === 'intro') ? 1 : parseInt(el.id.replace('sec', ''));
            
            if (sectionIndex === i) {
                el.classList.add('active');
            } else {
                el.classList.remove('active');
            }
        });
        current = i;
    }

    // Tries to start the background music
    function tryStartBgMusic() {
        const bg = document.getElementById('bgMusic');
        if(bg && !bgStarted){
            bg.play().then(() => {
                bgStarted = true;
            }).catch(err => {
                console.warn('bgMusic play failed (mobile restriction likely):', err);
            });
        }
    }

    // FIX: Open Door logic with the correct class name for the intro element
    function openDoor(){
        const introSection = document.getElementById('intro');
        
        // 1. Add the door-open class to the section itself for CSS
        introSection.classList.add('door-open');
        
        // 2. Proceed to the first envelope (Section 2)
        setTimeout(() => {
            showSection(2); 
        }, 2200); 
    }

    function openEnvelope(idx){
        // *** START MUSIC ON FIRST USER INTERACTION (SECTION 2) ***
        if (idx === 2) {
            tryStartBgMusic();
        }
        
        const env = document.querySelector(`#sec${idx} .envelope`);
        if(!env) return;

        env.classList.add('opened');

        const controls = env.closest('.card-wrap').querySelector('.controls');
        if(controls){
            setTimeout(()=> {
                controls.innerHTML = `<div><button class="btn" onclick="goNext(${idx})">Next →</button></div>`;
            }, 600);
        }
    }

    function skipOpen(idx){
        // *** START MUSIC ON FIRST USER INTERACTION (SECTION 2) ***
        if (idx === 2) {
            tryStartBgMusic();
        }

        const env = document.querySelector(`#sec${idx} .envelope`);
        if(env) env.classList.add('opened');
        const controls = env.closest('.card-wrap').querySelector('.controls');
        if(controls){
            controls.innerHTML = `<div><button class="btn" onclick="goNext(${idx})">Next →</button></div>`;
        }
    }

    function goNext(fromIdx){
        let next = fromIdx + 1;
        if(next > totalSections) next = totalSections;
        showSection(next);
    }

    function cutCake(){
        const cake = document.getElementById('cake');
        const slice = document.getElementById('sliceSound');
        const final = document.getElementById('finalMusic');
        const celebrationText = document.getElementById('celebrationText');
        const btn = document.getElementById('cutBtn');

        if(btn){ btn.disabled = true; btn.innerHTML = 'Celebrating...'; btn.style.opacity = .7; }

        if(slice){ slice.currentTime = 0; slice.play().catch(()=>{}); }
        
        if(final){
            // Stop the BG music and start the final song
            document.getElementById('bgMusic').pause();
            document.getElementById('bgMusic').currentTime = 0;
            
            final.currentTime = 0;
            final.play().catch(e => console.warn('finalMusic play failed', e));
        }

        // Show the celebration text (now just a glowing effect)
        celebrationText.style.opacity = '1';

        // Cake slice animation (no knife involved)
        setTimeout(()=>{
            cake.style.transform = 'scale(.96)';
            setTimeout(()=>{
                cake.src = 'assets/cake-sliced.png';
                cake.style.transform = 'scale(1)';
            }, 100);
        }, 600);


        // Start continuous confetti loop
        startConfettiLoop();

        // End celebration after CELEBRATION_DURATION
        setTimeout(()=>{
            // Clear confetti loop
            clearInterval(confettiLoopTimer); 

            celebrationText.style.opacity = '0';
            if(final){
                final.pause();
                final.currentTime = 0;
            }
            showClosingOverlay();
        }, CELEBRATION_DURATION); 
    }

    function startConfettiLoop() {
        launchConfetti(80);

        confettiLoopTimer = setInterval(() => {
            launchConfetti(20); 
        }, 500);
    }

    function launchConfetti(n){
        const colors = ['#f94144','#ff69b4','#f9c74f','#90be6d','#577590','#b983ff','#ffb3c6'];
        for(let i=0;i<n;i++){
            const el = document.createElement('div');
            el.className = 'confetti';
            el.style.left = (Math.random()*100) + 'vw';
            el.style.background = colors[Math.floor(Math.random()*colors.length)];
            el.style.width = (6 + Math.random()*14) + 'px';
            el.style.height = (8 + Math.random()*16) + 'px';
            el.style.top = '-20px';
            el.style.borderRadius = (Math.random()>0.5? '2px':'50%');
            el.style.opacity = 1;
            el.style.transform = `rotate(${Math.random()*360}deg)`;
            el.style.transition = `transform ${2.5 + Math.random()*1.5}s linear, top ${2.5 + Math.random()*1.5}s linear, opacity 1s ease`;
            document.body.appendChild(el);

            setTimeout(()=>{
                el.style.top = (70 + Math.random()*30) + 'vh';
                el.style.transform = `translateY(${120 + Math.random()*60}vh) rotate(${Math.random()*720}deg)`;
            }, 20);

            setTimeout(()=> el.remove(), 4200 + Math.random()*800);
        }
    }

    function showClosingOverlay(){
        const overlay = document.createElement('div');
        overlay.style.position = 'fixed';
        overlay.style.inset = '0';
        overlay.style.display = 'flex';
        overlay.style.alignItems = 'center';
        overlay.style.justifyContent = 'center';
        overlay.style.background = 'rgba(0,0,0,0.85)';
        overlay.style.color = '#fff';
        overlay.style.zIndex = 99999;
        overlay.style.fontSize = '24px';
        overlay.style.fontFamily = 'Segoe UI, Roboto, Arial, sans-serif';
        overlay.style.opacity = '0';
        overlay.style.transition = 'opacity .5s';
        overlay.innerHTML = '<h1>🎉 Happy Birthday Laraib! 🎉</h1><p style="font-size: 16px;">Wish you all the best.</p>';
        overlay.style.flexDirection = 'column';
        overlay.style.textAlign = 'center';
        
        document.body.appendChild(overlay);
        requestAnimationFrame(()=> overlay.style.opacity = '1');

        setTimeout(()=> {
            overlay.style.opacity = '0';
            setTimeout(()=> overlay.remove(), 600);
        }, 4000);
    }

    (function init(){
        showSection(1);
        // Automatic door opening is still here
        setTimeout(openDoor, 50); 
    })();
</script>
</body>
</html>
