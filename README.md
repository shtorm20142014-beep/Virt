<!DOCTYPE html>
<html lang="kk">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>💎 NEXO SHOP 💎 - Black Russia</title>
  <style>
    :root {
      --bg-color: #0b0e14;
      --card-bg: #151a23;
      --accent: #00d2ff;
      --accent-hover: #00a8cc;
      --kaspi-red: #f14635;
      --text: #ffffff;
      --text-sub: #a0a8b8;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background-color: var(--bg-color);
      color: var(--text);
      display: flex;
      justify-content: center;
      padding: 20px;
      min-height: 100vh;
    }

    .container {
      width: 100%;
      max-width: 480px;
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    header {
      text-align: center;
      background: var(--card-bg);
      padding: 20px;
      border-radius: 16px;
      border: 1px solid rgba(0, 210, 255, 0.2);
      box-shadow: 0 0 20px rgba(0, 210, 255, 0.1);
    }

    header h1 {
      font-size: 24px;
      color: var(--accent);
      margin-bottom: 8px;
    }

    header p {
      font-size: 14px;
      color: var(--text-sub);
      margin-bottom: 12px;
    }

    .badges {
      display: flex;
      justify-content: center;
      gap: 10px;
      font-size: 12px;
      flex-wrap: wrap;
    }

    .badge {
      background: rgba(255, 255, 255, 0.05);
      padding: 6px 12px;
      border-radius: 20px;
      border: 1px solid rgba(255, 255, 255, 0.1);
    }

    .grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 15px;
    }

    .card {
      background: var(--card-bg);
      border-radius: 14px;
      padding: 16px;
      text-align: center;
      border: 1px solid rgba(255, 255, 255, 0.05);
      transition: transform 0.2s;
    }

    .card:hover {
      transform: translateY(-3px);
    }

    .card-amount {
      font-size: 20px;
      font-weight: bold;
      color: #fff;
      margin-bottom: 8px;
    }

    .card-price {
      font-size: 18px;
      color: #ff3b30;
      font-weight: bold;
      margin-bottom: 12px;
    }

    .btn {
      width: 100%;
      padding: 10px;
      background: var(--accent);
      color: #000;
      font-weight: bold;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 14px;
      transition: background 0.2s;
    }

    .btn:hover {
      background: var(--accent-hover);
    }

    .modal-overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.85);
      display: none;
      justify-content: center;
      align-items: center;
      padding: 20px;
      z-index: 1000;
    }

    .modal {
      background: var(--card-bg);
      border-radius: 16px;
      width: 100%;
      max-width: 400px;
      padding: 24px;
      border: 1px solid rgba(255, 255, 255, 0.1);
    }

    .modal-step {
      display: none;
    }

    .modal-step.active {
      display: block;
    }

    .form-group {
      margin-bottom: 16px;
      text-align: left;
    }

    .form-group label {
      display: block;
      font-size: 14px;
      color: var(--text-sub);
      margin-bottom: 6px;
    }

    .form-group select, .form-group input {
      width: 100%;
      padding: 12px;
      background: #0b0e14;
      border: 1px solid rgba(255, 255, 255, 0.1);
      border-radius: 8px;
      color: #fff;
      font-size: 15px;
      outline: none;
    }

    .form-group select:focus, .form-group input:focus {
      border-color: var(--accent);
    }

    .kaspi-header {
      color: var(--kaspi-red);
      font-size: 28px;
      font-weight: 800;
      text-align: center;
      margin-bottom: 15px;
      letter-spacing: 0.5px;
    }

    .info-box {
      background: #0b0e14;
      padding: 15px;
      border-radius: 10px;
      margin-bottom: 15px;
      font-size: 14px;
      line-height: 1.6;
    }

    .info-box div {
      display: flex;
      justify-content: space-between;
      margin-bottom: 6px;
    }

    .phone-highlight {
      background: rgba(241, 70, 53, 0.15);
      border: 1px dashed var(--kaspi-red);
      padding: 12px;
      border-radius: 10px;
      text-align: center;
      margin-bottom: 15px;
    }

    .phone-highlight span {
      display: block;
      font-size: 12px;
      color: var(--text-sub);
    }

    .phone-highlight strong {
      font-size: 20px;
      color: #fff;
      letter-spacing: 1px;
    }

    .kaspi-btn {
      background: var(--kaspi-red);
      color: #fff;
      text-decoration: none;
      display: block;
      text-align: center;
      padding: 14px;
      border-radius: 10px;
      font-weight: bold;
      font-size: 15px;
      border: none;
      width: 100%;
      cursor: pointer;
    }

    .close-btn {
      background: transparent;
      color: var(--text-sub);
      border: none;
      width: 100%;
      padding: 8px;
      margin-top: 8px;
      cursor: pointer;
    }

    footer {
      text-align: center;
      font-size: 12px;
      color: var(--text-sub);
      padding: 10px;
    }
  </style>
