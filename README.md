<html lang="th" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>คณิตศาสตร์การเงิน ป.5</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://cdn.jsdelivr.net/npm/lucide@0.263.0/dist/umd/lucide.min.js"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet">
  <style>
    body {
      box-sizing: border-box;
      font-family: 'Kanit', sans-serif;
    }
    @keyframes bounce-coin {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }
    @keyframes sparkle {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.5; transform: scale(1.2); }
    }
    @keyframes slide-up {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-8px); }
    }
    @keyframes pulse-glow {
      0%, 100% { box-shadow: 0 0 0 0 rgba(255, 105, 180, 0.3); }
      50% { box-shadow: 0 0 0 10px rgba(255, 105, 180, 0); }
    }
    .coin-bounce { animation: bounce-coin 2s ease-in-out infinite; }
    .sparkle { animation: sparkle 1.5s ease-in-out infinite; }
    .slide-up { animation: slide-up 0.5s ease-out forwards; }
    .float-animation { animation: float 3s ease-in-out infinite; }
    .pulse-glow { animation: pulse-glow 2s infinite; }
    .coin-gold {
      background: linear-gradient(135deg, #FFD700 0%, #FFA500 50%, #FFD700 100%);
      box-shadow: 0 4px 15px rgba(255, 215, 0, 0.4);
    }
    .bill-gradient {
      background: linear-gradient(135deg, #FF69B4 0%, #FF1493 100%);
      box-shadow: 0 4px 15px rgba(255, 20, 147, 0.3);
    }
    .sticker-emoji {
      display: inline-block;
      animation: float 3s ease-in-out infinite;
    }
    .sticker-star { animation-delay: 0s; }
    .sticker-heart { animation-delay: 0.5s; }
    .sticker-flower { animation-delay: 1s; }
    .sticker-sparkle { animation-delay: 1.5s; }
    .cloud {
      position: absolute;
      background: white;
      border-radius: 100px;
      opacity: 0.85;
      box-shadow: 0 4px 15px rgba(255, 105, 180, 0.15);
    }
    .cloud::before,
    .cloud::after {
      content: '';
      position: absolute;
      background: white;
      border-radius: 100px;
    }
    .cloud::before {
      width: 50px;
      height: 50px;
      top: -25px;
      left: 10px;
    }
    .cloud::after {
      width: 40px;
      height: 40px;
      top: -15px;
      right: 10px;
    }
    @keyframes drift {
      0%, 100% { transform: translateX(0); }
      50% { transform: translateX(20px); }
    }
    .cloud-drift { animation: drift 6s ease-in-out infinite; }
    .cloud1 { animation-delay: 0s; }
    .cloud2 { animation-delay: 2s; }
    .cloud3 { animation-delay: 4s; }
  </style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
  <script src="https://cdn.tailwindcss.com/3.4.17" type="text/javascript"></script>
 <script src="/_sdk/telemetry_sdk.js"></script></head>
 <body class="h-full m-0 p-0 overflow-auto">
  <div id="app-container" class="min-h-full w-full relative" style="background: linear-gradient(135deg, #FFB6D9 0%, #FFC0E0 25%, #FFD9EF 50%, #FFE6F5 75%, #FFF0FA 100%);">
   <!-- Floating clouds -->
   <div class="cloud cloud-drift cloud1" style="width: 100px; height: 50px; top: 5%; left: 10%;"></div>
   <div class="cloud cloud-drift cloud2" style="width: 80px; height: 40px; top: 20%; right: 15%;"></div>
   <div class="cloud cloud-drift cloud3" style="width: 120px; height: 60px; top: 40%; left: 5%;"></div>
   <div class="cloud cloud-drift cloud1" style="width: 90px; height: 45px; top: 60%; right: 8%;"></div><!-- Floating stickers -->
   <div class="fixed top-10 right-10 text-4xl sticker-emoji sticker-star opacity-60 pointer-events-none">
    ⭐
   </div>
   <div class="fixed bottom-20 left-10 text-5xl sticker-emoji sticker-heart opacity-50 pointer-events-none">
    💖
   </div>
   <div class="fixed top-1/2 right-5 text-4xl sticker-emoji sticker-flower opacity-60 pointer-events-none">
    🌸
   </div>
   <div class="fixed bottom-1/3 right-1/4 text-3xl sticker-emoji sticker-sparkle opacity-70 pointer-events-none">
    ✨
   </div><!-- Header -->
   <header class="text-center py-6 px-4">
    <div class="flex justify-center items-center gap-3 mb-2">
     <span class="text-4xl coin-bounce">💰</span>
     <h1 id="main-title" class="text-3xl md:text-4xl font-bold text-white drop-shadow-lg" style="text-shadow: 2px 2px 4px rgba(255, 105, 180, 0.3);">คณิตศาสตร์การเงิน ป.5</h1><span class="text-4xl coin-bounce" style="animation-delay: 0.5s;">🪙</span>
    </div>
    <p id="welcome-text" class="text-lg text-white/90 mb-3">เรียนรู้เรื่องเงินอย่างสนุกสนาน!</p>
    <div id="teacher-section" class="inline-flex items-center gap-2 bg-white/30 backdrop-blur-sm rounded-full px-4 py-2">
     <span class="text-2xl">👩‍🏫</span>
     <p id="teacher-name" class="text-white font-semibold">ครูวิรัลพัชษ์ สว่างเดือน</p>
    </div>
   </header><!-- Score Display -->
   <div class="flex justify-center gap-4 px-4 mb-6 flex-wrap">
    <div class="bg-white/40 backdrop-blur-sm rounded-2xl px-6 py-3 text-white text-center border-2 border-white/50 pulse-glow">
     <div class="text-sm opacity-90 font-semibold">
      🎯 คะแนน
     </div>
     <div id="score" class="text-2xl font-bold">
      0
     </div>
    </div>
    <div class="bg-white/40 backdrop-blur-sm rounded-2xl px-6 py-3 text-white text-center border-2 border-white/50">
     <div class="text-sm opacity-90 font-semibold">
      📝 ข้อที่
     </div>
     <div id="question-num" class="text-2xl font-bold">
      1/10
     </div>
    </div>
    <div class="bg-white/40 backdrop-blur-sm rounded-2xl px-6 py-3 text-white text-center border-2 border-white/50">
     <div class="text-sm opacity-90 font-semibold">
      🔥 ถูกต้อง
     </div>
     <div id="streak" class="text-2xl font-bold">
      🔥 0
     </div>
    </div>
   </div><!-- Main Game Area -->
   <main class="px-4 pb-8">
    <!-- Topic Selection -->
    <div id="topic-selection" class="max-w-2xl mx-auto">
     <div class="bg-white rounded-3xl shadow-2xl p-6 md:p-8">
      <h2 class="text-2xl font-bold text-center mb-2" style="color: #FF1493;">🎨 เลือกหัวข้อที่ต้องการฝึก</h2>
      <p class="text-center text-gray-500 mb-6 text-sm">เลือกเรื่องที่อยากฝึก แล้วเริ่มเล่น!</p>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
       <button onclick="startGame('counting')" class="group relative overflow-hidden rounded-2xl p-6 text-left transition-all hover:scale-105 hover:shadow-xl" style="background: linear-gradient(135deg, #FFB6C1 0%, #FFB0D1 100%); border: 2px solid #FF69B4;">
        <div class="text-4xl mb-3 group-hover:scale-125 transition-transform">
         🧮
        </div><h3 class="text-xl font-bold text-white">นับเงิน</h3><p class="text-white/90 text-sm">ฝึกนับเหรียญและธนบัตร</p>
        <div class="absolute top-2 right-2 text-white/30 text-6xl group-hover:text-white/50 transition-colors">
         💵
        </div></button> <button onclick="startGame('change')" class="group relative overflow-hidden rounded-2xl p-6 text-left transition-all hover:scale-105 hover:shadow-xl" style="background: linear-gradient(135deg, #FFD9E8 0%, #FFC0E0 100%); border: 2px solid #FF69B4;">
        <div class="text-4xl mb-3 group-hover:scale-125 transition-transform">
         🛒
        </div><h3 class="text-xl font-bold text-white">ทอนเงิน</h3><p class="text-white/90 text-sm">คำนวณเงินทอน</p>
        <div class="absolute top-2 right-2 text-white/30 text-6xl group-hover:text-white/50 transition-colors">
         🧾
        </div></button> <button onclick="startGame('shopping')" class="group relative overflow-hidden rounded-2xl p-6 text-left transition-all hover:scale-105 hover:shadow-xl" style="background: linear-gradient(135deg, #FFE0E8 0%, #FFD9E8 100%); border: 2px solid #FF1493;">
        <div class="text-4xl mb-3 group-hover:scale-125 transition-transform">
         🏪
        </div><h3 class="text-xl font-bold text-white">ช้อปปิ้ง</h3><p class="text-white/90 text-sm">คำนวณราคาสินค้า</p>
        <div class="absolute top-2 right-2 text-white/30 text-6xl group-hover:text-white/50 transition-colors">
         🛍️
        </div></button> <button onclick="startGame('budget')" class="group relative overflow-hidden rounded-2xl p-6 text-left transition-all hover:scale-105 hover:shadow-xl" style="background: linear-gradient(135deg, #FFC9D7 0%, #FFB6C1 100%); border: 2px solid #FF69B4;">
        <div class="text-4xl mb-3 group-hover:scale-125 transition-transform">
         📊
        </div><h3 class="text-xl font-bold text-white">งบประมาณ</h3><p class="text-white/90 text-sm">วางแผนการใช้เงิน</p>
        <div class="absolute top-2 right-2 text-white/30 text-6xl group-hover:text-white/50 transition-colors">
         💹
        </div></button>
      </div>
     </div>
    </div><!-- Question Area -->
    <div id="question-area" class="max-w-2xl mx-auto hidden">
     <div class="bg-white rounded-3xl shadow-2xl p-6 md:p-8 slide-up">
      <!-- Money Display -->
      <div id="money-display" class="flex flex-wrap justify-center gap-3 mb-6 min-h-[80px]"></div><!-- Question -->
      <div id="question-box" class="bg-gradient-to-r from-pink-100 to-rose-100 rounded-2xl p-6 mb-6 border-2 border-pink-200">
       <p id="question-text" class="text-xl text-center text-gray-800 font-medium"></p>
      </div><!-- Answer Options -->
      <div id="answer-options" class="grid grid-cols-2 gap-4 mb-6"></div><!-- Input Answer -->
      <div id="input-answer" class="hidden mb-6">
       <div class="flex gap-3 justify-center items-center">
        <input type="number" id="answer-input" class="w-40 px-4 py-3 text-2xl text-center border-3 rounded-xl focus:outline-none focus:ring-4" style="border-color: #FF69B4; background: #FFF0FA;" placeholder="?"> <span class="text-xl text-gray-600 font-medium">บาท</span>
       </div><button onclick="checkInputAnswer()" class="mt-4 w-full text-white py-3 rounded-xl font-bold text-lg hover:opacity-90 transition-opacity" style="background: linear-gradient(135deg, #FF1493 0%, #FF69B4 100%);">ตรวจคำตอบ</button>
      </div><!-- Feedback -->
      <div id="feedback" class="hidden text-center py-4 rounded-2xl mb-4">
       <div id="feedback-icon" class="text-5xl mb-2"></div>
       <p id="feedback-text" class="text-xl font-bold"></p>
       <p id="feedback-explanation" class="text-gray-600 mt-2"></p>
      </div><!-- Next Button --> <button id="next-btn" onclick="nextQuestion()" class="hidden w-full text-white py-4 rounded-xl font-bold text-lg hover:opacity-90 transition-opacity" style="background: linear-gradient(135deg, #FF69B4 0%, #FF1493 100%);"> ข้อถัดไป ➡️ </button>
     </div>
    </div><!-- Results -->
    <div id="results-area" class="max-w-2xl mx-auto hidden">
     <div class="bg-white rounded-3xl shadow-2xl p-8 text-center slide-up">
      <div class="text-6xl mb-4 sparkle">
       🏆
      </div>
      <h2 class="text-3xl font-bold mb-2" style="color: #FF1493;">ยินดีด้วย!</h2>
      <p id="final-score" class="text-xl text-gray-600 mb-6"></p>
      <div id="stars-display" class="flex justify-center gap-2 mb-6"></div>
      <div id="achievement" class="rounded-2xl p-4 mb-6 border-2 border-pink-200" style="background: linear-gradient(135deg, #FFE6F5 0%, #FFD9EF 100%);">
       <p id="achievement-text" class="text-lg font-medium" style="color: #FF1493;"></p>
      </div>
      <div class="flex gap-4">
       <button onclick="restartGame()" class="flex-1 text-white py-4 rounded-xl font-bold text-lg hover:opacity-90 transition-opacity" style="background: linear-gradient(135deg, #FF69B4 0%, #FF1493 100%);"> 🔄 เล่นอีกครั้ง </button> <button onclick="goToMenu()" class="flex-1 text-white py-4 rounded-xl font-bold text-lg hover:opacity-90 transition-opacity" style="background: linear-gradient(135deg, #DDA0DD 0%, #DA70D6 100%);"> 📋 เลือกหัวข้อใหม่ </button>
      </div>
     </div>
    </div>
   </main>
  </div>
  <script>
    // Configuration
    const defaultConfig = {
      app_title: 'คณิตศาสตร์การเงิน ป.5',
      welcome_message: 'เรียนรู้เรื่องเงินอย่างสนุกสนาน!',
      teacher_name: 'ครูวิรัลพัชษ์ สว่างเดือน'
    };

    let config = { ...defaultConfig };

    // Game State
    let currentTopic = '';
    let currentQuestion = 0;
    let score = 0;
    let streak = 0;
    let questions = [];
    let correctAnswer = 0;
    const totalQuestions = 10;

    // Thai currency
    const coins = [
      { value: 10, emoji: '🪙', label: '10 บาท', color: '#C0C0C0' },
      { value: 5, emoji: '🪙', label: '5 บาท', color: '#C0C0C0' },
      { value: 2, emoji: '🪙', label: '2 บาท', color: '#CD7F32' },
      { value: 1, emoji: '🪙', label: '1 บาท', color: '#CD7F32' },
      { value: 0.50, emoji: '🪙', label: '50 สตางค์', color: '#CD7F32' },
      { value: 0.25, emoji: '🪙', label: '25 สตางค์', color: '#CD7F32' }
    ];

    const bills = [
      { value: 1000, emoji: '💵', label: '1,000 บาท', color: '#8B4513' },
      { value: 500, emoji: '💵', label: '500 บาท', color: '#800080' },
      { value: 100, emoji: '💵', label: '100 บาท', color: '#DC143C' },
      { value: 50, emoji: '💵', label: '50 บาท', color: '#4169E1' },
      { value: 20, emoji: '💵', label: '20 บาท', color: '#228B22' }
    ];

    const shopItems = [
      { name: 'ขนมปัง', emoji: '🍞', priceRange: [15, 35] },
      { name: 'นม', emoji: '🥛', priceRange: [12, 25] },
      { name: 'ไข่ 1 แผง', emoji: '🥚', priceRange: [50, 80] },
      { name: 'แอปเปิ้ล', emoji: '🍎', priceRange: [20, 40] },
      { name: 'ข้าวกล่อง', emoji: '🍱', priceRange: [35, 60] },
      { name: 'น้ำผลไม้', emoji: '🧃', priceRange: [15, 30] },
      { name: 'ขนมถุง', emoji: '🍪', priceRange: [10, 25] },
      { name: 'ไอศกรีม', emoji: '🍦', priceRange: [20, 45] },
      { name: 'ปากกา', emoji: '🖊️', priceRange: [10, 30] },
      { name: 'สมุด', emoji: '📓', priceRange: [15, 40] }
    ];

    // Initialize SDK
    if (window.elementSdk) {
      window.elementSdk.init({
        defaultConfig,
        onConfigChange: async (newConfig) => {
          config = { ...defaultConfig, ...newConfig };
          updateUI();
        },
        mapToCapabilities: (cfg) => ({
          recolorables: [],
          borderables: [],
          fontEditable: undefined,
          fontSizeable: undefined
        }),
        mapToEditPanelValues: (cfg) => new Map([
          ['app_title', cfg.app_title || defaultConfig.app_title],
          ['welcome_message', cfg.welcome_message || defaultConfig.welcome_message],
          ['teacher_name', cfg.teacher_name || defaultConfig.teacher_name]
        ])
      });
    }

    function updateUI() {
      document.getElementById('main-title').textContent = config.app_title || defaultConfig.app_title;
      document.getElementById('welcome-text').textContent = config.welcome_message || defaultConfig.welcome_message;
      document.getElementById('teacher-name').textContent = config.teacher_name || defaultConfig.teacher_name;
    }

    // Utility Functions
    function randomInt(min, max) {
      return Math.floor(Math.random() * (max - min + 1)) + min;
    }

    function shuffle(array) {
      const arr = [...array];
      for (let i = arr.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [arr[i], arr[j]] = [arr[j], arr[i]];
      }
      return arr;
    }

    function formatMoney(amount) {
      if (amount % 1 === 0) {
        return amount.toLocaleString();
      }
      return amount.toFixed(2);
    }

    // Money Display Functions
    function createCoinElement(coin, count) {
      const div = document.createElement('div');
      div.className = 'flex flex-col items-center';
      div.innerHTML = `
        <div class="coin-gold w-12 h-12 rounded-full flex items-center justify-center text-white font-bold text-sm shadow-lg">
          ${coin.value >= 1 ? coin.value : (coin.value * 100)}
        </div>
        <span class="text-xs text-gray-600 mt-1 font-medium">x${count}</span>
      `;
      return div;
    }

    function createBillElement(bill, count) {
      const div = document.createElement('div');
      div.className = 'flex flex-col items-center';
      div.innerHTML = `
        <div class="bill-gradient w-16 h-10 rounded-lg flex items-center justify-center text-white font-bold text-sm shadow-lg">
          ${bill.value}
        </div>
        <span class="text-xs text-gray-600 mt-1 font-medium">x${count}</span>
      `;
      return div;
    }

    // Question Generators
    function generateCountingQuestion() {
      const moneyDisplay = document.getElementById('money-display');
      moneyDisplay.innerHTML = '';
      
      const selectedBills = [];
      const selectedCoins = [];
      let total = 0;

      const billCount = randomInt(1, 3);
      for (let i = 0; i < billCount; i++) {
        const bill = bills[randomInt(2, 4)];
        const count = randomInt(1, 2);
        selectedBills.push({ ...bill, count });
        total += bill.value * count;
      }

      const coinCount = randomInt(1, 4);
      for (let i = 0; i < coinCount; i++) {
        const coin = coins[randomInt(0, 3)];
        const count = randomInt(1, 3);
        selectedCoins.push({ ...coin, count });
        total += coin.value * count;
      }

      selectedBills.forEach(b => moneyDisplay.appendChild(createBillElement(b, b.count)));
      selectedCoins.forEach(c => moneyDisplay.appendChild(createCoinElement(c, c.count)));

      correctAnswer = total;
      
      return {
        text: '💰 เงินทั้งหมดในภาพมีกี่บาท?',
        answer: total,
        type: 'multiple'
      };
    }

    function generateChangeQuestion() {
      const moneyDisplay = document.getElementById('money-display');
      moneyDisplay.innerHTML = '';

      const item = shopItems[randomInt(0, shopItems.length - 1)];
      const price = randomInt(item.priceRange[0], item.priceRange[1]);
      const paidOptions = [50, 100, 200, 500];
      const paid = paidOptions.find(p => p > price) || 500;
      const change = paid - price;

      moneyDisplay.innerHTML = `
        <div class="flex items-center gap-4 bg-pink-100 rounded-2xl p-4 w-full justify-center border-2 border-pink-200">
          <span class="text-5xl">${item.emoji}</span>
          <div class="text-left">
            <div class="font-bold text-lg text-gray-800">${item.name}</div>
            <div class="font-bold text-xl" style="color: #FF1493;">${price} บาท</div>
          </div>
        </div>
      `;

      correctAnswer = change;

      return {
        text: `🛒 ซื้อ${item.name}ราคา ${price} บาท จ่ายเงิน ${paid} บาท จะได้เงินทอนเท่าไร?`,
        answer: change,
        type: 'multiple'
      };
    }

    function generateShoppingQuestion() {
      const moneyDisplay = document.getElementById('money-display');
      moneyDisplay.innerHTML = '';

      const itemCount = randomInt(2, 3);
      const shuffledItems = shuffle(shopItems);
      const selectedItems = shuffledItems.slice(0, itemCount);
      
      let total = 0;
      const itemsHtml = selectedItems.map(item => {
        const price = randomInt(item.priceRange[0], item.priceRange[1]);
        total += price;
        return `
          <div class="flex flex-col items-center bg-rose-100 rounded-xl p-3 border border-pink-300">
            <span class="text-3xl mb-1">${item.emoji}</span>
            <span class="text-sm text-gray-700">${item.name}</span>
            <span class="font-bold" style="color: #FF1493;">${price} บาท</span>
          </div>
        `;
      }).join('');

      moneyDisplay.innerHTML = `<div class="flex flex-wrap justify-center gap-3 w-full">${itemsHtml}</div>`;

      correctAnswer = total;

      return {
        text: '🧮 รวมราคาสินค้าทั้งหมดเท่าไร?',
        answer: total,
        type: 'multiple'
      };
    }

    function generateBudgetQuestion() {
      const moneyDisplay = document.getElementById('money-display');
      moneyDisplay.innerHTML = '';

      const scenarios = [
        {
          text: (budget, spent) => `📊 มีเงินค่าขนม ${budget} บาทต่อสัปดาห์ ใช้ไปแล้ว ${spent} บาท เหลือเงินเท่าไร?`,
          budget: () => randomInt(100, 300),
          spent: (b) => randomInt(Math.floor(b * 0.3), Math.floor(b * 0.7))
        },
        {
          text: (target, saved) => `🎯 ต้องการเก็บเงิน ${target} บาท เก็บได้แล้ว ${saved} บาท ต้องเก็บเพิ่มอีกเท่าไร?`,
          budget: () => randomInt(200, 500),
          spent: (b) => randomInt(Math.floor(b * 0.2), Math.floor(b * 0.6))
        },
        {
          text: (daily, days) => `💵 ได้ค่าขนมวันละ ${daily} บาท ใน ${days} วัน จะมีเงินรวมเท่าไร?`,
          budget: () => randomInt(20, 50),
          spent: () => randomInt(5, 7),
          calc: 'multiply'
        }
      ];

      const scenario = scenarios[randomInt(0, scenarios.length - 1)];
      const budget = scenario.budget();
      const spent = scenario.spent(budget);
      
      let answer;
      if (scenario.calc === 'multiply') {
        answer = budget * spent;
      } else {
        answer = budget - spent;
      }

      const emoji = scenario.calc === 'multiply' ? '📅' : '💰';
      moneyDisplay.innerHTML = `
        <div class="text-center p-4 bg-rose-100 rounded-2xl w-full border-2 border-pink-200">
          <span class="text-5xl">${emoji}</span>
        </div>
      `;

      correctAnswer = answer;

      return {
        text: scenario.text(budget, spent),
        answer: answer,
        type: 'multiple'
      };
    }

    // Generate Wrong Answers
    function generateWrongAnswers(correct) {
      const wrongs = new Set();
      
      while (wrongs.size < 3) {
        const offset = randomInt(1, Math.max(20, Math.floor(correct * 0.3)));
        const wrong = Math.random() > 0.5 ? correct + offset : correct - offset;
        if (wrong > 0 && wrong !== correct) {
          wrongs.add(wrong);
        }
      }
      
      return Array.from(wrongs);
    }

    // Game Functions
    function startGame(topic) {
      currentTopic = topic;
      currentQuestion = 0;
      score = 0;
      streak = 0;
      questions = [];
      
      updateScoreDisplay();
      
      document.getElementById('topic-selection').classList.add('hidden');
      document.getElementById('question-area').classList.remove('hidden');
      document.getElementById('results-area').classList.add('hidden');
      
      showQuestion();
    }

    function showQuestion() {
      currentQuestion++;
      document.getElementById('question-num').textContent = `${currentQuestion}/${totalQuestions}`;
      document.getElementById('feedback').classList.add('hidden');
      document.getElementById('next-btn').classList.add('hidden');
      
      let question;
      switch (currentTopic) {
        case 'counting':
          question = generateCountingQuestion();
          break;
        case 'change':
          question = generateChangeQuestion();
          break;
        case 'shopping':
          question = generateShoppingQuestion();
          break;
        case 'budget':
          question = generateBudgetQuestion();
          break;
        default:
          question = generateCountingQuestion();
      }

      document.getElementById('question-text').textContent = question.text;
      
      const optionsContainer = document.getElementById('answer-options');
      optionsContainer.innerHTML = '';
      document.getElementById('input-answer').classList.add('hidden');
      optionsContainer.classList.remove('hidden');

      const wrongAnswers = generateWrongAnswers(question.answer);
      const allAnswers = shuffle([question.answer, ...wrongAnswers]);

      allAnswers.forEach(answer => {
        const btn = document.createElement('button');
        btn.className = 'text-gray-800 font-bold py-4 px-6 rounded-xl text-xl transition-all hover:scale-105 border-2 border-transparent hover:border-pink-300';
        btn.style.background = 'linear-gradient(135deg, #FFE6F5 0%, #FFD9EF 100%)';
        btn.textContent = `${formatMoney(answer)} บาท`;
        btn.onclick = () => checkAnswer(answer);
        optionsContainer.appendChild(btn);
      });
    }

    function checkAnswer(selected) {
      const isCorrect = selected === correctAnswer;
      showFeedback(isCorrect);
      
      const options = document.querySelectorAll('#answer-options button');
      options.forEach(btn => {
        btn.disabled = true;
        const btnValue = parseFloat(btn.textContent.replace(/[^0-9.]/g, ''));
        if (btnValue === correctAnswer) {
          btn.style.background = 'linear-gradient(135deg, #90EE90 0%, #7FD77F 100%)';
          btn.classList.add('border-green-500');
        } else if (btnValue === selected && !isCorrect) {
          btn.style.background = 'linear-gradient(135deg, #FFB6C1 0%, #FFA6B1 100%)';
          btn.classList.add('border-red-500');
        }
      });
    }

    function checkInputAnswer() {
      const input = document.getElementById('answer-input');
      const selected = parseFloat(input.value);
      
      if (isNaN(selected)) {
        input.style.borderColor = '#FF1493';
        return;
      }

      const isCorrect = selected === correctAnswer;
      showFeedback(isCorrect);
      input.disabled = true;
    }

    function showFeedback(isCorrect) {
      const feedback = document.getElementById('feedback');
      const icon = document.getElementById('feedback-icon');
      const text = document.getElementById('feedback-text');
      const explanation = document.getElementById('feedback-explanation');

      if (isCorrect) {
        score += 10 + streak * 2;
        streak++;
        
        feedback.className = 'text-center py-4 rounded-2xl mb-4';
        feedback.style.background = 'linear-gradient(135deg, #FFE6F5 0%, #FFD9EF 100%)';
        feedback.style.borderTop = '3px solid #FF1493';
        icon.textContent = ['🎉', '🌟', '✨', '🏆', '👏'][randomInt(0, 4)];
        text.textContent = ['เก่งมาก!', 'ยอดเยี่ยม!', 'ถูกต้อง!', 'สุดยอด!', 'เยี่ยมเลย!'][randomInt(0, 4)];
        text.style.color = '#FF1493';
        explanation.textContent = streak > 1 ? `🔥 ตอบถูกติดต่อกัน ${streak} ข้อ! +${streak * 2} โบนัส` : '';
      } else {
        streak = 0;
        
        feedback.className = 'text-center py-4 rounded-2xl mb-4';
        feedback.style.background = 'linear-gradient(135deg, #FFB6C1 0%, #FFA6B1 100%)';
        feedback.style.borderTop = '3px solid #FF1493';
        icon.textContent = '😅';
        text.textContent = 'ไม่ถูกต้อง';
        text.style.color = '#C2185B';
        explanation.textContent = `คำตอบที่ถูกต้องคือ ${formatMoney(correctAnswer)} บาท`;
      }

      feedback.classList.remove('hidden');
      document.getElementById('next-btn').classList.remove('hidden');
      updateScoreDisplay();
    }

    function updateScoreDisplay() {
      document.getElementById('score').textContent = score;
      document.getElementById('streak').textContent = `🔥 ${streak}`;
    }

    function nextQuestion() {
      if (currentQuestion >= totalQuestions) {
        showResults();
      } else {
        showQuestion();
      }
    }

    function showResults() {
      document.getElementById('question-area').classList.add('hidden');
      document.getElementById('results-area').classList.remove('hidden');

      const percentage = Math.round((score / (totalQuestions * 10)) * 100);
      
      document.getElementById('final-score').textContent = `คุณทำได้ ${score} คะแนน (${percentage}%)`;

      const starsDisplay = document.getElementById('stars-display');
      const starCount = percentage >= 90 ? 3 : percentage >= 70 ? 2 : percentage >= 50 ? 1 : 0;
      starsDisplay.innerHTML = Array(3).fill(0).map((_, i) => 
        `<span class="text-4xl">${i < starCount ? '⭐' : '☆'}</span>`
      ).join('');

      const achievements = [
        { min: 90, text: '🏆 ยอดเยี่ยม! คุณเป็นนักคณิตศาสตร์การเงินตัวจริง!' },
        { min: 70, text: '🌟 ดีมาก! คุณเข้าใจเรื่องเงินได้ดี!' },
        { min: 50, text: '👍 พยายามดี! ฝึกฝนต่อไปนะ!' },
        { min: 0, text: '💪 ไม่เป็นไร! ลองฝึกใหม่อีกครั้ง!' }
      ];

      const achievement = achievements.find(a => percentage >= a.min);
      document.getElementById('achievement-text').textContent = achievement.text;
    }

    function restartGame() {
      startGame(currentTopic);
    }

    function goToMenu() {
      document.getElementById('topic-selection').classList.remove('hidden');
      document.getElementById('question-area').classList.add('hidden');
      document.getElementById('results-area').classList.add('hidden');
      currentQuestion = 0;
      score = 0;
      streak = 0;
      updateScoreDisplay();
      document.getElementById('question-num').textContent = '1/10';
    }

    // Initialize
    updateUI();
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'a04b822328693437',t:'MTc4MDI4ODQ5Mg=='};var a=document.createElement('script');a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
