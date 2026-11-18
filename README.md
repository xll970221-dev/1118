# 1118
塔羅[1118221.html](https://github.com/user-attachments/files/35017627/1118221.html)


<!DOCTYPE html>
<html lang="zh-TW">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>✦ 達心塔羅 STARWOVEN TAROT</title>
  <style>
    * { box-sizing: border-box; }
    
    body { 
      margin: 0; 
      color: #e3d5f0; 
      font-family: Arial, "Noto Sans TC", sans-serif; 
      background-image: var(--full-bg, 
        radial-gradient(white 1px, transparent 1px), 
        radial-gradient(rgba(255,255,255,0.6) 1.5px, transparent 1.5px),
        linear-gradient(135deg, #150b24, #2b1d3a, #1a0f2b, #332344)
      );
      background-size: var(--full-bg-size, 120px 120px, 200px 200px, 400% 400%);
      background-position: 0 0, 40px 60px, 0% 50%;
      animation: gradientBG 15s ease infinite;
      background-attachment: fixed;
    }

    @keyframes gradientBG {
      0% { background-position: 0 0, 40px 60px, 0% 50%; }
      50% { background-position: 50px 50px, 90px 110px, 100% 50%; }
      100% { background-position: 0 0, 40px 60px, 0% 50%; }
    }

    header { background: rgba(33, 24, 47, 0.85); backdrop-filter: blur(8px); color: white; padding: 20px; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; }
    header h1 { font-size: 23px; margin: 0; display: flex; align-items: center; gap: 8px; }
    nav a { color: #e3d5f0; text-decoration: none; margin: 8px; }
    nav a:hover { color: #fff; }

    section { padding: 55px 20px; max-width: 1000px; margin: auto; text-align: center; }

    .hero { background: rgba(43, 32, 56, 0.75); backdrop-filter: blur(10px); border: 1px solid rgba(188, 165, 212, 0.2); border-radius: 25px; padding: 60px 20px; margin-top: 25px; color: #fbf9fc; }
    .hero h2 { font-size: 36px; color: #fff; }

    .event-banner { background: rgba(89, 65, 110, 0.9); color: white; padding: 20px; border-radius: 15px; margin: 0 auto 25px; max-width: 700px; box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3); text-align: left; }
    .event-banner img { max-width: 100%; max-height: 260px; border-radius: 10px; margin-top: 12px; object-fit: cover; display: block; }

    .calendar-grid { display: grid; grid-template-columns: repeat(7, 1fr); gap: 8px; max-width: 750px; margin: 20px auto; background: rgba(33, 24, 47, 0.85); backdrop-filter: blur(10px); border: 1px solid rgba(188, 165, 212, 0.2); padding: 18px; border-radius: 15px; box-shadow: 0 3px 15px rgba(0,0,0,0.3); }
    .cal-header { font-weight: bold; color: #d0bde6; padding: 8px 0; border-bottom: 1px solid rgba(255,255,255,0.1); }
    .cal-cell { background: rgba(43, 32, 56, 0.6); border: 1px solid rgba(188, 165, 212, 0.2); border-radius: 8px; padding: 8px 4px; min-height: 80px; font-size: 13px; text-align: center; color: #fff; }
    .cal-cell.open { background: rgba(89, 65, 110, 0.7); border-color: #bca5d4; }
    .cal-day-num { font-weight: bold; font-size: 15px; margin-bottom: 5px; }
    .cal-time-tag { background: #59416e; color: white; font-size: 11px; padding: 3px 5px; border-radius: 5px; display: inline-block; word-break: break-all; }

    .card { background: rgba(43, 32, 56, 0.85); backdrop-filter: blur(10px); border: 1px solid rgba(188, 165, 212, 0.2); color: #fff; border-radius: 15px; padding: 22px; margin: 15px auto; max-width: 400px; box-shadow: 0 3px 15px rgba(0,0,0,0.3); text-align: left; }
    .service-list { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 15px; }

    button { background: #59416e; color: white; border: none; border-radius: 30px; padding: 14px 25px; margin: 8px; cursor: pointer; font-size: 15px; }
    button:hover { background: #80639a; }
    .btn-danger { background: #c0392b; }
    .btn-danger:hover { background: #e74c3c; }
    .btn-sm { padding: 5px 10px; font-size: 12px; border-radius: 6px; margin: 2px; }

    input, select, textarea { width: 100%; max-width: 450px; display: block; padding: 13px; margin: 10px auto 18px; background: rgba(33, 24, 47, 0.6); color: white; border: 1px solid #80639a; border-radius: 9px; font-size: 15px; }
    input::placeholder, textarea::placeholder { color: #bca5d4; }
    label { display: block; font-weight: bold; text-align: left; max-width: 450px; margin: auto; color: #e3d5f0; }
    textarea { min-height: 100px; }

    .deck-area { display: flex; flex-wrap: wrap; justify-content: center; gap: 8px; max-width: 750px; margin: 15px auto; }
    .card-back { width: 56px; height: 90px; background: linear-gradient(135deg, #21182f, #493361); color: #e3d5f0; border: 2px solid #bca5d4; border-radius: 8px; display: flex; align-items: center; justify-content: center; cursor: pointer; transition: transform 0.2s; font-size: 16px; }
    .card-back:hover { transform: translateY(-8px); }
    .card-back.picked { background: #80639a; border-color: #f1c40f; color: #f1c40f; transform: translateY(-10px); }

    .tarot-card { background: rgba(33, 24, 47, 0.9); border: 1px solid #bca5d4; color: white; border-radius: 15px; padding: 25px; margin: 15px auto; max-width: 300px; }
    .result { background: rgba(43, 32, 56, 0.9); backdrop-filter: blur(10px); border: 1px solid rgba(188, 165, 212, 0.2); color: #fff; border-radius: 15px; padding: 20px; margin: 15px auto; max-width: 500px; line-height: 1.9; text-align: left; box-shadow: 0 3px 15px rgba(0,0,0,0.3); }

    #adminPanelContainer { background: rgba(33, 24, 47, 0.95); color: #fbf9fc; border-top: 6px solid #80639a; padding: 40px 20px; margin-top: 50px; text-align: left; display: none; }
    .admin-box { background: rgba(43, 32, 56, 0.85); border: 1px solid rgba(188, 165, 212, 0.2); border-radius: 15px; padding: 25px; margin: 20px auto; max-width: 1000px; box-shadow: 0 3px 15px rgba(0,0,0,0.3); }
    .admin-cal-grid { display: grid; grid-template-columns: repeat(7, 1fr); gap: 8px; margin-top: 15px; }
    .admin-cal-head { text-align: center; font-weight: bold; color: #d0bde6; padding: 6px; }
    .admin-cal-cell { background: rgba(33, 24, 47, 0.6); border: 1px solid #80639a; border-radius: 8px; padding: 8px; min-height: 90px; cursor: pointer; transition: 0.2s; font-size: 13px; text-align: center; color: white; }
    .admin-cal-cell:hover { border-color: #f1c40f; background: rgba(89, 65, 110, 0.7); }
    .admin-cal-cell.has-time { background: rgba(89, 65, 110, 0.9); border: 2px solid #bca5d4; }
    
    table { width: 100%; border-collapse: collapse; margin-top: 10px; font-size: 14px; color: #fff; }
    th, td { padding: 12px; border-bottom: 1px solid rgba(255,255,255,0.1); text-align: left; }
    th { background: rgba(33, 24, 47, 0.8); color: #d0bde6; }

    footer { background: #150b24; color: #bca5d4; text-align: center; padding: 30px; }

    @media (max-width: 600px) {
      header { flex-direction: column; }
      .hero h2 { font-size: 28px; }
      .calendar-grid, .admin-cal-grid { gap: 4px; padding: 8px; }
    }
  </style>
</head>
<body>

<header>
  <!-- 🔮 左上角登入入口：點 2 下即可輸入密碼 aa141319 進入後台 -->
  <h1>
    <span id="secretAdminTrigger" style="cursor:pointer; user-select:none; font-size:20px;" title="雙擊此處登入管理後台">🔮</span> 
    達心塔羅
  </h1>
  <nav>
    <a href="#services">服務項目</a>
    <a href="#calendar">可約月曆</a>
    <a href="#draw">免費抽牌</a>
    <a href="#booking">預約</a>
  </nav>
</header>

<section class="hero">
  <div id="eventBanner" class="event-banner" hidden></div>

  <p>STARWOVEN TAROT</p>
  <h2>達心直達你心<br>陪你從混亂中釐清</h2>
  <p>在適合自己的時刻，慢慢梳理問題、看見方向。</p>
  <a href="#booking"><button>立即預約</button></a>
  <a href="#draw"><button>免費抽牌</button></a>
</section>

<!-- 老師可約時段月曆（客人視角） -->
<section id="calendar">
  <h2>📅 老師可預約時間表</h2>
  <p>以下為本月開放預約的日期與時段，請先確認時間再填寫下方預約單。</p>
  <div id="publicCalendar" class="calendar-grid"></div>
</section>

<section id="services">
  <h2>服務項目</h2>
  <p>選擇適合你的方式，為自己留一段安靜的時間。</p>
  <div id="serviceList" class="service-list"></div>
</section>

<section id="draw">
  <h2>✦ 免費線上抽牌 ✦</h2>
  <p>讓塔羅牌為你帶來新的方向。</p>
  <h3 id="remaining">今日剩餘免費次數：3 次</h3>

  <label for="question">請輸入你想詢問的問題</label>
  <textarea id="question" placeholder="例如：我最近的感情發展如何？"></textarea>

  <div>
    <button onclick="prepareDeck(1)">抽一張牌</button>
    <button onclick="prepareDeck(3)">抽三張牌</button>
  </div>

  <p id="pickHint" style="font-weight:bold; color:#d0bde6;"></p>
  <div id="cardDeckArea" class="deck-area"></div>

  <div id="drawResult"></div>

  <div id="bookingLink" hidden>
    <h3>想深入了解你的問題嗎？</h3>
    <p>歡迎預約專屬塔羅占卜。</p>
    <a href="#booking"><button>預約深入解讀</button></a>
  </div>
</section>

<section id="booking">
  <h2>✦ 線上預約 ✦</h2>
  <p>填寫資料，為你安排專屬占卜。</p>

  <form id="bookingForm">
    <label for="customerName">姓名</label>
    <input id="customerName" type="text" placeholder="請輸入姓名" required>

    <label for="customerPhone">手機電話</label>
    <input id="customerPhone" type="tel" placeholder="請輸入手機號碼" required>

    <label for="customerEmail">Email</label>
    <input id="customerEmail" type="email" placeholder="請輸入電子信箱" required>

    <label for="bookingDate">預約日期</label>
    <input id="bookingDate" type="date" required onchange="updateBookingTimes()">

    <label for="bookingTime">預約時段（依老師排班顯示）</label>
    <select id="bookingTime" required>
      <option value="">請先選擇預約日期</option>
    </select>

    <label for="bookingService">預約服務</label>
    <select id="bookingService" required>
      <option value="">請選擇服務</option>
    </select>

    <label for="bookingQuestion">想詢問的問題</label>
    <textarea id="bookingQuestion" placeholder="請描述你想詢問的問題"></textarea>

    <button type="submit">送出預約</button>
  </form>

  <p id="bookingMessage" style="font-weight:bold; color:#d0bde6;"></p>
</section>

<!-- 🔒 內部管理後台面板 -->
<div id="adminPanelContainer">
  <div style="max-width:1000px; margin:0 auto; text-align:center; display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:10px;">
    <h2 style="color:#fff; margin:0;">🔒 塔羅師內部管理系統</h2>
    <div>
      <button onclick="switchToCustomerView()" class="btn-sm" style="background:#59416e; color:white; padding:10px 18px; margin:0 5px;">👁️ 切換客人視角</button>
      <button class="btn-danger" onclick="adminLogout()" style="margin:0;">登出管理後台</button>
    </div>
  </div>

  <!-- 0. 網站背景與星光點綴設定 -->
  <div class="admin-box">
    <h3>🎨 網站背景與星光點綴設定</h3>
    <label>1. 選擇星光點綴樣式</label>
    <select id="bgSparkle" style="margin-bottom:15px;">
      <option value="dots">✨ 細緻白點（預設）</option>
      <option value="stars">✦ 閃爍四角星星</option>
      <option value="none">🌑 無點綴（純淨背景）</option>
    </select>
    <label>2. 選擇底色類型</label>
    <select id="bgType" onchange="toggleBgInputs()" style="margin-bottom:15px;">
      <option value="gradient">動態漸層色調</option>
      <option value="solid">單一純色背景</option>
    </select>
    <div id="solidColorBox" style="display:none; margin-bottom:15px;">
      <label>選擇單一背景顏色</label>
      <input type="color" id="singleColor" value="#1f1430" style="height:40px; padding:2px; cursor:pointer;">
    </div>
    <div id="gradientColorBox" style="display:flex; flex-wrap:wrap; gap:15px; align-items:center; margin-bottom:15px;">
      <div><label>漸層色 1</label><input type="color" id="color1" value="#150b24" style="height:40px; padding:2px; cursor:pointer;"></div>
      <div><label>漸層色 2</label><input type="color" id="color2" value="#2b1d3a" style="height:40px; padding:2px; cursor:pointer;"></div>
      <div><label>漸層色 3</label><input type="color" id="color3" value="#1a0f2b" style="height:40px; padding:2px; cursor:pointer;"></div>
      <div><label>漸層色 4</label><input type="color" id="color4" value="#332344" style="height:40px; padding:2px; cursor:pointer;"></div>
    </div>
    <button onclick="saveThemeColors()">儲存並套用背景設定</button>
    <button onclick="resetThemeColors()" class="btn-danger">恢復預設暗紫白點</button>
  </div>

  <!-- 0.5 服務項目、原價與優惠管理 -->
  <div class="admin-box">
    <h3>💰 服務項目、原價與優惠價格管理</h3>
    <p style="font-size:13px; color:#bca5d4;">在此可直接自訂各服務的「原價」與「優惠價說明」（若無優惠可將優惠欄位清空）。</p>
    <div style="overflow-x:auto;">
      <table>
        <thead>
          <tr>
            <th>服務名稱</th>
            <th>時長 / 類型</th>
            <th>原價 (NT$)</th>
            <th>優惠價 / 折扣說明</th>
            <th>操作</th>
          </tr>
        </thead>
        <tbody id="adminServiceTable"></tbody>
      </table>
    </div>
  </div>

  <!-- 1. 活動公告管理 -->
  <div class="admin-box">
    <h3>🎉 活動優惠管理（超過設定時間自動下架）</h3>
    <form id="adminEventForm">
      <label>活動名稱</label>
      <input type="text" id="evTitle" placeholder="例如：中秋節預約打折優惠" required>
      <label>活動截止日期</label>
      <input type="date" id="evEndDate" required>
      <label>活動內容</label>
      <textarea id="evContent" placeholder="活動說明..."></textarea>
      <label>活動照片（選填）</label>
      <input type="file" id="evPhotoFile" accept="image/*">
      <button type="submit">上架活動</button>
    </form>
    <div id="adminEventList" style="margin-top:15px;"></div>
  </div>

  <!-- 2. 月曆排班管理 -->
  <div class="admin-box">
    <div style="display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:10px;">
      <h3 style="margin:0;">📅 老師月曆排班表（點擊日期設定時段）</h3>
      <div>
        <button onclick="batchWeekdays()" class="btn-sm" style="background:#59416e; color:white; padding:8px 12px;">⚡ 一鍵設定週一至週五</button>
        <button onclick="clearCalendar()" class="btn-danger btn-sm" style="padding:8px 12px;">🗑️ 一鍵清除全部</button>
      </div>
    </div>
    <p style="font-size:13px; color:#bca5d4; text-align:left;">💡 點擊下方月曆某一天即可設定（例如輸入 <code>7~11</code> 或 <code>14:00</code>），清空則代表休息。</p>
    <div id="adminCalendar" class="admin-cal-grid"></div>
  </div>

  <!-- 3. 客戶預約資料表 -->
  <div class="admin-box">
    <h3>📋 客戶預約資料表</h3>
    <div style="overflow-x:auto;">
      <table>
        <thead>
          <tr>
            <th>預約日期 / 時段</th>
            <th>客人姓名</th>
            <th>手機電話</th>
            <th>Email</th>
            <th>預約服務</th>
            <th>詢問問題</th>
            <th>狀態</th>
            <th>操作</th>
          </tr>
        </thead>
        <tbody id="adminBookingTable"></tbody>
      </table>
    </div>
  </div>
</div>

<footer>
  <h3 style="margin:0 0 10px 0;">✦ 達心塔羅 STARWOVEN TAROT</h3>
  <p style="margin:0;">願每一道星光，都能陪你找到方向。</p>
</footer>

<script>
// ===== 0. 背景與星光點綴初始化邏輯 =====
const STAR_SVG_1 = `url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Cpath d='M25 15 L27 23 L35 25 L27 27 L25 35 L23 27 L15 25 L23 23 Z' fill='rgba(255,255,255,0.75)'/%3E%3Cpath d='M90 75 L91.5 80.5 L97 82 L91.5 83.5 L90 89 L88.5 83.5 L83 82 L88.5 80.5 Z' fill='rgba(255,255,255,0.5)'/%3E%3C/svg%3E")`;
const STAR_SVG_2 = `url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='200' height='200' viewBox='0 0 200 200'%3E%3Cpath d='M140 30 L142 38 L150 40 L142 42 L140 50 L138 42 L130 40 L138 38 Z' fill='rgba(255,255,255,0.65)'/%3E%3Cpath d='M50 150 L51.5 156.5 L58 158 L51.5 159.5 L50 166 L48.5 159.5 L42 158 L48.5 156.5 Z' fill='rgba(255,255,255,0.45)'/%3E%3C/svg%3E")`;

function applyThemeColors() {
  const saved = JSON.parse(localStorage.getItem("starwovenThemeSettings") || "null");
  let baseGradient = 'linear-gradient(135deg, #150b24, #2b1d3a, #1a0f2b, #332344)';
  let baseSize = '400% 400%';
  let sparkle = 'dots';

  if (saved) {
    sparkle = saved.sparkle || 'dots';
    if (saved.type === "solid") {
      baseGradient = `linear-gradient(${saved.color}, ${saved.color})`;
      baseSize = '100% 100%';
    } else {
      baseGradient = `linear-gradient(135deg, ${saved.c1}, ${saved.c2}, ${saved.c3}, ${saved.c4})`;
      baseSize = '400% 400%';
    }
  }

  let fullBg = '', fullSize = '';
  if (sparkle === 'stars') {
    fullBg = `${STAR_SVG_1}, ${STAR_SVG_2}, ${baseGradient}`;
    fullSize = `120px 120px, 200px 200px, ${baseSize}`;
  } else if (sparkle === 'none') {
    fullBg = `none, none, ${baseGradient}`;
    fullSize = `120px 120px, 200px 200px, ${baseSize}`;
  } else {
    fullBg = `radial-gradient(white 1px, transparent 1px), radial-gradient(rgba(255,255,255,0.6) 1.5px, transparent 1.5px), ${baseGradient}`;
    fullSize = `120px 120px, 200px 200px, ${baseSize}`;
  }

  document.documentElement.style.setProperty('--full-bg', fullBg);
  document.documentElement.style.setProperty('--full-bg-size', fullSize);
}
applyThemeColors();

function toggleBgInputs() {
  const type = document.getElementById("bgType").value;
  if (type === "solid") {
    document.getElementById("solidColorBox").style.display = "block";
    document.getElementById("gradientColorBox").style.display = "none";
  } else {
    document.getElementById("solidColorBox").style.display = "none";
    document.getElementById("gradientColorBox").style.display = "flex";
  }
}

function saveThemeColors() {
  const sparkle = document.getElementById("bgSparkle").value;
  const type = document.getElementById("bgType").value;
  let settings = { sparkle, type };

  if (type === "solid") {
    settings.color = document.getElementById("singleColor").value;
  } else {
    settings.c1 = document.getElementById("color1").value;
    settings.c2 = document.getElementById("color2").value;
    settings.c3 = document.getElementById("color3").value;
    settings.c4 = document.getElementById("color4").value;
  }

  localStorage.setItem("starwovenThemeSettings", JSON.stringify(settings));
  applyThemeColors();
  alert("✅ 背景與星光點綴已成功更新並套用！");
}

function resetThemeColors() {
  localStorage.removeItem("starwovenThemeSettings");
  applyThemeColors();
  document.getElementById("bgSparkle").value = "dots";
  document.getElementById("bgType").value = "gradient";
  document.getElementById("singleColor").value = "#1f1430";
  document.getElementById("color1").value = "#150b24";
  document.getElementById("color2").value = "#2b1d3a";
  document.getElementById("color3").value = "#1a0f2b";
  document.getElementById("color4").value = "#332344";
  toggleBgInputs();
  alert("🔄 已恢復預設暗紫白點星空背景！");
}

// ===== 1. 服務項目與價格設定 =====
const defaultServices = [
  {name:"塔羅語音", time:"30分鐘", price:600, promo:""},
  {name:"塔羅面對面", time:"30分鐘", price:600, promo:""},
  {name:"塔羅文字一題", time:"依問題安排", price:300, promo:""},
  {name:"靈氣語音", time:"30分鐘", price:800, promo:""},
  {name:"靈氣面對面", time:"60分鐘", price:1500, promo:""},
  {name:"八字語音", time:"30分鐘", price:800, promo:""},
  {name:"八字面對面", time:"60分鐘", price:1500, promo:""}
];

function getServices() {
  const saved = localStorage.getItem("starwovenServices");
  return saved ? JSON.parse(saved) : defaultServices;
}

function renderServices() {
  const services = getServices();
  const serviceList = document.getElementById("serviceList");
  const serviceSelect = document.getElementById("bookingService");

  serviceList.innerHTML = "";
  serviceSelect.innerHTML = `<option value="">請選擇服務</option>`;

  services.forEach(service => {
    serviceList.innerHTML += `
      <div class="card">
        <h3>${service.name}</h3>
        <p>${service.time}</p>
        ${service.promo ? `
          <p style="text-decoration:line-through; color:#aaa; margin:0; font-size:13px;">NT$${service.price}</p>
          <h3 style="color:#ffcc00; margin:5px 0;">🔥 ${service.promo}</h3>
        ` : `
          <h3>NT$${service.price}</h3>
        `}
      </div>
    `;

    const displayPriceText = service.promo ? `${service.promo}` : `NT$${service.price}`;
    serviceSelect.innerHTML += `
      <option value="${service.name} - ${displayPriceText}">
        ${service.name} (${displayPriceText})
      </option>
    `;
  });
}
renderServices();

// ===== 2. 78張完整塔羅牌庫 =====
const tarotDeck = [
  {name:"愚者", suit:"大阿爾克那", meaning:"開始、冒險、純真"},
  {name:"魔術師", suit:"大阿爾克那", meaning:"創造力、行動、資源"},
  {name:"女祭師", suit:"大阿爾克那", meaning:"直覺、潛意識、靜止、研究者"},
  {name:"皇后", suit:"大阿爾克那", meaning:"豐盛、母愛、感官"},
  {name:"皇帝", suit:"大阿爾克那", meaning:"權威、結構、自律"},
  {name:"教皇", suit:"大阿爾克那", meaning:"傳統、教導、儀式"},
  {name:"戀人", suit:"大阿爾克那", meaning:"選擇、結合、價值觀"},
  {name:"戰車", suit:"大阿爾克那", meaning:"意志、勝利、自控、方向性"},
  {name:"力量", suit:"大阿爾克那", meaning:"勇氣、耐性、以柔克剛"},
  {name:"隱士", suit:"大阿爾克那", meaning:"內省、導師、孤獨"},
  {name:"命運之輪", suit:"大阿爾克那", meaning:"轉機、業力、改變"},
  {name:"正義", suit:"大阿爾克那", meaning:"公平、真相、法律"},
  {name:"吊人", suit:"大阿爾克那", meaning:"犧牲、換位思考、等待"},
  {name:"死神", suit:"大阿爾克那", meaning:"結束、轉化、新生"},
  {name:"節制", suit:"大阿爾克那", meaning:"平衡、調和、療癒"},
  {name:"惡魔", suit:"大阿爾克那", meaning:"慾望、束縛、成癮"},
  {name:"高塔", suit:"大阿爾克那", meaning:"崩塌、震撼、覺醒"},
  {name:"星星", suit:"大阿爾克那", meaning:"希望、療癒、靈感"},
  {name:"月亮", suit:"大阿爾克那", meaning:"不安、幻影、直覺、危險"},
  {name:"太陽", suit:"大阿爾克那", meaning:"成功、快樂、光明"},
  {name:"審判", suit:"大阿爾克那", meaning:"覺醒、召喚、重生"},
  {name:"世界", suit:"大阿爾克那", meaning:"圓滿、成就、統合"},

  {name:"權杖1", suit:"權杖", meaning:"新的開始、靈感"},
  {name:"權杖2", suit:"權杖", meaning:"規劃、遠見"},
  {name:"權杖3", suit:"權杖", meaning:"行動、貿易"},
  {name:"權杖4", suit:"權杖", meaning:"穩定、慶祝"},
  {name:"權杖5", suit:"權杖", meaning:"競爭、混亂"},
  {name:"權杖6", suit:"權杖", meaning:"勝利、榮耀"},
  {name:"權杖7", suit:"權杖", meaning:"防禦、挑戰"},
  {name:"權杖8", suit:"權杖", meaning:"快速、訊息"},
  {name:"權杖9", suit:"權杖", meaning:"防備、韌性"},
  {name:"權杖10", suit:"權杖", meaning:"壓力、責任"},
  {name:"權杖侍者", suit:"權杖", meaning:"好奇、嘗試、信差"},
  {name:"權杖騎士", suit:"權杖", meaning:"衝勁、冒險、執行"},
  {name:"權杖皇后", suit:"權杖", meaning:"魅力、自信、熱誠"},
  {name:"權杖國王", suit:"權杖", meaning:"領導、遠見、掌控"},

  {name:"聖杯1", suit:"聖杯", meaning:"情感滿溢、新戀情"},
  {name:"聖杯2", suit:"聖杯", meaning:"結合、平等、承諾、情感交流"},
  {name:"聖杯3", suit:"聖杯", meaning:"慶祝、友誼、豐收"},
  {name:"聖杯4", suit:"聖杯", meaning:"厭倦、沉思、拒絕"},
  {name:"聖杯5", suit:"聖杯", meaning:"悲傷、遺憾、失望"},
  {name:"聖杯6", suit:"聖杯", meaning:"童年、回憶、懷舊、餽贈"},
  {name:"聖杯7", suit:"聖杯", meaning:"幻想、選擇、混亂"},
  {name:"聖杯8", suit:"聖杯", meaning:"追尋、告別、離去"},
  {name:"聖杯9", suit:"聖杯", meaning:"滿足、炫耀、願望達成"},
  {name:"聖杯10", suit:"聖杯", meaning:"和諧、家庭、圓滿"},
  {name:"聖杯侍者", suit:"聖杯", meaning:"感性、夢想、傳情"},
  {name:"聖杯騎士", suit:"聖杯", meaning:"浪漫、求婚、理想主義"},
  {name:"聖杯皇后", suit:"聖杯", meaning:"直覺、慈悲、溫暖"},
  {name:"聖杯國王", suit:"聖杯", meaning:"包容、智慧、穩重"},

  {name:"寶劍1", suit:"寶劍", meaning:"突破、理智、正義"},
  {name:"寶劍2", suit:"寶劍", meaning:"猶豫、平衡、封閉"},
  {name:"寶劍3", suit:"寶劍", meaning:"心碎、悲傷、分離"},
  {name:"寶劍4", suit:"寶劍", meaning:"休息、沉思、康復"},
  {name:"寶劍5", suit:"寶劍", meaning:"自私、衝突、慘勝"},
  {name:"寶劍6", suit:"寶劍", meaning:"療癒、遷移、度過"},
  {name:"寶劍7", suit:"寶劍", meaning:"詭計、逃避、孤立"},
  {name:"寶劍8", suit:"寶劍", meaning:"束縛、無力、作繭自縛"},
  {name:"寶劍9", suit:"寶劍", meaning:"焦慮、惡夢、失眠"},
  {name:"寶劍10", suit:"寶劍", meaning:"谷底、結束、背叛"},
  {name:"寶劍侍者", suit:"寶劍", meaning:"警覺、求知、探測"},
  {name:"寶劍騎士", suit:"寶劍", meaning:"銳利、急躁、直言"},
  {name:"寶劍皇后", suit:"寶劍", meaning:"獨立、冷靜、批判"},
  {name:"寶劍國王", suit:"寶劍", meaning:"專業、判斷、公正"},

  {name:"錢幣1", suit:"錢幣", meaning:"新工作、工作機會"},
  {name:"錢幣2", suit:"錢幣", meaning:"平衡、彈性、金錢流動"},
  {name:"錢幣3", suit:"錢幣", meaning:"團隊合作、專業技術"},
  {name:"錢幣4", suit:"錢幣", meaning:"守財、保守、穩固、控制欲"},
  {name:"錢幣5", suit:"錢幣", meaning:"貧困、困境、被排斥、跟隨"},
  {name:"錢幣6", suit:"錢幣", meaning:"施予、慈善、資源分配"},
  {name:"錢幣7", suit:"錢幣", meaning:"評估、等待、中場休息、懷疑"},
  {name:"錢幣8", suit:"錢幣", meaning:"專注磨練、職人精神"},
  {name:"錢幣9", suit:"錢幣", meaning:"獨立、富足、自律"},
  {name:"錢幣10", suit:"錢幣", meaning:"傳承、家族、長久穩定"},
  {name:"錢幣侍者", suit:"錢幣", meaning:"務實學習、理財起點"},
  {name:"錢幣騎士", suit:"錢幣", meaning:"可靠、勤勉、耐力"},
  {name:"錢幣皇后", suit:"錢幣", meaning:"豐饒、照顧、安全感"},
  {name:"錢幣國王", suit:"錢幣", meaning:"企業家、慷慨、穩定"}
];

// ===== 3. 日期與活動工具 =====
function getToday() {
  const now = new Date();
  const taiwan = new Date(now.toLocaleString("en-US", {timeZone:"Asia/Taipei"}));
  return taiwan.getFullYear() + "-" +
    String(taiwan.getMonth()+1).padStart(2,"0") + "-" +
    String(taiwan.getDate()).padStart(2,"0");
}

function loadActiveEvents() {
  const events = JSON.parse(localStorage.getItem("starwovenEvents") || "[]");
  const today = getToday();
  const banner = document.getElementById("eventBanner");
  const activeEvents = events.filter(ev => ev.endDate >= today);
  localStorage.setItem("starwovenEvents", JSON.stringify(activeEvents));

  if (activeEvents.length > 0) {
    const ev = activeEvents[0];
    banner.hidden = false;
    banner.innerHTML = `
      <h3 style="margin-top:0;">🎉 ${ev.title}</h3>
      <p style="margin:5px 0;">活動期間：即日起至 ${ev.endDate}</p>
      <p style="margin:8px 0;">${ev.content}</p>
      ${ev.photo ? `<img src="${ev.photo}" alt="活動照片">` : ""}
    `;
  } else {
    banner.hidden = true;
  }
}
loadActiveEvents();

// ===== 4. 客人視角月曆與預約時段 =====
function renderPublicCalendar() {
  const schedule = JSON.parse(localStorage.getItem("starwovenSchedule") || "{}");
  const calEl = document.getElementById("publicCalendar");
  const todayObj = new Date(getToday());
  const year = todayObj.getFullYear();
  const month = todayObj.getMonth();

  const weekDays = ["日","一","二","三","四","五","六"];
  let html = weekDays.map(w => `<div class="cal-header">${w}</div>`).join("");

  const firstDay = new Date(year, month, 1).getDay();
  const daysInMonth = new Date(year, month + 1, 0).getDate();

  for (let i = 0; i < firstDay; i++) html += `<div></div>`;

  for (let day = 1; day <= daysInMonth; day++) {
    const dateStr = `${year}-${String(month+1).padStart(2,"0")}-${String(day).padStart(2,"0")}`;
    const timeText = schedule[dateStr];
    const isPast = dateStr < getToday();

    if (timeText && !isPast) {
      html += `
        <div class="cal-cell open">
          <div class="cal-day-num">${day}</div>
          <div class="cal-time-tag">${timeText}</div>
        </div>
      `;
    } else {
      html += `
        <div class="cal-cell">
          <div class="cal-day-num" style="color:#aaa;">${day}</div>
          <div style="font-size:11px; color:#bbb;">休</div>
        </div>
      `;
    }
  }
  calEl.innerHTML = html;
}
renderPublicCalendar();

function updateBookingTimes() {
  const dateVal = document.getElementById("bookingDate").value;
  const schedule = JSON.parse(localStorage.getItem("starwovenSchedule") || "{}");
  const timeSelect = document.getElementById("bookingTime");
  timeSelect.innerHTML = `<option value="">請選擇時段</option>`;

  if (schedule[dateVal]) {
    const slots = schedule[dateVal].split(/[,，]/).map(s => s.trim()).filter(Boolean);
    slots.forEach(slot => {
      timeSelect.innerHTML += `<option value="${slot}">${slot}</option>`;
    });
  } else {
    timeSelect.innerHTML += `<option value="" disabled>此日期老師未開放預約</option>`;
  }
}

// ===== 5. 抽牌邏輯（固定正位解讀） =====
function getUsage() {
  const saved = JSON.parse(localStorage.getItem("starwovenUsage") || "{}");
  if (saved.date !== getToday()) return {date:getToday(), count:0};
  return saved;
}

function updateRemaining() {
  const usage = getUsage();
  const remaining = Math.max(0, 3 - usage.count);
  document.getElementById("remaining").textContent = "今日剩餘免費次數：" + remaining + " 次";
  document.getElementById("bookingLink").hidden = remaining > 0;
}
updateRemaining();

let targetCards = 0, shuffledDeck = [], pickedIndices = [];

function prepareDeck(number) {
  const usage = getUsage();
  if (usage.count >= 3) {
    alert("今日免費次數已用完，明天再來！或直接預約專屬占卜。");
    document.getElementById("bookingLink").hidden = false;
    return;
  }
  if (!document.getElementById("question").value.trim()) {
    alert("請先輸入你想詢問的問題！");
    document.getElementById("question").focus();
    return;
  }

  targetCards = number;
  pickedIndices = [];
  shuffledDeck = [...tarotDeck].sort(() => Math.random() - 0.5);

  document.getElementById("drawResult").innerHTML = "";
  document.getElementById("pickHint").textContent = `請憑直覺從下方牌堆點選 ${number} 張牌背：`;

  const deckArea = document.getElementById("cardDeckArea");
  deckArea.innerHTML = "";

  for (let i = 0; i < 22; i++) {
    const cardBack = document.createElement("div");
    cardBack.className = "card-back";
    cardBack.textContent = "✦";
    cardBack.onclick = () => pickCard(i, cardBack);
    deckArea.appendChild(cardBack);
  }
}

function pickCard(index, element) {
  if (pickedIndices.includes(index) || pickedIndices.length >= targetCards) return;
  pickedIndices.push(index);
  element.classList.add("picked");
  element.textContent = "★";

  if (pickedIndices.length === targetCards) {
    let usage = getUsage();
    usage.count++;
    localStorage.setItem("starwovenUsage", JSON.stringify(usage));

    const positions = targetCards === 3 ? ["過去","現在","未來"] : ["目前指引"];
    let html = "";

    pickedIndices.forEach((deckIdx, i) => {
      const card = shuffledDeck[deckIdx];
      const direction = "正位";
      const interpretation = `這張牌呈現出能量的順暢流動。核心意涵指向：<strong>${card.meaning}</strong>。代表目前在此領域進展明朗，保持正向覺察即可。`;

      html += `
        <div class="tarot-card">
          <p>${positions[i]}</p>
          <h2>${card.name}</h2>
          <h3>${direction}</h3>
          <p>${card.suit}</p>
        </div>
        <div class="result">
          <h3>${card.name} ｜ ${direction}</h3>
          <p>${interpretation}</p>
        </div>
      `;
    });

    document.getElementById("drawResult").innerHTML = html;
    document.getElementById("cardDeckArea").innerHTML = "";
    document.getElementById("pickHint").textContent = "";
    updateRemaining();
    document.getElementById("bookingLink").hidden = false;
  }
}

// ===== 6. 預約表單送出 =====
document.getElementById("bookingDate").min = getToday();
document.getElementById("bookingForm").addEventListener("submit", function(event) {
  event.preventDefault();
  const booking = {
    name: document.getElementById("customerName").value,
    phone: document.getElementById("customerPhone").value,
    email: document.getElementById("customerEmail").value,
    date: document.getElementById("bookingDate").value,
    time: document.getElementById("bookingTime").value,
    service: document.getElementById("bookingService").value,
    question: document.getElementById("bookingQuestion").value,
    status: "待確認"
  };

  const bookings = JSON.parse(localStorage.getItem("starwovenBookings") || "[]");
  bookings.push(booking);
  localStorage.setItem("starwovenBookings", JSON.stringify(bookings));

  document.getElementById("bookingMessage").textContent = "✅ 預約已送出！老師確認後將會與您聯繫。";
  this.reset();
  renderAdminBookings();
});

// ==========================================
// 🔒 內部管理後台與登入/登出機制（密碼：aa141319）
// ==========================================
const ADMIN_PASSWORD = "aa141319";

// 對著左上角 🔮 點兩下（DblClick）觸發登入
document.getElementById("secretAdminTrigger").addEventListener("dblclick", () => {
  if (localStorage.getItem("starwovenAdminAuth") === "true") {
    openAdminPanel();
  } else {
    const pwd = prompt("請輸入塔羅師管理密碼：");
    if (pwd === ADMIN_PASSWORD) {
      localStorage.setItem("starwovenAdminAuth", "true");
      openAdminPanel();
      alert("✅ 登入成功！");
    } else if (pwd !== null) {
      alert("❌ 密碼錯誤！");
    }
  }
});

// 檢查是否已登入（若已登入則自動顯示後台）
if (localStorage.getItem("starwovenAdminAuth") === "true") {
  openAdminPanel();
}

function openAdminPanel() {
  document.getElementById("adminPanelContainer").style.display = "block";
  window.scrollTo({ top: document.body.scrollHeight, behavior: 'smooth' });
  initAdminData();
}

// 點擊登出才會登出
function adminLogout() {
  if (confirm("確定要登出管理後台嗎？")) {
    localStorage.removeItem("starwovenAdminAuth");
    document.getElementById("adminPanelContainer").style.display = "none";
    alert("🔒 已安全登出管理後台。");
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }
}

// 切換為客人視角（捲動回頂端，不清除登入狀態）
function switchToCustomerView() {
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

function initAdminData() {
  renderAdminEvents();
  renderAdminCalendar();
  renderAdminBookings();
  renderAdminServices();
  
  const saved = JSON.parse(localStorage.getItem("starwovenThemeSettings") || "null");
  if (saved) {
    document.getElementById("bgSparkle").value = saved.sparkle || "dots";
    document.getElementById("bgType").value = saved.type || "gradient";
    if (saved.type === "solid") {
      document.getElementById("singleColor").value = saved.color || "#1f1430";
    } else {
      document.getElementById("color1").value = saved.c1 || "#150b24";
      document.getElementById("color2").value = saved.c2 || "#2b1d3a";
      document.getElementById("color3").value = saved.c3 || "#1a0f2b";
      document.getElementById("color4").value = saved.c4 || "#332344";
    }
  }
  toggleBgInputs();
}

// 服務、原價與優惠後台管理
function renderAdminServices() {
  const services = getServices();
  const tbody = document.getElementById("adminServiceTable");
  tbody.innerHTML = services.map((s, idx) => `
    <tr>
      <td><strong>${s.name}</strong><br><small>${s.time}</small></td>
      <td>${s.time}</td>
      <td><input type="number" id="price_${idx}" value="${s.price}" style="margin:0; padding:6px; font-size:13px; width:90px;"></td>
      <td><input type="text" id="promo_${idx}" value="${s.promo || ''}" placeholder="例如：NT$700 或 限時優惠" style="margin:0; padding:6px; font-size:13px;"></td>
      <td><button class="btn-sm" style="background:#59416e; color:white;" onclick="updateService(${idx})">儲存</button></td>
    </tr>
  `).join("");
}

function updateService(idx) {
  const services = getServices();
  const newPrice = Number(document.getElementById(`price_${idx}`).value);
  const newPromo = document.getElementById(`promo_${idx}`).value.trim();

  if (isNaN(newPrice) || newPrice < 0) {
    alert("請輸入有效的金額數字！");
    return;
  }

  services[idx].price = newPrice;
  services[idx].promo = newPromo;
  localStorage.setItem("starwovenServices", JSON.stringify(services));
  renderServices();
  alert(`✅ ${services[idx].name} 的價格與優惠設定已更新！`);
}

document.getElementById("adminEventForm").addEventListener("submit", function(e) {
  e.preventDefault();
  const title = document.getElementById("evTitle").value;
  const endDate = document.getElementById("evEndDate").value;
  const content = document.getElementById("evContent").value;
  const fileInput = document.getElementById("evPhotoFile");

  const saveEv = (photoBase64) => {
    const events = JSON.parse(localStorage.getItem("starwovenEvents") || "[]");
    events.unshift({ title, endDate, content, photo: photoBase64 });
    localStorage.setItem("starwovenEvents", JSON.stringify(events));
    this.reset();
    renderAdminEvents();
    loadActiveEvents();
    alert("活動已成功上架！");
  };

  if (fileInput.files && fileInput.files[0]) {
    const reader = new FileReader();
    reader.onload = (ev) => saveEv(ev.target.result);
    reader.readAsDataURL(fileInput.files[0]);
  } else {
    saveEv("");
  }
});

function renderAdminEvents() {
  const events = JSON.parse(localStorage.getItem("starwovenEvents") || "[]");
  const list = document.getElementById("adminEventList");
  if (events.length === 0) {
    list.innerHTML = "<p style='color:#bca5d4;'>目前沒有上架中的活動。</p>";
    return;
  }
  list.innerHTML = events.map((ev, idx) => `
    <div style="border:1px solid rgba(188,165,212,0.3); padding:12px; border-radius:8px; margin-bottom:8px; display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; background:rgba(33,24,47,0.7);">
      <div style="text-align:left;">
        <strong>${ev.title}</strong>（截止：${ev.endDate}）<br><small>${ev.content}</small>
      </div>
      <button class="btn-danger btn-sm" onclick="deleteAdminEvent(${idx})">刪除下架</button>
    </div>
  `).join("");
}

function deleteAdminEvent(idx) {
  const events = JSON.parse(localStorage.getItem("starwovenEvents") || "[]");
  events.splice(idx, 1);
  localStorage.setItem("starwovenEvents", JSON.stringify(events));
  renderAdminEvents();
  loadActiveEvents();
}

function renderAdminCalendar() {
  const schedule = JSON.parse(localStorage.getItem("starwovenSchedule") || "{}");
  const calEl = document.getElementById("adminCalendar");
  const now = new Date();
  const year = now.getFullYear();
  const month = now.getMonth();

  const weekDays = ["日","一","二","三","四","五","六"];
  let html = weekDays.map(w => `<div class="admin-cal-head">${w}</div>`).join("");

  const firstDay = new Date(year, month, 1).getDay();
  const daysInMonth = new Date(year, month + 1, 0).getDate();

  for (let i = 0; i < firstDay; i++) html += `<div></div>`;

  for (let day = 1; day <= daysInMonth; day++) {
    const dateStr = `${year}-${String(month+1).padStart(2,"0")}-${String(day).padStart(2,"0")}`;
    const val = schedule[dateStr] || "";

    html += `
      <div class="admin-cal-cell ${val ? 'has-time' : ''}" onclick="editDaySchedule('${dateStr}')">
        <div style="font-weight:bold;">${month+1}/${day}</div>
        <div style="font-size:12px; color:#d0bde6; margin-top:6px;">
          ${val ? `<strong>${val}</strong>` : '<span style="color:#aaa;">點擊排班</span>'}
        </div>
      </div>
    `;
  }
  calEl.innerHTML = html;
}

function editDaySchedule(dateStr) {
  const schedule = JSON.parse(localStorage.getItem("starwovenSchedule") || "{}");
  const current = schedule[dateStr] || "";
  const input = prompt(`設定【${dateStr}】可預約時間：\n（例如輸入 7~11 或 13:00, 15:00）\n※ 清空文字即代表當天休息：`, current);

  if (input === null) return;
  if (input.trim() === "") {
    delete schedule[dateStr];
  } else {
    schedule[dateStr] = input.trim();
  }
  localStorage.setItem("starwovenSchedule", JSON.stringify(schedule));
  renderAdminCalendar();
  renderPublicCalendar();
}

function batchWeekdays() {
  const timeInput = prompt("請輸入週一至週五固定開放時間（例如：13:00~20:00 或 7~11）：", "13:00~20:00");
  if (!timeInput || !timeInput.trim()) return;

  const schedule = JSON.parse(localStorage.getItem("starwovenSchedule") || "{}");
  const now = new Date();
  const year = now.getFullYear();
  const month = now.getMonth();
  const daysInMonth = new Date(year, month + 1, 0).getDate();

  for (let day = 1; day <= daysInMonth; day++) {
    const d = new Date(year, month, day);
    const weekDay = d.getDay();
    if (weekDay !== 0 && weekDay !== 6) {
      const dateStr = `${year}-${String(month+1).padStart(2,"0")}-${String(day).padStart(2,"0")}`;
      schedule[dateStr] = timeInput.trim();
    }
  }
  localStorage.setItem("starwovenSchedule", JSON.stringify(schedule));
  renderAdminCalendar();
  renderPublicCalendar();
  alert("已完成本月週一至週五排班設定！");
}

function clearCalendar() {
  if (!confirm("確定要一鍵清空本月所有排班嗎？")) return;
  localStorage.removeItem("starwovenSchedule");
  renderAdminCalendar();
  renderPublicCalendar();
}

function renderAdminBookings() {
  const bookings = JSON.parse(localStorage.getItem("starwovenBookings") || "[]");
  const tbody = document.getElementById("adminBookingTable");

  if (bookings.length === 0) {
    tbody.innerHTML = `<tr><td colspan="8" style="text-align:center; color:#bca5d4;">目前尚無客人預約</td></tr>`;
    return;
  }

  tbody.innerHTML = bookings.map((b, i) => `
    <tr>
      <td><strong>${b.date}</strong><br>${b.time}</td>
      <td>${b.name}</td>
      <td>${b.phone}</td>
      <td>${b.email}</td>
      <td>${b.service}</td>
      <td>${b.question || "（未填寫）"}</td>
      <td><span style="background:#59416e; padding:4px 8px; border-radius:6px;">${b.status}</span></td>
      <td>
        <button class="btn-sm" style="background:#59416e; color:white;" onclick="changeStatus(${i}, '已確認')">確認</button>
        <button class="btn-danger btn-sm" onclick="deleteBooking(${i})">刪除</button>
      </td>
    </tr>
  `).join("");
}

function changeStatus(i, status) {
  const bookings = JSON.parse(localStorage.getItem("starwovenBookings") || "[]");
  bookings[i].status = status;
  localStorage.setItem("starwovenBookings", JSON.stringify(bookings));
  renderAdminBookings();
}

function deleteBooking(i) {
  if (!confirm("確定要刪除這筆預約紀錄嗎？")) return;
  const bookings = JSON.parse(localStorage.getItem("starwovenBookings") || "[]");
  bookings.splice(i, 1);
  localStorage.setItem("starwovenBookings", JSON.stringify(bookings));
  renderAdminBookings();
}
</script>

</body>
</html>