</head>
<body>

  <div class="container">
    <header>
      <h1>💎 NEXO SHOP 💎</h1>
      <p>Виртуалды дүкен • Black Russia магазины</p>
      <div class="badges">
        <span class="badge">⚡ Жылдам жеткізу</span>
        <span class="badge">🔒 Қауіпсіз</span>
        <span class="badge">💰 Қолжетімді бағалар</span>
      </div>
    </header>

    <div class="grid">
      <div class="card">
        <div class="card-amount">💰 5KK</div>
        <div class="card-price">🔥 1 200 ₸</div>
        <button class="btn" onclick="openOrder('5KK', '1 200 ₸')">🛒 Сатып алу</button>
      </div>
      <div class="card">
        <div class="card-amount">💎 8KK</div>
        <div class="card-price">🔥 1 500 ₸</div>
        <button class="btn" onclick="openOrder('8KK', '1 500 ₸')">🛒 Сатып алу</button>
      </div>
      <div class="card">
        <div class="card-amount">🚀 10KK</div>
        <div class="card-price">🔥 1 800 ₸</div>
        <button class="btn" onclick="openOrder('10KK', '1 800 ₸')">🛒 Сатып алу</button>
      </div>
      <div class="card">
        <div class="card-amount">👑 15KK</div>
        <div class="card-price">🔥 2 400 ₸</div>
        <button class="btn" onclick="openOrder('15KK', '2 400 ₸')">🛒 Сатып алу</button>
      </div>
    </div>

    <footer>
      ⭐ NEXO SHOP — сапа мен жылдамдық бір жерде!
    </footer>
  </div>

  <div class="modal-overlay" id="modalOverlay">
    <div class="modal">
      
      <!-- 1-қадам: Сервер мен Ник таңдау -->
      <div class="modal-step active" id="step1">
        <h3 style="margin-bottom: 16px; text-align: center;">Деректерді енгізіңіз</h3>
        <div class="form-group">
          <label for="serverSelect">Серверді таңдаңыз (1-91):</label>
          <select id="serverSelect"></select>
        </div>
        <div class="form-group">
          <label for="nicknameInput">Ойын ішіндегі Ник (Nickname):</label>
          <input type="text" id="nicknameInput" placeholder="Мысалы: Nexo_Shop">
        </div>
        <button class="btn" onclick="goToStep2()">Жалғастыру</button>
        <button class="close-btn" onclick="closeModal()">Бас тарту</button>
      </div>

      <!-- 2-қадам: Төлем ақпараты және Каспи қосымшасына өту -->
      <div class="modal-step" id="step2">
        <div class="kaspi-header">kaspi.kz</div>
        
        <div class="info-box">
          <div><span>Тауар:</span> <strong id="summaryItem">-</strong></div>
          <div><span>Бағасы:</span> <strong id="summaryPrice">-</strong></div>
          <div><span>Сервер:</span> <strong id="summaryServer">-</strong></div>
          <div><span>Ник:</span> <strong id="summaryNick">-</strong></div>
        </div>

        <div class="phone-highlight">
          <span>Аударылатын нөмір:</span>
          <strong>8 707 515 34 05</strong>
        </div>

        <button class="kaspi-btn" onclick="payViaKaspi()">📲 Нөмірді көшіріп, Kaspi қосымшасын ашу</button>
        <button class="close-btn" onclick="closeModal()">Жабу</button>
      </div>

    </div>
  </div>

  <script>
    // Black Russia 1-ден 91-ге дейінгі ресми сервер тізімі
    const serverNames = [
      "RED", "GREEN", "BLUE", "YELLOW", "ORANGE", "PURPLE", "LIME", "PINK", "CHERRY", "BLACK",
      "INDIGO", "WHITE", "MAGENTA", "CRIMSON", "GOLD", "AZURE", "PLATINUM", "AQUA", "GRAY", "ICE",
      "CHILLI", "CHOCO", "MOSCOW", "SPB", "UFA", "SOCHI", "KAZAN", "SAMARA", "ROSTOV", "ANAPA",
      "EKB", "KRASNODAR", "ARZAMAS", "NOVOSIB", "GROZNY", "SARATOV", "OMSK", "IRKUTSK", "VOLGOGRAD", "VORONEZH",
      "BELGOROD", "MAKHACHKALA", "VLADIKAVKAZ", "VLADIVOSTOK", "KALININGRAD", "CHELYABINSK", "KRASNOYARSK", "CHEBOKSARY", "KHABAROVSK", "PERM",
      "TULA", "RYAZAN", "MURMANSK", "PENZA", "KURSK", "ARKHANGELSK", "ORENBURG", "KIROV", "KEMEROVO", "TYUMEN",
      "TOLYATTI", "IVANOVO", "STAVROPOL", "SMOLENSK", "PSKOV", "BRYANSK", "OREL", "YAROSLAVL", "BARNAUL", "LIPETSK",
      "ULYANOVSK", "YAKUTSK", "TAMBOV", "BRATSK", "ASTRAKHAN", "CHITA", "KOSTROMA", "VLADIMIR", "KALUGA", "NOVGOROD",
      "TAGANROG", "VOLOGDA", "TVER", "TOMSK", "IZHEVSK", "SURGUT", "PODOLSK", "MAGADAN", "CHEREPOVETS", "NORILSK", "ASTANA"
    ];

    let selectedItem = "";
    let selectedPrice = "";

    // 91 серверді ретімен тізімге орналастыру
    const serverSelect = document.getElementById('serverSelect');
    serverNames.forEach((name, index) => {
      const opt = document.createElement('option');
      opt.value = `${index + 1} - ${name}`;
      opt.textContent = `${index + 1} - ${name}`;
      serverSelect.appendChild(opt);
    });

    function openOrder(item, price) {
      selectedItem = item;
      selectedPrice = price;
      document.getElementById('modalOverlay').style.display = 'flex';
      document.getElementById('step1').classList.add('active');
      document.getElementById('step2').classList.remove('active');
    }

    function goToStep2() {
      const nick = document.getElementById('nicknameInput').value.trim();
      if (!nick) {
        alert('Өтініш, ойындағы никіңізді енгізіңіз!');
        return;
      }

      document.getElementById('summaryItem').textContent = selectedItem;
      document.getElementById('summaryPrice').textContent = selectedPrice;
      document.getElementById('summaryServer').textContent = document.getElementById('serverSelect').value;
      document.getElementById('summaryNick').textContent = nick;

      document.getElementById('step1').classList.remove('active');
      document.getElementById('step2').classList.active = false;
      document.getElementById('step2').classList.add('active');
    }

    function payViaKaspi() {
      const phoneNumber = "87075153405";
      
      // Телефон нөмірін клипбордқа көшіру
      if (navigator.clipboard && navigator.clipboard.writeText) {
        navigator.clipboard.writeText(phoneNumber);
      }

      alert("87075153405 нөмірі көшірілді! Kaspi қосымшасында 'Переводы' бөліміне қоя салыңыз.");

      // Мобильді Kaspi қосымшасын тікелей ашу (Deep Link)
      window.location.href = "kaspi://";

      // Егер Kaspi қосымшасы ашылмай калса (мысалы ПК-де), 1 секундтан соң веб-сайтына бағыттайды
      setTimeout(function() {
        window.location.href = "https://kaspi.kz";
      }, 1000);
    }

    function closeModal() {
      document.getElementById('modalOverlay').style.display = 'none';
      document.getElementById('nicknameInput').value = '';
    }
  </script>
</body>
</html>
