<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Laraib</title>
<style>
  html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    overflow: hidden;
  }
  .section {
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    color: #fff;
    padding: 20px;
    position: absolute;
    top: 0;
    left: 0;
    opacity: 0;
    transition: opacity 1s, transform 1s;
  }
  .active {
    opacity: 1;
    transform: translateY(0);
    z-index: 2;
  }
  .hidden {
    transform: translateY(50px);
  }
  .btn-next {
    margin-top: 40px;
    padding: 12px 24px;
    border: none;
    border-radius: 8px;
    background: #4b2e83;
    color: #fff;
    font-size: 16px;
    cursor: pointer;
  }
  /* Background colors for each section */
  #sec1 { background: linear-gradient(120deg,#a1c4fd,#c2e9fb); }
  #sec2 { background: linear-gradient(120deg,#fbc2eb,#a6c1ee); }
  #sec3 { background: linear-gradient(120deg,#fad0c4,#ffd1ff); }
  #sec4 { background: linear-gradient(120deg,#f6d365,#fda085); }
  #sec5 { background: linear-gradient(120deg,#84fab0,#8fd3f4); }
</style>
</head>
<body>

<div id="sec1" class="section active">
  <h1 style="font-size:48px;">🌸 Happy Birthday, Laraib! 🎉✨</h1>
  <button class="btn-next" onclick="nextSection()">Next</button>
</div>

<div id="sec2" class="section hidden">
  <h2>🌼 Aap Jaisi Khoobsurat Insaan</h2>
  <p>Aap jaisi achi, pyari, seedhi aur sachi insaan ko hamesha duniya ki sab se behtareen cheezein milni chahiye. Aapka ikhlaq, lehja aur soch aap ko sab se alag banati hain.</p>
  <button class="btn-next" onclick="nextSection()">Next</button>
</div>

<div id="sec3" class="section hidden">
  <h2>📸 Yaadein Jo Reh Gayi</h2>
  <p>Mujhe abhi tak woh din yaad hai jab hum shed se wapis aa rahe thay aur barish ho rahi thi. Mere mana karne ke bawajood aap ne paani me jump kiya tha. Us moment ki khushi aur masoomiyat abhi tak yaad hai.</p>
  <p>Aur phir… aap ke haath ka banaya hua pulao aur custard — abhi tak uski khushboo yaad aati hai.</p>
  <button class="btn-next" onclick="nextSection()">Next</button>
</div>

<div id="sec4" class="section hidden">
  <h2>✨ Aap Ki Aankhein</h2>
  <p>Aap ki aankhein… woh gehra kaala rang jo sirf khoobsurat nahi balkay bohot expressive bhi hai. Jaise inme koi purani kahani, koi raaz, koi narmi chhupi ho.</p>
  <button class="btn-next" onclick="nextSection()">Next</button>
</div>

<div id="sec5" class="section hidden">
  <h2>🤲 Duaen & Motivation</h2>
  <p>Allah aap ke tamam goals aasaan kare. Aap jahan bhi jaayein, izzat, mohabbat aur ache log milain. Aapka dil hamesha halka aur khush rahe.</p>
  <p>Laraib… aap intelligent hain aur sincere bhi. Sirf yaad rakhein: <strong>“Jahan niyat saaf hoti hai, wahan raasta ban hi jaata hai.”</strong></p>
  <p><strong>“Aap kamzor nahi — bas nazuk dil ki hain. Aur nazuk dil wale hi asli strong hote hain.”</strong></p>
  <p>Happy Birthday once again! 🌸✨</p>
</div>

<script>
  let current = 1;
  function nextSection() {
    document.getElementById('sec' + current).classList.remove('active');
    document.getElementById('sec' + current).classList.add('hidden');
    current++;
    if(current <= 5){
      document.getElementById('sec' + current).classList.add('active');
      document.getElementById('sec' + current).classList.remove('hidden');
    }
  }
</script>

</body>
</html>
