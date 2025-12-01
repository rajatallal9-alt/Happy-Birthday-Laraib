<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Happy Birthday Laraib — Card</title>
<style>
  :root{
    --accent-1: #8b2eff;
    --accent-2: #4b2e83;
    --card-bg: #fff7ff;
  }

  html,body{
    height:100%;
    margin:0;
    font-family: "Segoe UI", Roboto, Arial, sans-serif;
    background: linear-gradient(180deg,#f8f0ff 0%, #fff 60%), url('assets/bg.jpg') center/cover no-repeat;
    -webkit-font-smoothing:antialiased;
    -moz-osx-font-smoothing:grayscale;
    color:#222;
    overflow:hidden;
  }

  /* Generic layout for full-screen sections */
  .section {
    position:absolute;
    inset:0;
    display:flex;
    justify-content:center;
    align-items:center;
    padding:20px;
    box-sizing:border-box;
    opacity:0;
    transform: translateY(24px);
    transition: opacity .6s ease, transform .6s ease;
    pointer-events:none;
  }
  .section.active{
    opacity:1;
    transform: translateY(0);
    pointer-events:auto;
    z-index:5;
  }

  /* Envelope container (made bigger to fit longer text) */
  .card-wrap{
    width:100%;
    max-width:920px;
    display:flex;
    flex-direction:column;
    align-items:center;
    gap:18px;
  }

  /* ENVELOPE (pure CSS) - enlarged */
  .envelope {
    width: 720px;
    max-width: 94%;
    height: 420px; /* increased height */
    position: relative;
    perspective: 1400px;
  }

  /* Body/back of envelope */
  .envelope .body {
    position:absolute;
    inset:0;
    border-radius:12px;
    background: linear-gradient(180deg, #fff, #fff7fb);
    box-shadow: 0 18px 60px rgba(20,10,60,0.16);
    overflow:visible;
    display:flex;
    align-items:center;
    justify-content:center;
    padding:28px;
    box-sizing:border-box;
  }

  /* Flap (front triangle) */
  .envelope .flap {
    position:absolute;
    top:0;
    left:0;
    width:100%;
    height:58%;
    transform-origin: top center;
    background: linear-gradient(180deg,#ffd7f6,#ffecff);
    border-top-left-radius:14px;
    border-top-right-radius:14px;
    box-shadow: 0 12px 40px rgba(120,60,160,0.12);
    transform-style: preserve-3d;
    transition: transform .8s cubic-bezier(.2,.9,.3,1);
    backface-visibility: hidden;
    z-index:8;
    display:flex;
    align-items:flex-end;
    justify-content:center;
  }

  .envelope .flap::after{
    content:"";
    display:block;
    width:78%;
    height:26px;
    margin-bottom:22px;
    background: linear-gradient(90deg, rgba(75,46,131,0.08), rgba(139,46,255,0.12));
    border-radius:6px;
    opacity:.95;
  }

  /* Letter inside envelope (made taller and scrollable) */
  .envelope .letter {
    position:absolute;
    left:6%;
    width:88%;
    height:72%;
    top:16%;
    background: linear-gradient(180deg,#fff,#fffefc);
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
    overflow:auto; /* allow scrolling for long text */
    scrollbar-width: thin;
  }

  /* When envelope is opened */
  .envelope.opened .flap {
    transform: rotateX(-180deg) translateY(-6%);
  }
  .envelope.opened .letter {
    transform: translateY(-6px) scale(1);
    opacity:1;
  }

  /* Message content inside the letter */
  .card-content{
    width:100%;
    color:var(--accent-2);
    text-align:left;
  }
  .card-content h1,
  .card-content h2 {
    margin:0 0 8px 0;
    font-size:24px;
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

  /* Buttons */
  .controls{
    display:flex;
    gap:12px;
    margin-top:8px;
  }
  .btn{
    appearance:none;
    border:0;
    padding:10px 18px;
    border-radius:10px;
    background:linear-gradient(90deg,var(--accent-1), #5b18d6);
    color:#fff;
    cursor:pointer;
    font-size:16px;
    box-shadow: 0 6px 18px rgba(91,24,214,0.18);
  }
  .btn.secondary{
    background:transparent;
    color:var(--accent-2);
    box-shadow:none;
    border:1px solid rgba(75,46,131,0.08);
  }

  /* Final cake helpers */
  #cake { max-width:40%; width:320px; transition: transform .4s ease; border-radius:14px; }
  #knife { width:130px; position:absolute; left:-300px; top:40%; transform:rotate(-18deg); transition:left .7s, transform .4s; opacity:0; }

  .confetti { position:fixed; width:10px; height:14px; z-index:9999; pointer-events:none; }

  @media (max-width:900px){
    .envelope { width: 92%; height: 420px; }
    .envelope .letter { height:70%; top:18%; padding:16px; }
    .card-content p{ font-size:16px; }
    #cake { width:260px; }
    #knife { width:100px; left:-200px; }
  }

  @media (max-width:520px){
    .envelope{ height:480px; } /* allow more vertical space on narrow screens */
    .envelope .letter { height:72%; top:14%; }
    .card-content h1{ font-size:20px; }
    .card-content p{ font-size:15px; }
  }
</style>
</head>
<body>

<!-- Section 1 -->
<section id="sec1" class="section active" aria-label="Card 1">
  <div class="card-wrap">
    <div class="envelope" data-index="1" aria-hidden="false">
      <div class="flap" aria-hidden="true"></div>
      <div class="letter" role="article" aria-labelledby="title1">
        <div class="card-content">
          <h1 id="title1">✨ Happy Birthday, Laraib! ✨</h1>
          <p>Laraib… aaj ka din waqai bohot khaas hai. Main dil se dua karta hoon ke yeh din aap ki zindagi me naye raaste, naye mauqe, aur bohot sari khushiyan le kar aaye.</p>
          <div class="quote">"Aaj ka din waqai bohot khaas hai."</div>
        </div>
      </div>
      <div class="body" aria-hidden="true"></div>
    </div>

    <div class="controls">
      <button class="btn" onclick="openEnvelope(1)">Open Card</button>
      <button class="btn secondary" onclick="skipOpen(1)">Skip</button>
    </div>
  </div>
</section>

<!-- Section 2 -->
<section id="sec2" class="section" aria-label="Card 2">
  <div class="card-wrap">
    <div class="envelope" data-index="2">
      <div class="flap"></div>
      <div class="letter" role="article" aria-labelledby="title2">
        <div class="card-content">
          <h2 id="title2">🌼 Aap Jaisi Khoobsurat Insaan</h2>
          <p>Aap jaisi achi, pyari, seedhi aur sachi insaan ko hamesha duniya ki sab se behtareen cheezein milni chahiye. Aapka ikhlaq, lehja aur soch aap ko sab se alag banati hain.</p>
          <div class="quote">"Aap jaisi achi, pyari, seedhi aur sachi insaan ko hamesha duniya ki sab se behtareen cheezein milni chahiye. Aapka ikhlaq, lehja aur soch aap ko sab se alag banati hain"</div>
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

<!-- Section 3 -->
<section id="sec3" class="section" aria-label="Card 3">
  <div class="card-wrap">
    <div class="envelope" data-index="3">
      <div class="flap"></div>
      <div class="letter" role="article" aria-labelledby="title3">
        <div class="card-content">
          <h2 id="title3">📸 Yaadein Jo Reh Gayi</h2>
          <p>Mujhe abhi tak woh din yaad hai jab hum shed se wapis aa rahe thay aur barish ho rahi thi. Mere mana karne ke bawajood aap ne paani me jump kiya tha. Us moment ki khushi aur masoomiyat abhi tak yaad hai.

Aur phir… aap ke haath ka banaya hua pulao aur custard — abhi tak uski khushboo yaad aati hai. Shayad isliye kyun ke wo dil se bana tha. Aur bhi bohot sari choti choti yaadein hain, par yeh yaadein khud hi bohot khaas hain.</p>
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

<!-- Section 4 -->
<section id="sec4" class="section" aria-label="Card 4">
  <div class="card-wrap">
    <div class="envelope" data-index="4">
      <div class="flap"></div>
      <div class="letter" role="article" aria-labelledby="title4">
        <div class="card-content">
          <h2 id="title4">✨ Aap Ki Aankhein</h2>
          <p>Aap ki aankhein… woh gehra kaala rang jo sirf khoobsurat nahi balkay bohot expressive bhi hai. Jaise inme koi purani kahani, koi raaz, koi narmi chhupi ho. Kuch khoobsurtiyaan rang se nahi… rooh se hoti hain.

نور ہی نور سے مکھڑے پہ وہ نوری آنکھیں
اس کے انجیل سے چہرے پہ زبوری آنکھیں</p>
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

<!-- Section 5 -->
<section id="sec5" class="section" aria-label="Card 5">
  <div class="card-wrap">
    <div class="envelope" data-index="5">
      <div class="flap"></div>
      <div class="letter" role="article" aria-labelledby="title5">
        <div class="card-content">
          <h2 id="title5">🤲 Dil Se Dua</h2>
          <p>Allah aap ke tamam goals aasaan kare. Aap jahan bhi jaayein, izzat, mohabbat aur ache log milain. Aapka dil hamesha halka aur khush rahe. Ameen.</p>
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

<!-- Section 6 -->
<section id="sec6" class="section" aria-label="Card 6">
  <div class="card-wrap">
    <div class="envelope" data-index="6">
      <div class="flap"></div>
      <div class="letter" role="article" aria-labelledby="title6">
        <div class="card-content">
          <h2 id="title6">💡 Motivation For You</h2>
          <p>Laraib… aap intelligent hain aur sincere bhi. Potential bohot zyada hai. Sirf yaad rakhein: “Jahan niyat saaf hoti hai, wahan raasta ban hi jaata hai.”

“Aap kamzor nahi — bas nazuk dil ki hain. Aur nazuk dil wale hi asli strong hote hain.”</p>
        </div>
      </div>
      <div class="body"></div>
    </div>

    <div class="controls">
      <!-- openEnvelope(6, {startBg:true}) will start background music when this envelope is opened if you want; but user asked to start music when first envelope is opened -->
      <button class="btn" onclick="openEnvelope(6)">Open Card</button>
      <button class="btn secondary" onclick="skipOpen(6)">Skip</button>
    </div>
  </div>
</section>

<!-- Section 7 (End Note & Surprise) -->
<section id="sec7" class="section" aria-label="Card 7">
  <div class="card-wrap" style="align-items:center">
    <div class="envelope" data-index="7">
      <div class="flap"></div>
      <div class="letter" role="article" aria-labelledby="title7">
        <div class="card-content">
          <h2 id="title7">🎂 End Note</h2>
          <p>Happy Birthday once again, Laraib! Allah kare yeh saal aap ki zindagi ka sab se behtareen saal ho. Aap hamesha muskurayein, chamkain aur khush rahein. Aap jaisi log zindagi me gift hote hain — rare aur beautiful. 🌸✨</p>
        </div>
      </div>
      <div class="body"></div>
    </div>

    <div class="controls" style="margin-bottom:14px;">
      <button class="btn" onclick="openEnvelope(7)">Open Card</button>
      <button class="btn secondary" onclick="skipOpen(7)">Skip</button>
    </div>

    <div style="position:relative; width:100%; display:flex; justify-content:center; align-items:center; gap:18px;">
      <img id="knife" src="assets/knife.png" alt="" aria-hidden="true" />
      <img id="cake" src="assets/cake.png" alt="Birthday cake" />
    </div>

    <div style="margin-top:16px;">
      <button id="cutBtn" class="btn" onclick="cutCake()">Cut Cake 🎂</button>
    </div>

    <!-- background and final audios -->
    <audio id="bgMusic" src="assets/ma_agar_kahon_tum_sa_haseen.mp3" loop preload="auto" aria-hidden="true"></audio>
    <audio id="finalMusic" src="assets/happy_birthday_song.mp3" preload="auto" aria-hidden="true"></audio>
    <audio id="sliceSound" src="assets/cake_cut.mp3" preload="auto" aria-hidden="true"></audio>
  </div>
</section>

<script>
  // Section navigation + envelope logic
  const totalSections = 7;
  let current = 1;
  let bgStarted = false;

  function showSection(i){
    for(let s=1;s<=totalSections;s++){
      const el = document.getElementById('sec'+s);
      if(!el) continue;
      if(s === i) el.classList.add('active');
      else el.classList.remove('active');
    }
    current = i;
  }

  // When openEnvelope is called:
  // - animate envelope open
  // - start bg music only when the first envelope (index 1) is opened
  function openEnvelope(idx, opts = {}) {
    const env = document.querySelector(`#sec${idx} .envelope`);
    if(!env) return;

    // Start background music when the FIRST envelope (idx === 1) is opened.
    if(idx === 1 && !bgStarted) {
      const bg = document.getElementById('bgMusic');
      if(bg){
        bg.play().catch((err)=>{
          // If play fails (autoplay policy), show a console warning. The user opened the envelope via click so this should typically succeed.
          console.warn('bgMusic play failed:', err);
        });
        bgStarted = true;
      }
    }

    // Open the envelope visually
    env.classList.add('opened');

    // Replace controls with Next after a short delay so the letter is visible first
    const controls = env.closest('.card-wrap').querySelector('.controls');
    if(controls){
      setTimeout(()=> {
        controls.innerHTML = `<div><button class="btn" onclick="goNext(${idx})">Next →</button></div>`;
      }, 600);
    }
  }

  // Skip opening (immediately reveal and show Next)
  function skipOpen(idx){
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

  // Cake cutting sequence:
  // - play slice sound, swap cake to sliced, play finalMusic for exactly 10 seconds, launch confetti
  // - after 10 seconds stop finalMusic and automatically "close" final envelope
  function cutCake(){
    const knife = document.getElementById('knife');
    const cake = document.getElementById('cake');
    const slice = document.getElementById('sliceSound');
    const final = document.getElementById('finalMusic');
    const env = document.querySelector('#sec7 .envelope');
    const btn = document.getElementById('cutBtn');

    // Animate knife in
    knife.style.opacity = '1';
    knife.style.left = '50%';
    knife.style.transform = 'translateX(-160px) rotate(-8deg)';

    setTimeout(()=>{
      if(slice){ slice.currentTime = 0; slice.play().catch(()=>{}); }
      cake.style.transform = 'scale(.96)';
      setTimeout(()=>{
        cake.src = 'assets/cake-sliced.png';
        cake.style.transform = 'scale(1)';
      }, 240);
    },700);

    // Play final music and confetti for 10 seconds
    if(final){
      final.currentTime = 0;
      final.play().catch((e)=> console.warn('finalMusic play failed', e));
      launchConfetti(60);
      // After 10 seconds stop music and "close" final envelope
      setTimeout(()=>{
        final.pause();
        final.currentTime = 0;
        // close the envelope (flip flap back)
        if(env) env.classList.remove('opened');
        // optionally navigate back to first section or keep on final screen closed; we'll show a short thank you overlay
        showClosingOverlay();
      }, 10000);
    } else {
      // if no final audio, still confetti and close after 10s
      launchConfetti(60);
      setTimeout(()=>{
        if(env) env.classList.remove('opened');
        showClosingOverlay();
      }, 10000);
    }

    // hide knife later
    setTimeout(()=>{
      knife.style.opacity = '0';
      knife.style.left = '-300px';
    },2200);

    if(btn){ btn.disabled = true; btn.style.opacity = .7; }
  }

  function showClosingOverlay(){
    // A small thank-you overlay that fades in and then disappears
    const overlay = document.createElement('div');
    overlay.style.position = 'fixed';
    overlay.style.inset = '0';
    overlay.style.display = 'flex';
    overlay.style.alignItems = 'center';
    overlay.style.justifyContent = 'center';
    overlay.style.background = 'rgba(0,0,0,0.45)';
    overlay.style.color = '#fff';
    overlay.style.zIndex = 99999;
    overlay.style.fontSize = '28px';
    overlay.style.fontFamily = 'Segoe UI, Roboto, Arial, sans-serif';
    overlay.style.opacity = '0';
    overlay.style.transition = 'opacity .5s';
    overlay.textContent = '🎉 Thank you — Celebration complete! 🎉';
    document.body.appendChild(overlay);
    requestAnimationFrame(()=> overlay.style.opacity = '1');

    setTimeout(()=> {
      overlay.style.opacity = '0';
      setTimeout(()=> overlay.remove(), 600);
    }, 2500);
  }

  // Confetti generator
  function launchConfetti(n){
    const colors = ['#f94144','#f3722c','#f9c74f','#90be6d','#577590','#b983ff','#ffb3c6'];
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
      el.style.transition = `transform ${1.8 + Math.random()*1.4}s linear, top ${1.8 + Math.random()*1.4}s linear, opacity 1s ease`;
      document.body.appendChild(el);

      setTimeout(()=>{
        el.style.top = (70 + Math.random()*30) + 'vh';
        el.style.transform = `translateY(${120 + Math.random()*60}vh) rotate(${Math.random()*720}deg)`;
      }, 20);

      setTimeout(()=> el.remove(), 4200 + Math.random()*800);
    }
  }

  // Keyboard navigation: Right arrow/space to next, left to previous
  document.addEventListener('keydown', (e)=>{
    if(e.key === 'ArrowRight' || e.key === ' '){
      const next = Math.min(totalSections, current + 1);
      showSection(next);
    } else if(e.key === 'ArrowLeft'){
      const prev = Math.max(1, current - 1);
      showSection(prev);
    }
  });

  // Initialize
  (function init(){
    showSection(1);
  })();
</script>
</body>
</html>
