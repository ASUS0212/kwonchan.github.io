# kwonchan.github.io
<html lang="ko">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>내 링크 허브</title>
  <meta name="description" content="내가 자주 쓰는 사이트로 바로 이동하는 링크 허브" />
  <link rel="icon" type="image/png" href="/favicon.png">
  <style>
    :root{
      --bg: #0b0f17;
      --card: #121826;
      --muted: #9aa4b2;
      --text: #e5e7eb;
      --accent: #60a5fa;
      --ring: 0 0 0 3px rgba(96,165,250,.35);
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, "Noto Sans KR", Arial, "Apple Color Emoji","Segoe UI Emoji";
      color:var(--text); background: radial-gradient(1200px 800px at 10% -10%, #1a2336 0%, rgba(11,15,23,0) 60%), var(--bg);
    }
    .wrap{max-width:980px; margin:0 auto; padding:40px 20px 80px}
    header{display:flex; align-items:center; justify-content:space-between; gap:12px; margin-bottom:24px}
    .brand{display:flex; align-items:center; gap:12px}
    .brand .logo{width:44px;height:44px; display:grid; place-items:center; background:#162036; border:1px solid #242f49; border-radius:14px}
    .brand h1{font-size:clamp(20px, 2.5vw, 28px); margin:0}
    .desc{color:var(--muted); font-size:14px; margin-top:4px}

    .toolbar{display:flex; gap:10px; flex-wrap:wrap}
    .search{position:relative; flex:1 1 260px}
    .search input{
      width:100%; padding:12px 40px 12px 14px; border-radius:12px; border:1px solid #26324e; background:#0f1524; color:var(--text);
    }
    .search input:focus{outline:none; box-shadow:var(--ring); border-color:#35508a}
    .search .icon{position:absolute; right:10px; top:50%; transform:translateY(-50%); opacity:.7}

    .add-btn, .mode-btn{
      padding:12px 14px; border-radius:12px; border:1px solid #26324e; background:#0f1524; color:var(--text); cursor:pointer;
    }
    .add-btn:focus, .mode-btn:focus{outline:none; box-shadow:var(--ring)}

    .grid{display:grid; grid-template-columns: repeat(auto-fill, minmax(220px, 1fr)); gap:14px; margin-top:18px}
    .card{
      border:1px solid #202a44; 
      background:linear-gradient(180deg, #121a2b, #0f1524); 
      border-radius:16px; 
      padding:16px; 
      display:flex; 
      gap:12px; 
      align-items:center; 
      text-decoration:none; 
      color:inherit; 
      transition: transform .12s ease, box-shadow .12s ease, border-color .12s ease;
    }
    .card:hover{transform: translateY(-2px); box-shadow: 0 6px 24px rgba(0,0,0,.3); border-color:#2a3a63}
    .iconbox{width:40px;height:40px;border-radius:10px; display:grid; place-items:center; background:#0c1221; border:1px solid #243257; font-size:20px}
    .meta{min-width:0}
    .title{font-weight:700; font-size:15px; white-space:nowrap; overflow:hidden; text-overflow:ellipsis}
    .url{color:var(--muted); font-size:12px; white-space:nowrap; overflow:hidden; text-overflow:ellipsis}

    .card:focus{outline:2px solid var(--accent); outline-offset:2px}

    footer{margin-top:36px; color:var(--muted); font-size:12px; text-align:center}

    body.light{--bg:#f6f7fb; --card:#ffffff; --text:#0c1220; --muted:#5b6472; background:#f6f7fb}
    body.light .brand .logo{background:#ffffff; border-color:#e5e7eb}
    body.light .search input, body.light .add-btn, body.light .mode-btn{background:#ffffff; border-color:#e5e7eb}
    body.light .card{background:#ffffff; border-color:#eaeef3}
    body.light .iconbox{background:#f5f7fb; border-color:#e2e8f0}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="brand">
        <div class="logo" aria-hidden="true">🔗</div>
        <div>
          <h1>내 링크 허브</h1>
          <p class="desc">자주 가는 사이트를 한 곳에 모아 바로 연결하세요.</p>
        </div>
      </div>
      <div class="toolbar">
        <div class="search" role="search">
          <input id="q" type="search" placeholder="링크 검색 (예: 유튜브, 네이버)" aria-label="링크 검색" />
          <span class="icon">🔍</span>
        </div>
        <button class="mode-btn" id="modeBtn" aria-pressed="false" aria-label="테마 전환">🌙 다크 모드</button>
        <button class="add-btn" id="addBtn" aria-label="링크 추가">＋ 링크</button>
      </div>
    </header>

    <main>
      <div id="grid" class="grid" aria-live="polite">
        <a class="card" href="http://kwonchan.kro.kr/" target="_blank" rel="noopener noreferrer" tabindex="0">
          <div class="iconbox">🌐</div>
          <div class="meta">
            <div class="title">공유기 설정</div>
            <div class="url">wasdbnm.kro.kr</div>
          </div>
        </a>
        <a class="card" href="https://bumdaeng.com/" target="_blank" rel="noopener noreferrer" tabindex="0">
          <div class="iconbox">🐾</div>
          <div class="meta">
            <div class="title">Bumdaeng Nas</div>
            <div class="url">bumdaeng.com</div>
          </div>
        </a>
        <a class="card" href="https://swjb-h.goesw.kr/index.do" target="_blank" rel="noopener noreferrer" tabindex="0">
          <div class="iconbox">🏫</div>
          <div class="meta">
            <div class="title">수원정보과학고</div>
            <div class="url">swjb-h.goesw.kr</div>
          </div>
        </a>
        <a class="card" href="http://www.xn--s39aj90b0nb2xw6xh.kr/" target="_blank" rel="noopener noreferrer" tabindex="0">
          <div class="iconbox">🇰🇷</div>
          <div class="meta">
            <div class="title">컴시간알리미</div>
            <div class="url">xn--s39aj90b0nb2xw6xh.kr</div>
          </div>
        </a>
        <!-- 추가: 유튜브 -->
        <a class="card" href="https://www.youtube.com/" target="_blank" rel="noopener noreferrer" tabindex="0">
          <div class="iconbox">▶️</div>
          <div class="meta">
            <div class="title">유튜브</div>
            <div class="url">youtube.com</div>
          </div>
        </a>
        <!-- 추가: 유튜브 뮤직 -->
        <a class="card" href="https://music.youtube.com/" target="_blank" rel="noopener noreferrer" tabindex="0">
          <div class="iconbox">🎵</div>
          <div class="meta">
            <div class="title">유튜브 뮤직</div>
            <div class="url">music.youtube.com</div>
          </div>
        </a>
        <!-- 추가: 사운드클라우드 -->
        <a class="card" href="https://soundcloud.com/" target="_blank" rel="noopener noreferrer" tabindex="0">
          <div class="iconbox">☁️</div>
          <div class="meta">
            <div class="title">사운드클라우드</div>
            <div class="url">soundcloud.com</div>
          </div>
        </a>
        <!-- 추가: 스포티파이 -->
        <a class="card" href="https://spotify.com/" target="_blank" rel="noopener noreferrer" tabindex="0">
          <div class="iconbox">🟢</div>
          <div class="meta">
            <div class="title">스포티파이</div>
            <div class="url">spotify.com</div>
          </div>
        </a>
      </div>
    </main>

    <footer>
      <p>© <span id="year"></span> 내 링크 허브 — 안전하게 새 창으로 열림</p>
    </footer>
  </div>

  <script>
    // 연도 자동 표시
    document.getElementById('year').textContent = new Date().getFullYear();

    // 모드 버튼 및 테마 변경
    const modeBtn = document.getElementById('modeBtn');
    function updateModeBtn(){
      const isLight = document.body.classList.contains('light');
      modeBtn.textContent = isLight ? '🌞 라이트 모드' : '🌙 다크 모드';
      modeBtn.setAttribute('aria-pressed', isLight ? 'true' : 'false');
    }
    // 초기 모드 상태 반영
    const savedMode = localStorage.getItem('theme');
    if(savedMode === 'light'){
      document.body.classList.add('light');
    }
    updateModeBtn();

    modeBtn.addEventListener('click', () => {
      document.body.classList.toggle('light');
      localStorage.setItem('theme', document.body.classList.contains('light') ? 'light' : 'dark');
      updateModeBtn();
    });

    // 검색 필터링
    const q = document.getElementById('q');
    const grid = document.getElementById('grid');
    q.addEventListener('input', () => {
      const term = q.value.toLowerCase();
      for (const card of grid.querySelectorAll('.card')) {
        const title = card.querySelector('.title').textContent.toLowerCase();
        const url = card.querySelector('.url').textContent.toLowerCase();
        if (title.includes(term) || url.includes(term)) {
          card.style.display = '';
        } else {
          card.style.display = 'none';
        }
      }
    });
  </script>
</body>
</html>
