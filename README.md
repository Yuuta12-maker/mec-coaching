<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>マインドエンジニアリング・コーチング | 努力せずに変わる新しいアプローチ</title>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
  <style>
    :root {
      --primary: #c50502;
      --primary-dark: #9e0000;
      --primary-light: #ff4c4a;
      --secondary: #333333;
      --light: #ffffff;
      --gray-light: #f8f9fa;
      --gray: #e9ecef;
      --gray-dark: #6c757d;
    }
    
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    body {
      font-family: 'Noto Sans JP', sans-serif;
      color: var(--secondary);
      line-height: 1.6;
    }
    
    h1, h2, h3, h4, h5, h6 {
      font-weight: 700;
      line-height: 1.2;
    }
    
    a {
      text-decoration: none;
      color: inherit;
    }
    
    .container {
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }
    
    .btn {
      display: inline-block;
      padding: 12px 30px;
      border-radius: 50px;
      font-weight: 700;
      text-align: center;
      transition: all 0.3s ease;
      cursor: pointer;
    }
    
    .btn-primary {
      background-color: var(--primary);
      color: var(--light);
      box-shadow: 0 4px 10px rgba(197, 5, 2, 0.3);
    }
    
    .btn-primary:hover {
      background-color: var(--primary-dark);
      transform: translateY(-2px);
      box-shadow: 0 6px 15px rgba(197, 5, 2, 0.4);
    }
    
    .btn-lg {
      padding: 15px 40px;
      font-size: 18px;
    }
    
    .text-center {
      text-align: center;
    }
    
    .section {
      padding: 80px 0;
    }
    
    .section-title {
      margin-bottom: 50px;
      font-size: 36px;
      position: relative;
      padding-bottom: 15px;
    }
    
    .section-title:after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 80px;
      height: 3px;
      background-color: var(--primary);
    }
    
    .section-title.text-center:after {
      left: 50%;
      transform: translateX(-50%);
    }
    
    /* Header Styles */
    .header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      background-color: transparent;
      padding: 20px 0;
      transition: all 0.3s ease;
    }
    
    .header.scrolled {
      background-color: rgba(255, 255, 255, 0.95);
      box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
      padding: 10px 0;
    }
    
    .header-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    
    .logo {
      display: flex;
      align-items: center;
    }
    
    .logo img {
      height: 50px;
    }
    
    .nav-links {
      display: flex;
      gap: 30px;
    }
    
    .nav-link {
      font-weight: 500;
      position: relative;
    }
    
    .nav-link:after {
      content: '';
      position: absolute;
      bottom: -5px;
      left: 0;
      width: 0;
      height: 2px;
      background-color: var(--primary);
      transition: width 0.3s ease;
    }
    
    .nav-link:hover:after {
      width: 100%;
    }
    
    .mobile-menu-btn {
      display: none;
      font-size: 24px;
      cursor: pointer;
    }
    
    /* Hero Section Styles */
    .hero {
      position: relative;
      height: 100vh;
      min-height: 700px;
      background-color: #000;
      color: var(--light);
      overflow: hidden;
      display: flex;
      align-items: center;
    }
    
    .hero:before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: radial-gradient(circle at 30% 50%, rgba(197, 5, 2, 0.4) 0%, rgba(0, 0, 0, 0.8) 80%);
      z-index: 1;
    }
    
    .hero-background {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: url('images/hero-bg.jpg');
      background-size: cover;
      background-position: center;
      opacity: 0.5;
    }
    
    .hero-content {
      position: relative;
      z-index: 2;
      width: 100%;
      max-width: 800px;
    }
    
    .hero-title {
      font-size: 48px;
      margin-bottom: 20px;
      line-height: 1.1;
    }
    
    .hero-subtitle {
      font-size: 20px;
      margin-bottom: 40px;
      font-weight: 400;
      max-width: 600px;
    }
    
    .hero-cta {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
    }
    
    .scroll-down {
      position: absolute;
      bottom: 30px;
      left: 50%;
      transform: translateX(-50%);
      z-index: 2;
      animation: bounce 2s infinite;
      color: var(--light);
      font-size: 12px;
      text-align: center;
    }
    
    .scroll-down i {
      display: block;
      font-size: 24px;
      margin-top: 8px;
    }
    
    @keyframes bounce {
      0%, 20%, 50%, 80%, 100% {
        transform: translateY(0) translateX(-50%);
      }
      40% {
        transform: translateY(-20px) translateX(-50%);
      }
      60% {
        transform: translateY(-10px) translateX(-50%);
      }
    }
    
    /* Problem Section Styles */
    .problem {
      background-color: var(--gray-light);
    }
    
    .problem-list {
      max-width: 700px;
      margin: 0 auto;
    }
    
    .problem-item {
      display: flex;
      align-items: baseline;
      gap: 15px;
      margin-bottom: 20px;
    }
    
    .problem-icon {
      color: var(--primary);
      font-size: 18px;
      flex-shrink: 0;
    }
    
    .problem-text {
      font-size: 18px;
    }
    
    .problem-conclusion {
      text-align: center;
      font-size: 20px;
      font-weight: 700;
      margin-top: 40px;
      padding: 20px;
      background-color: var(--light);
      border-radius: 8px;
      box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
    }
    
    /* Solution Section Styles */
    .solution-content {
      display: flex;
      flex-wrap: wrap;
      gap: 50px;
      align-items: center;
    }
    
    .solution-image {
      flex: 1;
      min-width: 300px;
    }
    
    .solution-image img {
      width: 100%;
      border-radius: 8px;
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
    }
    
    .solution-text {
      flex: 1;
      min-width: 300px;
    }
    
    .solution-text p {
      margin-bottom: 20px;
      font-size: 18px;
    }
    
    .solution-highlight {
      font-weight: 700;
      color: var(--primary);
    }
    
    /* Concept Section Styles */
    .concept {
      background-color: var(--gray-light);
    }
    
    .concept-cards {
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
      justify-content: center;
    }
    
    .concept-card {
      background-color: var(--light);
      border-radius: 8px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
      padding: 30px;
      width: 100%;
      max-width: 350px;
      transition: all 0.3s ease;
    }
    
    .concept-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
    }
    
    .concept-icon {
      font-size: 40px;
      color: var(--primary);
      margin-bottom: 20px;
    }
    
    .concept-title {
      font-size: 22px;
      margin-bottom: 15px;
      position: relative;
      padding-bottom: 10px;
    }
    
    .concept-title:after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 40px;
      height: 2px;
      background-color: var(--primary);
    }
    
    .concept-description {
      font-size: 16px;
    }
    
    /* Benefits Section Styles */
    .benefits-list {
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
      justify-content: center;
    }
    
    .benefit-item {
      width: 100%;
      max-width: 350px;
      display: flex;
      align-items: flex-start;
      gap: 15px;
    }
    
    .benefit-icon {
      width: 50px;
      height: 50px;
      background-color: rgba(197, 5, 2, 0.1);
      color: var(--primary);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 20px;
      flex-shrink: 0;
    }
    
    .benefit-text h3 {
      font-size: 18px;
      margin-bottom: 8px;
    }
    
    /* Program Section Styles */
    .program {
      background-color: var(--gray-light);
    }
    
    .timeline {
      position: relative;
      max-width: 800px;
      margin: 0 auto;
    }
    
    .timeline:before {
      content: '';
      position: absolute;
      top: 0;
      left: 50%;
      transform: translateX(-50%);
      width: 2px;
      height: 100%;
      background-color: var(--primary);
    }
    
    .timeline-item {
      position: relative;
      margin-bottom: 50px;
      width: calc(50% - 30px);
    }
    
    .timeline-item:nth-child(odd) {
      left: 0;
    }
    
    .timeline-item:nth-child(even) {
      left: calc(50% + 30px);
    }
    
    .timeline-item:before {
      content: '';
      position: absolute;
      top: 20px;
      width: 30px;
      height: 2px;
      background-color: var(--primary);
    }
    
    .timeline-item:nth-child(odd):before {
      right: -30px;
    }
    
    .timeline-item:nth-child(even):before {
      left: -30px;
    }
    
    .timeline-item:after {
      content: '';
      position: absolute;
      top: 16px;
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background-color: var(--primary);
    }
    
    .timeline-item:nth-child(odd):after {
      right: -35px;
    }
    
    .timeline-item:nth-child(even):after {
      left: -35px;
    }
    
    .timeline-content {
      background-color: var(--light);
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
    }
    
    .timeline-title {
      font-size: 20px;
      margin-bottom: 10px;
      color: var(--primary);
    }
    
    .pricing {
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
      justify-content: center;
      margin-top: 50px;
    }
    
    .pricing-card {
      background-color: var(--light);
      border-radius: 8px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
      padding: 30px;
      width: 100%;
      max-width: 350px;
      transition: all 0.3s ease;
    }
    
    .pricing-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
    }
    
    .pricing-title {
      font-size: 24px;
      text-align: center;
      margin-bottom: 15px;
    }
    
    .pricing-price {
      font-size: 36px;
      text-align: center;
      color: var(--primary);
      margin-bottom: 20px;
    }
    
    .pricing-description {
      margin-bottom: 20px;
      padding-bottom: 20px;
      border-bottom: 1px solid var(--gray);
    }
    
    .pricing-features {
      list-style: none;
      margin-bottom: 30px;
    }
    
    .pricing-feature {
      margin-bottom: 10px;
      display: flex;
      align-items: baseline;
      gap: 10px;
    }
    
    .pricing-feature i {
      color: var(--primary);
    }
    
    .pricing-cta {
      text-align: center;
    }
    
    /* Coach Section Styles */
    .coach-profile {
      display: flex;
      flex-wrap: wrap;
      gap: 50px;
      align-items: center;
    }
    
    .coach-image {
      flex: 1;
      min-width: 300px;
    }
    
    .coach-image img {
      width: 100%;
      border-radius: 8px;
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
    }
    
    .coach-info {
      flex: 1;
      min-width: 300px;
    }
    
    .coach-name {
      font-size: 28px;
      margin-bottom: 10px;
    }
    
    .coach-title {
      font-size: 18px;
      color: var(--primary);
      margin-bottom: 20px;
    }
    
    .coach-bio {
      margin-bottom: 20px;
    }
    
    .coach-credentials {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
      margin-top: 20px;
    }
    
    .credential {
      background-color: var(--gray-light);
      padding: 8px 15px;
      border-radius: 50px;
      font-size: 14px;
      display: flex;
      align-items: center;
      gap: 8px;
    }
    
    .credential i {
      color: var(--primary);
    }
    
    /* FAQ Section Styles */
    .faq {
      background-color: var(--gray-light);
    }
    
    .faq-list {
      max-width: 800px;
      margin: 0 auto;
    }
    
    .faq-item {
      background-color: var(--light);
      border-radius: 8px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
      margin-bottom: 20px;
      overflow: hidden;
    }
    
    .faq-question {
      padding: 20px;
      cursor: pointer;
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-weight: 700;
      font-size: 18px;
    }
    
    .faq-question i {
      transition: transform 0.3s ease;
    }
    
    .faq-item.active .faq-question i {
      transform: rotate(180deg);
    }
    
    .faq-answer {
      padding: 0 20px;
      max-height: 0;
      overflow: hidden;
      transition: max-height 0.3s ease, padding 0.3s ease;
    }
    
    .faq-item.active .faq-answer {
      padding: 0 20px 20px;
      max-height: 500px;
    }
    
    /* CTA Section Styles */
    .cta {
      background-color: #000;
      color: var(--light);
      position: relative;
      overflow: hidden;
    }
    
    .cta:before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: radial-gradient(circle at 70% 50%, rgba(197, 5, 2, 0.6) 0%, rgba(0, 0, 0, 0.8) 70%);
      z-index: 1;
    }
    
    .cta-content {
      position: relative;
      z-index: 2;
      text-align: center;
      max-width: 700px;
      margin: 0 auto;
    }
    
    .cta-title {
      font-size: 36px;
      margin-bottom: 20px;
    }
    
    .cta-text {
      font-size: 18px;
      margin-bottom: 30px;
    }
    
    .limited-offer {
      display: inline-block;
      background-color: rgba(255, 255, 255, 0.1);
      border: 2px solid var(--primary);
      padding: 10px 20px;
      border-radius: 50px;
      font-weight: 700;
      margin-bottom: 30px;
    }
    
    /* Contact Section Styles */
    .contact-info {
      text-align: center;
      max-width: 700px;
      margin: 0 auto;
    }
    
    .contact-item {
      margin-bottom: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
    }
    
    .contact-item i {
      color: var(--primary);
    }
    
    /* Footer Styles */
    .footer {
      background-color: #1a1a1a;
      color: var(--light);
      padding: 50px 0 20px;
    }
    
    .footer-content {
      display: flex;
      flex-wrap: wrap;
      gap: 50px;
      margin-bottom: 30px;
    }
    
    .footer-logo {
      flex: 1;
      min-width: 250px;
    }
    
    .footer-logo img {
      height: 40px;
      margin-bottom: 15px;
    }
    
    .footer-links {
      flex: 1;
      min-width: 250px;
    }
    
    .footer-title {
      font-size: 18px;
      margin-bottom: 20px;
      position: relative;
      padding-bottom: 10px;
    }
    
    .footer-title:after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 30px;
      height: 2px;
      background-color: var(--primary);
    }
    
    .footer-nav {
      list-style: none;
    }
    
    .footer-nav li {
      margin-bottom: 10px;
    }
    
    .footer-nav a {
      display: block;
      transition: color 0.3s ease;
    }
    
    .footer-nav a:hover {
      color: var(--primary);
    }
    
    .footer-social {
      display: flex;
      gap: 15px;
      margin-top: 20px;
    }
    
    .social-icon {
      width: 40px;
      height: 40px;
      background-color: rgba(255, 255, 255, 0.1);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: all 0.3s ease;
    }
    
    .social-icon:hover {
      background-color: var(--primary);
      transform: translateY(-3px);
    }
    
    .footer-bottom {
      text-align: center;
      padding-top: 20px;
      border-top: 1px solid rgba(255, 255, 255, 0.1);
      font-size: 14px;
      color: var(--gray-dark);
    }
    
    /* Floating CTA Button (Mobile) */
    .floating-cta {
      position: fixed;
      bottom: 20px;
      right: 20px;
      z-index: 999;
      display: none;
    }
    
    /* Responsive Styles */
    @media (max-width: 992px) {
      .section {
        padding: 60px 0;
      }
      
      .section-title {
        font-size: 30px;
      }
      
      .hero-title {
        font-size: 36px;
      }
      
      .hero-subtitle {
        font-size: 18px;
      }
      
      .timeline:before {
        left: 20px;
      }
      
      .timeline-item {
        width: calc(100% - 40px);
        left: 40px !important;
      }
      
      .timeline-item:before {
        left: -20px !important;
        width: 20px;
      }
      
      .timeline-item:after {
        left: -25px !important;
      }
    }
    
    @media (max-width: 768px) {
      .header .nav-links {
        display: none;
      }
      
      .mobile-menu-btn {
        display: block;
      }
      
      .hero {
        min-height: 600px;
      }
      
      .hero-title {
        font-size: 32px;
      }
      
      .floating-cta {
        display: block;
      }
    }
    
    @media (max-width: 576px) {
      .hero-title {
        font-size: 28px;
      }
      
      .btn-lg {
        padding: 12px 30px;
        font-size: 16px;
      }
      
      .section-title {
        font-size: 26px;
      }
    }
  </style>
