<!doctype html>
<html lang="hi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>For You ❤️</title>
  <style>
    body{font-family: system-ui, -apple-system, Roboto, "Noto Sans", sans-serif; background:#fff7f9; color:#222; margin:0; padding:0; display:flex; align-items:center; justify-content:center; min-height:100vh}
    .card{width:95%; max-width:720px; background:white; border-radius:16px; box-shadow:0 10px 30px rgba(0,0,0,0.08); padding:28px}
    h1{margin:0 0 8px; font-size:28px}
    p.lead{margin:0 0 18px; font-size:16px}
    .photo{width:100%; height:300px; border-radius:12px; object-fit:cover; background:linear-gradient(135deg,#ffd6e0,#fff1f5)}
    .poem{background:#fff0f6; padding:14px; border-radius:10px; margin-top:16px}
    .btn{display:inline-block; margin-top:18px; padding:10px 16px; border-radius:10px; text-decoration:none; background:#ff5773; color:white}
    .secret{display:none; margin-top:16px}
  </style>
</head>
<body>
  <div class="card">
    <h1>For my favourite person 💖</h1>
    <p class="lead">Yeh chhota sa surprise tumhare liye. Agar tum ready ho, "Open Surprise" button dabao.</p>

    <!-- Replace the src with your photo filename or a public image URL -->
    <img class="photo" id="photo" src="https://images.unsplash.com/photo-1511988617509-a57c8a288659?q=80&w=1400&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder" alt="Our photo">

    <div class="poem">
      <strong>Ek chhota sa sher —</strong>
      <p>"Tumhari ek muskaan se subah roshan ho jaati hai,<br>
      Tumhari ek baat se din mera halka sa meetha ho jaata hai.<br>
      Har chhoti khushi tumse judi hai — bas yun hi saath rehna."</p>
    </div>

    <a class="btn" id="openBtn" href="#">Open Surprise</a>

    <div class="secret" id="secret">
      <h3>Surprise! 🎉</h3>
      <p>Maine tumhare liye ek chhota playlist banaya hai aur ek video clip. Tumhara favourite line: <em>"Tum ho to sab perfect lagta hai"</em></p>
      <p>Message: <strong>"Mujhe tum chahiye — bas yunhi saath"</strong></p>
      <p><small>Yeh page locally chal raha hai. Agar chaho to main ise host karne ka step-by-step bata dunga.</small></p>
    </div>

  </div>

  <script>
    const btn = document.getElementById('openBtn');
    const secret = document.getElementById('secret');
    btn.addEventListener('click', function(e){
      e.preventDefault();
      secret.style.display = 'block';
      // thoda animation
      secret.style.opacity = 0;
      let op = 0;
      const t = setInterval(()=>{ op += 0.06; secret.style.opacity = op; if(op>=1) clearInterval(t); },16);
      // change button text
      btn.textContent = 'Hope you liked it ❤';
    });
  </script>
</body>
</html>
