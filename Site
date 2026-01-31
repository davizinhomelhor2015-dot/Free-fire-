<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Free Fire — Mundo do Melhor</title>
  <meta name="description" content="Página interativa responsiva Free Fire — Mundo do Melhor. Projetada para celular e desktop." />

  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Exo+2:wght@400;600;700;900&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg-1:#070606;
      --bg-2:#1a0f00;
      --accent:#FF6B00;
      --accent-2:#FFB84D;
      --gold:#FFD700;
      --radius:16px;
      --max-width:1100px;
    }

    *{box-sizing:border-box}
    html,body{
      height:100%;
      margin:0;
      font-family:'Exo 2',system-ui,-apple-system,Segoe UI,Roboto,Arial
    }

    body{
      background:linear-gradient(160deg,var(--bg-1) 0%, #120700 40%, var(--bg-2) 100%);
      color:#fff;
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:20px
    }

    .wrap{
      width:100%;
      max-width:var(--max-width);
      display:grid;
      gap:20px;
      grid-template-columns:1fr;
      align-items:center
    }

    @media(min-width:900px){
      .wrap{grid-template-columns:520px 1fr}
    }

    .panel{
      background:linear-gradient(180deg,rgba(255,107,0,0.06),rgba(255,140,0,0.03));
      border-radius:var(--radius);
      padding:26px;
      border:1px solid rgba(255,107,0,0.08);
      box-shadow:0 12px 40px rgba(0,0,0,0.6);
      display:flex;
      flex-direction:column;
      gap:14px;
      position:relative;
      overflow:hidden
    }

    .ribbon{
      position:absolute;
      right:-40px;
      top:18px;
      transform:rotate(22deg);
      background:linear-gradient(90deg,var(--accent),var(--accent-2));
      color:#120b00;
      padding:9px 86px;
      font-weight:900;
      border-radius:8px;
      letter-spacing:2px
    }

    .logo{display:flex;justify-content:center}
    .brand{
      font-weight:900;
      color:var(--accent);
      font-size:2rem;
      letter-spacing:4px
    }

    h1{margin:4px 0}
    .lead{color:var(--gold);font-weight:700}

    .meta{display:flex;gap:10px;flex-wrap:wrap}
    .pill{
      background:rgba(255,107,0,0.08);
      padding:8px 12px;
      border-radius:999px;
      font-weight:700;
      color:var(--accent)
    }

    .small-footer{
      margin-top:auto;
      text-align:center;
      color:var(--gold);
      font-weight:700
    }

    .game{
      background:rgba(0,0,0,0.55);
      border-radius:var(--radius);
      padding:24px;
      border:1px solid rgba(255,255,255,0.05);
      box-shadow:0 12px 40px rgba(0,0,0,0.6);
      display:flex;
      flex-direction:column;
      align-items:center;
      justify-content:center;
      min-height:320px;
      position:relative
    }

    .subtitle{color:var(--gold);font-weight:800}
    .desc{text-align:center;color:#ddd;margin-bottom:14px}

    .btn{
      padding:16px 36px;
      background:linear-gradient(135deg,var(--accent),#FF8C00);
      border-radius:999px;
      border:3px solid var(--gold);
      font-weight:900;
      cursor:pointer
    }

    .btn.ready{
      background:linear-gradient(90deg,var(--gold),#FFA500)
    }

    .counter{
      margin-top:12px;
      padding:10px 16px;
      border-radius:999px;
      border:2px solid rgba(255,107,0,0.2);
      color:var(--gold);
      font-weight:800
    }

    .reveal{
      display:none;
      text-align:center;
      padding:22px;
      border-radius:12px;
      border:3px solid var(--accent);
      margin-top:16px
    }

    .reveal.show{display:block}

    .decor{
      position:absolute;
      inset:0;
      display:flex;
      align-items:center;
      justify-content:center;
      opacity:.12;
      font-size:80px;
      pointer-events:none
    }
  </style>
</head>

<body>
  <main class="wrap">

    <section class="panel" aria-labelledby="titulo">
      <div class="ribbon" aria-hidden="true">MUNDO DO MELHOR</div>

      <div class="logo"><div class="brand">FREE FIRE</div></div>

      <div>
        <h1 id="titulo">Oi Mary! 🔥</h1>
        <p class="lead">Bem-vinda ao Mundo do mais capudo</p>
      </div>

      <div class="meta">
        <div class="pill">Explorar</div>
        <div class="pill">Treinar</div>
        <div class="pill">Booyah!</div>
      </div>

      <div class="small-footer">🎮 Free Fire — Mundo do Melhor</div>
    </section>

    <section class="game" aria-label="Área interativa">
      <div class="decor">🔥🎆</div>

      <div>
        <div class="subtitle">Pronto pra brincar?</div>
        

        <button id="escapeBtn" class="btn">
          🎯 <span id="btnLabel">CLIQUE AQUI</span> 🎯
        </button>

        <div   aria-live="polite">
        
        </div>

        <div id="reveal" class="reveal" aria-hidden="true">
          <h2>CAPTURADO! 🎯</h2>
          <div style="font-size:2rem">BOOYAH! 🏆</div>
          <p><strong>Vitor Sant:</strong> Oi meu assistente!</p>
          <button id="reset" class="btn">JOGAR NOVAMENTE</button>
        </div>
      </div>
    </section>

  </main>

  <script>
    (function(){
      const MAX = 5;
      let count = 0;

      const btn = document.getElementById('escapeBtn');
      const btnLabel = document.getElementById('btnLabel');
      const countText = document.getElementById('countText');
      const reveal = document.getElementById('reveal');
      const reset = document.getElementById('reset');

      function update(){
        countText.textContent = `Fugas: ${count}/${MAX}`;
      }

      function move(){
        const x = Math.random() * (window.innerWidth - 100);
        const y = Math.random() * (window.innerHeight - 100);
        btn.style.position = 'fixed';
        btn.style.left = x + 'px';
        btn.style.top = y + 'px';
      }

      btn.addEventListener('mouseenter', ()=>{
        if(count < MAX){
          count++;
          move();
          update();
          if(count === MAX){
            btn.classList.add('ready');
            btnLabel.textContent = 'AGORA SIM!';
          }
        }
      });

      btn.addEventListener('click', ()=>{
        if(count >= MAX){
          reveal.classList.add('show');
          reveal.setAttribute('aria-hidden','false');
          btn.style.display='none';
        }
      });

      reset.addEventListener('click', ()=>{
        count = 0;
        update();
        reveal.classList.remove('show');
        reveal.setAttribute('aria-hidden','true');
        btn.style.display='';
        btn.style.position='';
        btn.classList.remove('ready');
        btnLabel.textContent='CLIQUE AQUI';
      });

      update();
    })();
  </script>
</body>
</html>