</head>
<body>
  <!-- Header -->
  <header class="header">
    <div class="container">
      <div class="header-inner">
        <div class="logo">
          <img src="images/mec-logo.png" alt="MEC Logo">
        </div>
        <nav class="nav-links">
          <a href="#about" class="nav-link">特徴</a>
          <a href="#concept" class="nav-link">コンセプト</a>
          <a href="#program" class="nav-link">プログラム</a>
          <a href="#coach" class="nav-link">コーチ</a>
          <a href="#faq" class="nav-link">FAQ</a>
          <a href="#contact" class="nav-link btn btn-primary">無料相談</a>
        </nav>
        <div class="mobile-menu-btn">
          <i class="fas fa-bars"></i>
        </div>
      </div>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero">
    <div class="hero-background"></div>
    <div class="container">
      <div class="hero-content">
        <h1 class="hero-title">努力せずに変わる。<br>認知科学が解き放つ、<br>あなたの無限の可能性</h1>
        <p class="hero-subtitle">最新の認知科学とホメオスタシス理論に基づき、マインドの力で自然に理想の自分へ。根性論やツラい努力とはサヨナラ。</p>
        <div class="hero-cta">
          <a href="#contact" class="btn btn-primary btn-lg">無料カウンセリングに申し込む</a>
        </div>
      </div>
    </div>
    <div class="scroll-down">
      詳しく見る
      <i class="fas fa-chevron-down"></i>
    </div>
  </section>

  <!-- Problem Section -->
  <section id="problem" class="section problem">
    <div class="container">
      <h2 class="section-title text-center">なぜあなたの努力は実を結ばないのか？</h2>
      <div class="problem-list">
        <div class="problem-item">
          <div class="problem-icon">
            <i class="fas fa-check-circle"></i>
          </div>
          <div class="problem-text">
            自己啓発本を読んでも一時的なモチベーションだけで終わる
          </div>
        </div>
        <div class="problem-item">
          <div class="problem-icon">
            <i class="fas fa-check-circle"></i>
          </div>
          <div class="problem-text">
            目標設定しても継続できず、いつの間にか元の生活に戻っている
          </div>
        </div>
        <div class="problem-item">
          <div class="problem-icon">
            <i class="fas fa-check-circle"></i>
          </div>
          <div class="problem-text">
            「頑張れ」「根性で乗り切れ」という精神論にうんざりしている
          </div>
        </div>
        <div class="problem-item">
          <div class="problem-icon">
            <i class="fas fa-check-circle"></i>
          </div>
          <div class="problem-text">
            過去の失敗体験が新しい行動の妨げになっている
          </div>
        </div>
        <div class="problem-item">
          <div class="problem-icon">
            <i class="fas fa-check-circle"></i>
          </div>
          <div class="problem-text">
            「なりたい自分」と「現実の自分」のギャップに苦しんでいる
          </div>
        </div>
        <div class="problem-conclusion">
          これらは決してあなたの「意志が弱い」からではありません。<br>
          実は脳の仕組み自体が、あなたを「現状維持」へと導くように設計されているのです。
        </div>
      </div>
    </div>
  </section>

  <!-- Solution Section -->
  <section id="about" class="section solution">
    <div class="container">
      <h2 class="section-title">マインドエンジニアリング・コーチングとは？</h2>
      <div class="solution-content">
        <div class="solution-image">
          <img src="images/concept-diagram.jpg" alt="マインドエンジニアリングの概念図">
        </div>
        <div class="solution-text">
          <p>マインドエンジニアリング・コーチングは、最新の認知科学的知見を基盤とした画期的なアプローチです。</p>
          <p>従来の「現状から頑張って目標に向かう」という方法ではなく、「理想の未来から現在を引き寄せる」という逆転の発想で、脳の自然な働き（ホメオスタシス）を味方につけます。</p>
          <p>このコーチングの真骨頂は、<span class="solution-highlight">「脳の自動操縦システムを再プログラミングする」</span>ことにあります。そして、その方法はシンプルで効果的。理想のゴールを設定し、新しいコンフォートゾーンをマインドの中に創り出すだけです。</p>
          <p>あなたの脳は、設定された新しい「当たり前」へと自然に向かおうとします。これにより、無理な努力や我慢なしに行動が変化するのです。</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Concept Section -->
  <section id="concept" class="section concept">
    <div class="container">
      <h2 class="section-title text-center">3つの革新的コンセプト</h2>
      <div class="concept-cards">
        <div class="concept-card">
          <div class="concept-icon">
            <i class="fas fa-bullseye"></i>
          </div>
          <h3 class="concept-title">ゴール設定の新概念</h3>
          <div class="concept-description">
            <p>マインドエンジニアリング・コーチングにおけるゴール設定は、従来のSMART目標とは一線を画します。</p>
            <ul>
              <li>100%やりたいことに焦点</li>
              <li>現状の外に設定</li>
              <li>達成方法が思いつかなくてもOK</li>
              <li>社会にも貢献する要素を含む</li>
            </ul>
            <p>真のゴールは、想像するだけで少し不安になるくらいの大きさが理想的。そこに向かうエネルギーが自然と湧いてくるのです。</p>
          </div>
        </div>
        <div class="concept-card">
          <div class="concept-icon">
            <i class="fas fa-sync-alt"></i>
          </div>
          <h3 class="concept-title">ホメオスタシスの力を味方に</h3>
          <div class="concept-description">
            <p>ホメオスタシスとは、生体が一定の状態を保とうとする機能です。これは精神世界にも存在します。</p>
            <p>マインドエンジニアリング・コーチングでは、このホメオスタシスの力を逆手にとります。</p>
            <p>新しいゴールの世界をリアルにイメージすることで、脳は「その世界こそが当たり前」と認識するようになります。すると不思議なことに、ホメオスタシスの力によって、あなたは自然にその新しい状態に向かって行動し始めるのです。</p>
          </div>
        </div>
        <div class="concept-card">
          <div class="concept-icon">
            <i class="fas fa-expand-arrows-alt"></i>
          </div>
          <h3 class="concept-title">コンフォートゾーンの再設計</h3>
          <div class="concept-description">
            <p>コンフォートゾーンとは「当然あって然るべき空間」、つまり「当たり前」と感じる環境や状態のことです。</p>
            <p>マインドエンジニアリング・コーチングでは、このコンフォートゾーンを意図的に再設計します。</p>
            <p>ゴールの世界の状態をリアルにイメージすることで、脳はその状態を新しい「当たり前」として認識し始めます。すると、現状とゴールのギャップが生じ、そのギャップを埋めようとするエネルギーが自然と湧き出すのです。</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Benefits Section -->
  <section id="benefits" class="section benefits">
    <div class="container">
      <h2 class="section-title text-center">マインドエンジニアリング・コーチングがもたらす7つの変化</h2>
      <div class="benefits-list">
        <div class="benefit-item">
          <div class="benefit-icon">
            <i class="fas fa-walking"></i>
          </div>
          <div class="benefit-text">
            <h3>自然な行動変容</h3>
            <p>無理な努力や根性論なしに、望ましい行動が自然と身につく</p>
          </div>
        </div>
        <div class="benefit-item">
          <div class="benefit-icon">
            <i class="fas fa-fire"></i>
          </div>
          <div class="benefit-text">
            <h3>内発的モチベーション</h3>
            <p>外部からの刺激に頼らない、持続的な原動力が生まれる</p>
          </div>
        </div>
        <div class="benefit-item">
          <div class="benefit-icon">
            <i class="fas fa-heart"></i>
          </div>
          <div class="benefit-text">
            <h3>ストレスフリーな成長</h3>
            <p>変化のプロセスが苦痛ではなく、むしろ心地よく感じられる</p>
          </div>
        </div>
        <div class="benefit-item">
          <div class="benefit-icon">
            <i class="fas fa-unlock"></i>
          </div>
          <div class="benefit-text">
            <h3>過去の制限からの解放</h3>
            <p>「過去の経験」が現在の選択肢を狭める呪縛から自由になる</p>
          </div>
        </div>
        <div class="benefit-item">
          <div class="benefit-icon">
            <i class="fas fa-lightbulb"></i>
          </div>
          <div class="benefit-text">
            <h3>創造性の向上</h3>
            <p>固定観念から解放され、新しい発想や解決策が自然と浮かぶようになる</p>
          </div>
        </div>
        <div class="benefit-item">
          <div class="benefit-icon">
            <i class="fas fa-users"></i>
          </div>
          <div class="benefit-text">
            <h3>人間関係の質的向上</h3>
            <p>自己理解が深まることで、他者との関わり方が変化する</p>
          </div>
        </div>
        <div class="benefit-item">
          <div class="benefit-icon">
            <i class="fas fa-balance-scale"></i>
          </div>
          <div class="benefit-text">
            <h3>人生の各領域におけるバランス</h3>
            <p>仕事、健康、人間関係など様々な領域で調和のとれた成長を実現</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Program Section -->
  <section id="program" class="section program">
    <div class="container">
      <h2 class="section-title text-center">マインドエンジニアリング・コーチング プログラム内容</h2>
      <div class="timeline">
        <div class="timeline-item">
          <div class="timeline-content">
            <h3 class="timeline-title">第1回：マインドエンジニアリング概論</h3>
            <p>ホメオスタシス理論の理解と現状・コンフォートゾーンの分析を行います。自分自身の潜在的な思考パターンを発見するきっかけとなります。</p>
          </div>
        </div>
        <div class="timeline-item">
          <div class="timeline-content">
            <h3 class="timeline-title">第2回：理想のゴール設定ワーク</h3>
            <p>本当にやりたいことの発掘し、現状の外のゴール設定法を学びます。従来の目標設定とは一線を画す、マインドエンジニアリング独自のアプローチを体験します。</p>
          </div>
        </div>
        <div class="timeline-item">
          <div class="timeline-content">
            <h3 class="timeline-title">第3回：新しいコンフォートゾーンの構築</h3>
            <p>ゴール世界の臨場感イメージングとマインドマップ作成を通じて、脳の中に新しい「当たり前」の状態を構築します。</p>
          </div>
        </div>
        <div class="timeline-item">
          <div class="timeline-content">
            <h3 class="timeline-title">第4・5回：実践と調整</h3>
            <p>行動変容の観察と分析、障害となるスコトーマの解除を行います。日常の中で起こる変化を確認し、必要に応じたアジャストメントを行います。</p>
          </div>
        </div>
        <div class="timeline-item">
          <div class="timeline-content">
            <h3 class="timeline-title">第6回：自走化プラン</h3>
            <p>継続的な成長のための仕組み作りとゴールの発展的アップデートを行います。コーチングが終わった後も、自分自身でさらなる成長を続けるための土台を固めます。</p>
          </div>
        </div>
      </div>
      <div class="pricing">
        <div class="pricing-card">
          <h3 class="pricing-title">個人セッション</h3>
          <div class="pricing-price">300,000円</div>
          <div class="pricing-description">
            1対1の完全パーソナルコーチングで、あなただけの課題に焦点を当てた最も効果的なプログラムです。
          </div>
          <ul class="pricing-features">
            <li class="pricing-feature">
              <i class="fas fa-check"></i>
              <span>1回60分 × 全6回</span>
            </li>
            <li class="pricing-feature">
              <i class="fas fa-check"></i>
              <span>専用ワークブック</span>
            </li>
            <li class="pricing-feature">
              <i class="fas fa-check"></i>
              <span>セッション間のメールサポート</span>
            </li>
            <li class="pricing-feature">
              <i class="fas fa-check"></i>
              <span>コミュニティ参加権</span>
            </li>
          </ul>
          <div class="pricing-cta">
            <a href="#contact" class="btn btn-primary">申し込む</a>
          </div>
        </div>
        <div class="pricing-card">
          <h3 class="pricing-title">グループセッション</h3>
          <div class="pricing-price">150,000円</div>
          <div class="pricing-description">
            少人数グループでのコーチングで、相互作用による気づきと仲間との共有体験を通じて成長します。
          </div>
          <ul class="pricing-features">
            <li class="pricing-feature">
              <i class="fas fa-check"></i>
              <span>1回90分 × 全6回</span>
            </li>
            <li class="pricing-feature">
              <i class="fas fa-check"></i>
              <span>専用ワークブック</span>
            </li>
            <li class="pricing-feature">
              <i class="fas fa-check"></i>
              <span>セッション間のメールサポート</span>
            </li>
            <li class="pricing-feature">
              <i class="fas fa-check"></i>
              <span>コミュニティ参加権</span>
            </li>
            <li class="pricing-feature">
              <i class="fas fa-check"></i>
              <span>定員4名</span>
            </li>
          </ul>
          <div class="pricing-cta">
            <a href="#contact" class="btn btn-primary">申し込む</a>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Coach Section -->
  <section id="coach" class="section coach">
    <div class="container">
      <h2 class="section-title">コーチプロフィール</h2>
      <div class="coach-profile">
        <div class="coach-image">
          <img src="images/coach-profile.jpg" alt="コーチの写真">
        </div>
        <div class="coach-info">
          <h3 class="coach-name">石田 太郎</h3>
          <div class="coach-title">マインドエンジニアリング・コーチング創始者</div>
          <div class="coach-bio">
            <p>認知科学とコーチングの専門家として10年の実績。東京大学卒業後、外資系コンサルティング企業でのキャリアを経て、人間の可能性を最大限に引き出すマインドエンジニアリング・コーチングを開発。</p>
            <p>「努力感なく理想の自分になる」をコンセプトに、これまで200名以上のクライアントの変革をサポートしてきました。認知科学と脳科学の最新研究を取り入れた独自のメソッドは、従来のコーチングとは一線を画す効果を生み出しています。</p>
          </div>
          <div class="coach-credentials">
            <div class="credential">
              <i class="fas fa-certificate"></i>
              <span>日本コーチ連盟認定コーチ</span>
            </div>
            <div class="credential">
              <i class="fas fa-user-graduate"></i>
              <span>認知科学学会会員</span>
            </div>
            <div class="credential">
              <i class="fas fa-book"></i>
              <span>著書「脳が勝手に動き出す法則」</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- FAQ Section -->
  <section id="faq" class="section faq">
    <div class="container">
      <h2 class="section-title text-center">よくある質問</h2>
      <div class="faq-list">
        <div class="faq-item">
          <div class="faq-question">
            従来のコーチングとどう違うのですか？
            <i class="fas fa-chevron-down"></i>
          </div>
          <div class="faq-answer">
            <p>従来のコーチングが「現状から目標に向かう」アプローチを取るのに対し、マインドエンジニアリング・コーチングは「理想の未来から現在を引き寄せる」という逆転の発想を採用しています。また、認知科学的知見に基づく「ホメオスタシス」の力を活用する点が大きな特徴です。</p>
          </div>
        </div>
        <div class="faq-item">
          <div class="faq-question">
            具体的な目標がない状態でも参加できますか？
            <i class="fas fa-chevron-down"></i>
          </div>
          <div class="faq-answer">
            <p>もちろん可能です。むしろ「何が本当にやりたいのかわからない」という方こそ、このコーチングで大きな気づきを得られることが多いです。セッションを通じて、あなた自身が本当に望む「現状の外のゴール」を発見するサポートをします。</p>
          </div>
        </div>
        <div class="faq-item">
          <div class="faq-question">
            オンラインでも受講できますか？
            <i class="fas fa-chevron-down"></i>
          </div>
          <div class="faq-answer">
            <p>はい、すべてのセッションはオンラインでも対面でも受講可能です。オンラインの場合はZoomを使用します。</p>
          </div>
        </div>
        <div class="faq-item">
          <div class="faq-question">
            効果はどのくらいで実感できますか？
            <i class="fas fa-chevron-down"></i>
          </div>
          <div class="faq-answer">
            <p>多くのクライアントは、最初のセッションから「ものの見方」の変化を感じ始めます。具体的な行動変容は個人差がありますが、3回目のセッション頃から「自然と行動が変わってきた」という報告が増えます。</p>
          </div>
        </div>
        <div class="faq-item">
          <div class="faq-question">
            忙しくてワークに時間がとれない場合でも効果はありますか？
            <i class="fas fa-chevron-down"></i>
          </div>
          <div class="faq-answer">
            <p>このコーチングの特徴は「努力感なく変化する」ことにあります。セッション間の課題も最小限に設計され、日常生活の中で自然と実践できるものばかりです。むしろ「忙しくて自己啓発に時間がとれない」という方こそ、このアプローチが合っています。</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- CTA Section -->
  <section id="cta" class="section cta">
    <div class="container">
      <div class="cta-content">
        <h2 class="cta-title">あなたの無限の可能性を解き放つ第一歩を踏み出しませんか？</h2>
        <p class="cta-text">マインドエンジニアリング・コーチングは、「努力」や「根性」に頼らず、認知科学の力で自然に望む自分になるための画期的なプログラムです。</p>
        <p class="cta-text">「本当はこうなりたい」という思いはあるのに、なかなか行動に移せない。そんなもどかしさを感じているなら、まずは無料カウンセリングで、あなたの可能性を探ってみませんか？</p>
        <div class="limited-offer">
          ＼ 先着5名様限定 ／
        </div>
        <a href="#contact" class="btn btn-primary btn-lg">無料カウンセリングに申し込む</a>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="section contact">
    <div class="container">
      <h2 class="section-title text-center">お問い合わせ</h2>
      <div class="contact-info">
        <p>ご質問やご不明点がございましたら、お気軽にお問い合わせください。<br>24時間以内に返信いたします。</p>
        <div class="contact-item">
          <i class="fas fa-envelope"></i>
          <span>info@mind-engineering.com</span>
        </div>
        <div class="contact-item">
          <i class="fas fa-phone"></i>
          <span>03-XXXX-XXXX（平日10:00-18:00）</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-logo">
          <img src="images/mec-logo.png" alt="MEC Logo">
          <p>マインドエンジニアリング・コーチングで、努力感なく理想の自分に。</p>
          <div class="footer-social">
            <a href="#" class="social-icon">
              <i class="fab fa-twitter"></i>
            </a>
            <a href="#" class="social-icon">
              <i class="fab fa-facebook-f"></i>
            </a>
            <a href="#" class="social-icon">
              <i class="fab fa-instagram"></i>
            </a>
            <a href="#" class="social-icon">
              <i class="fab fa-youtube"></i>
            </a>
          </div>
        </div>
        <div class="footer-links">
          <h3 class="footer-title">サイトマップ</h3>
          <ul class="footer-nav">
            <li><a href="#about">特徴</a></li>
            <li><a href="#concept">コンセプト</a></li>
            <li><a href="#benefits">メリット</a></li>
            <li><a href="#program">プログラム</a></li>
            <li><a href="#coach">コーチ</a></li>
            <li><a href="#faq">FAQ</a></li>
            <li><a href="#contact">お問い合わせ</a></li>
          </ul>
        </div>
        <div class="footer-links">
          <h3 class="footer-title">サポート</h3>
          <ul class="footer-nav">
            <li><a href="#">プライバシーポリシー</a></li>
            <li><a href="#">利用規約</a></li>
            <li><a href="#">特定商取引法に基づく表記</a></li>
            <li><a href="#">コーチングポリシー</a></li>
          </ul>
        </div>
      </div>
      <div class="footer-bottom">
        <p>&copy; 2025 マインドエンジニアリング・コーチング. All rights reserved.</p>
      </div>
    </div>
  </footer>

  <!-- Floating CTA Button (Mobile) -->
  <div class="floating-cta">
    <a href="#contact" class="btn btn-primary">無料相談</a>
  </div>

  <script>
    // Header Scroll Effect
    window.addEventListener('scroll', function() {
      const header = document.querySelector('.header');
      if (window.scrollY > 50) {
        header.classList.add('scrolled');
      } else {
        header.classList.remove('scrolled');
      }
    });
    
    // FAQ Accordion
    document.querySelectorAll('.faq-question').forEach(question => {
      question.addEventListener('click', function() {
        this.parentElement.classList.toggle('active');
      });
    });
    
    // Mobile Menu Toggle
    document.querySelector('.mobile-menu-btn').addEventListener('click', function() {
      // Mobile menu implementation can be added here
      alert('モバイルメニューは実装時に追加されます');
    });
    
    // Smooth Scroll for Navigation Links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        
        const targetId = this.getAttribute('href');
        if (targetId === '#') return;
        
        const targetElement = document.querySelector(targetId);
        if (targetElement) {
          window.scrollTo({
            top: targetElement.offsetTop - 80,
            behavior: 'smooth'
          });
        }
      });
    });
  </script>
</body>
</html>
