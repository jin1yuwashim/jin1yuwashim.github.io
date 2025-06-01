<!DOCTYPE html>
<html lang="zh-Hant">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>我的個人介紹網站</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <style>
    html {
      scroll-padding-top: 70px;
    }

    section {
      padding: 60px 0;
      min-height: 75vh;
      position: relative;
      scroll-margin-top: 70px;
    }

    .nav-link {
      color: rgba(255, 255, 255, 0.55);
      transition: color 0.3s;
    }

    .nav-link.active {
      color: #fff !important;
      font-weight: bold;
    }

    .navbar {
      height: 70px;
    }

    .section-image {
      position: absolute;
      bottom: 15px;
      right: 15px;
      width: 120px;
      height: 80px;
      overflow: hidden;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
      background-color: #fff;
    }

    .section-image img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }
  </style>
</head>

<body>

  <!-- 導覽列 -->
  <nav id="navbar" class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top">
    <div class="container">
      <a class="navbar-brand" href="#">我的簡介</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navContent">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navContent">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item">
            <a class="nav-link" href="#about">個人介紹</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#education">教育背景</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#skills">專業技能</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- 個人介紹 -->
  <section id="about" class="bg-light" style="padding-top: 100px;">
    <div class="container">
      <h2 class="text-center mb-4">👤 個人介紹</h2>
      <div class="row align-items-center">
        <div class="col-md-4 text-center">
          <div class="mx-auto mb-3"
            style="width: 300px; height: 300px; overflow: hidden; border-radius: 50%; box-shadow: 0 0 10px rgba(0,0,0,0.2);">
            <img src="IMG_6224.jpg" alt="大頭照" style="width: 100%; height: 100%; object-fit: cover;">
          </div>
        </div>
        <div class="col-md-8">
          <p style="font-size: 1.1rem;">
            我是劉冠緯，一位對資訊產業抱有期待的學生。在聯合大學主修資訊管理，熱愛唱歌和玩遊戲。<br>
            目前正在彌補自己過去缺失的知識，並且累積自己的底蘊和探索其他領域的興趣。<br>
            未來想往資訊安全與網路的方向前進，希望在做專題的這一年能夠累積更深厚的技術，讓自己在未來就職時能夠更有競爭力。<br>
            而我也相信努力必然會看見成效的，只要一直往前邁進、不斷學習，時間自然會記錄下你一路行走過來的軌跡。
          </p>
        </div>
      </div>
    </div>
    <div class="section-image">
      <img src="img300.jpg" alt="個人介紹圖示">
    </div>
  </section>

  <!-- 教育背景 -->
  <section id="education">
    <div class="container">
      <h2 class="text-center mb-4">🎓 教育背景</h2>
      <ul class="list-group list-group-flush">
        <li class="list-group-item">2023 - 至今：聯合大學 資訊管理系</li>
        <li class="list-group-item">2021 - 2023：新竹高商 資訊處理科</li>
      </ul>
    </div>
    <div class="section-image">
      <img src="img300.jpg" alt="教育背景圖示">
    </div>
  </section>

  <!-- 專業技能 -->
  <section id="skills" class="bg-light">
    <div class="container">
      <h2 class="text-center mb-4">🛠️ 專業技能</h2>
      <div class="row">
        <div class="col-md-4">
          <div class="card shadow-sm">
            <div class="card-body">
              <h5 class="card-title">網頁開發</h5>
              <p class="card-text">熟悉 HTML、CSS，正在學習 JavaScript 與 Python。</p>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card shadow-sm">
            <div class="card-body">
              <h5 class="card-title">資料處理</h5>
              <p class="card-text">會使用 Excel、SQL 進行資料清理與整理，也擅長文字編輯。</p>
            </div>
          </div>
        </div>
        <div class="col-md-4">
          <div class="card shadow-sm">
            <div class="card-body">
              <h5 class="card-title">團隊合作</h5>
              <p class="card-text">有專題和小組報告經驗，擅長溝通與協作。</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="section-image">
      <img src="img300.jpg" alt="專業技能圖示">
    </div>
  </section>

 

  <!-- Bootstrap JS -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>

  <!-- 導覽列點擊和滾動高亮功能 -->
  <script>
    // 等待頁面完全載入
    document.addEventListener('DOMContentLoaded', function() {
      // 取得所有導覽連結和區段
      const navLinks = document.querySelectorAll('.nav-link');
      const sections = document.querySelectorAll('section[id]');
      
      let isScrolling = false; // 標記是否正在滾動
      
      // 點擊導覽連結時的處理
      navLinks.forEach(link => {
        link.addEventListener('click', function(e) {
          e.preventDefault();
          
          // 設定滾動標記
          isScrolling = true;
          
          // 移除所有 active 類別
          navLinks.forEach(nav => nav.classList.remove('active'));
          
          // 為當前點擊的連結添加 active 類別
          this.classList.add('active');
          
          // 取得目標區段並滾動到該位置
          const targetId = this.getAttribute('href').substring(1);
          const targetSection = document.getElementById(targetId);
          
          if (targetSection) {
            // 計算正確的滾動位置（考慮導覽列高度）
            const offsetTop = targetSection.offsetTop - 70;
            
            window.scrollTo({
              top: offsetTop,
              behavior: 'smooth'
            });
            
            // 滾動完成後重置標記
            setTimeout(() => {
              isScrolling = false;
            }, 1000);
          }
        });
      });
      
      // 滾動時檢查哪個區段在視窗中
      function checkActiveSection() {
        // 如果正在程式化滾動，則不更新 active 狀態
        if (isScrolling) return;
        
        const scrollPos = window.scrollY + 120; // 考慮導覽列高度
        let currentSection = '';
        
        sections.forEach(section => {
          const sectionTop = section.offsetTop;
          const sectionHeight = section.offsetHeight;
          const sectionId = section.getAttribute('id');
          
          if (scrollPos >= sectionTop && scrollPos < sectionTop + sectionHeight) {
            currentSection = sectionId;
          }
        });
        
        // 更新導覽列 active 狀態
        if (currentSection) {
          navLinks.forEach(nav => nav.classList.remove('active'));
          const activeLink = document.querySelector(`.nav-link[href="#${currentSection}"]`);
          if (activeLink) {
            activeLink.classList.add('active');
          }
        }
      }
      
      // 使用節流函數來減少滾動事件的觸發頻率
      let scrollTimeout;
      window.addEventListener('scroll', function() {
        if (scrollTimeout) {
          clearTimeout(scrollTimeout);
        }
        scrollTimeout = setTimeout(checkActiveSection, 50);
      });
      
      // 初始檢查
      setTimeout(checkActiveSection, 100);
    });
  </script>
</body>

</html>
