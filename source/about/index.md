---
title: 关于
date: 2025-08-27 19:30:27
---
---
title: 关于我
layout: page
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
  /* 基础样式 */
  .about-container {
    max-width: 900px;
    margin: 0 auto;
    padding: 20px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: #333;
    line-height: 1.6;
  }
  
  .about-card {
    background: linear-gradient(135deg, #6e45e2 0%, #88d3ce 100%);
    border-radius: 20px;
    padding: 30px;
    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
    margin-bottom: 30px;
    position: relative;
    overflow: hidden;
  }
  
  .about-card::before {
    content: "";
    position: absolute;
    top: -50px;
    right: -50px;
    width: 200px;
    height: 200px;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.1);
    z-index: 0;
  }
  
  .about-card::after {
    content: "";
    position: absolute;
    bottom: -80px;
    left: -80px;
    width: 300px;
    height: 300px;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.1);
    z-index: 0;
  }
  
  .about-header {
    text-align: center;
    margin-bottom: 30px;
    position: relative;
    z-index: 1;
  }
  
  .about-avatar {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    border: 5px solid rgba(255, 255, 255, 0.3);
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
  }
  
  .about-avatar:hover {
    transform: scale(1.05);
  }
  
  .about-header h1 {
    margin: 20px 0 5px;
    color: white;
    font-size: 2.5rem;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
  }
  
  .about-header p {
    color: rgba(255, 255, 255, 0.9);
    font-size: 1.2rem;
    margin: 0;
  }
  
  .about-content {
    background: white;
    border-radius: 15px;
    padding: 30px;
    position: relative;
    z-index: 1;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  }
  
  .about-section {
    margin-bottom: 30px;
  }
  
  .about-section h2 {
    color: #6e45e2;
    border-bottom: 2px solid #f0f0f0;
    padding-bottom: 10px;
    margin-top: 0;
    display: flex;
    align-items: center;
  }
  
  .about-section h2 i {
    margin-right: 10px;
    background: linear-gradient(135deg, #6e45e2 0%, #88d3ce 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  
  .skills {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 15px;
  }
  
  .skill-tag {
    background: linear-gradient(135deg, #6e45e2 0%, #88d3ce 100%);
    color: white;
    padding: 8px 15px;
    border-radius: 50px;
    font-size: 0.9rem;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s;
  }
  
  .skill-tag:hover {
    transform: translateY(-3px);
  }
  
  .timeline {
    position: relative;
    margin-left: 10px;
    padding-left: 30px;
    border-left: 2px solid #6e45e2;
  }
  
  .timeline-item {
    margin-bottom: 20px;
    position: relative;
  }
  
  .timeline-item::before {
    content: "";
    position: absolute;
    left: -40px;
    top: 5px;
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background: #6e45e2;
  }
  
  .timeline-date {
    font-weight: bold;
    color: #6e45e2;
    margin-bottom: 5px;
  }
  
  .timeline-content h3 {
    margin: 0 0 5px;
    color: #333;
  }
  
  .timeline-content p {
    margin: 0;
    color: #666;
  }
  
  .social-links {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 20px;
  }
  
  .social-link {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: linear-gradient(135deg, #6e45e2 0%, #88d3ce 100%);
    color: white;
    font-size: 1.5rem;
    text-decoration: none;
    transition: transform 0.3s, box-shadow 0.3s;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  
  .social-link:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
  }
  
  .anime-music {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 15px;
  }
  
  .music-item {
    background: #f8f9fa;
    border-left: 4px solid #6e45e2;
    padding: 10px 15px;
    border-radius: 4px;
    flex: 1 0 calc(50% - 10px);
    min-width: 200px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
  }
  
  /* 响应式设计 */
  @media (max-width: 768px) {
    .about-container {
      padding: 15px;
    }
    
    .about-card {
      padding: 20px;
    }
    
    .about-content {
      padding: 20px;
    }
    
    .about-avatar {
      width: 120px;
      height: 120px;
    }
    
    .about-header h1 {
      font-size: 2rem;
    }
    
    .skills {
      justify-content: center;
    }
    
    .music-item {
      flex: 1 0 100%;
    }
  }
  
  /* 动漫风格装饰 */
  .anime-decoration {
    position: absolute;
    z-index: 0;
    opacity: 0.1;
  }
  
  .decoration-1 {
    top: 20px;
    right: 20px;
    font-size: 100px;
    transform: rotate(15deg);
  }
  
  .decoration-2 {
    bottom: 20px;
    left: 20px;
    font-size: 80px;
    transform: rotate(-10deg);
  }
  
  /* 闪烁动画 */
  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.5; }
  }
  
  .blink {
    animation: blink 2s infinite;
    color: #ff6b6b;
  }
</style>

<div class="about-container">
  <div class="about-card">
    <i class="fas fa-code anime-decoration decoration-1"></i>
    <i class="fas fa-headphones anime-decoration decoration-2"></i>
    
    <div class="about-header">
      <img src="https://images.unsplash.com/photo-1633332755192-727a05c4013d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=200&q=80" alt="头像" class="about-avatar">
      <h1>SystemError</h1>
      <p>初中生开发者 & 数码爱好者</p>
    </div>

    <div class="about-content">
      <div class="about-section">
        <h2><i class="fas fa-user"></i> 关于我</h2>
        <p>你好！我是 <span class="blink">SystemError</span>，一名14岁的初中生，热爱编程！虽然年轻，但我已经掌握了多种编程技术，喜欢探索数字世界的奥秘。</p>
        <p>在我的学习旅程中，我特别喜欢开发有趣的小项目，解决技术问题，并且热衷于学习新的编程语言和框架。</p>
      </div>

      <div class="about-section">
        <h2><i class="fas fa-rocket"></i> 技能专长</h2>
        <div class="skills">
          <span class="skill-tag">HTML/CSS</span>
          <span class="skill-tag">Python</span>
          <span class="skill-tag">Flutter</span>
          <span class="skill-tag">Node.js</span>
          <span class="skill-tag">JavaScript</span>
          <span class="skill-tag">Git</span>
          <span class="skill-tag">响应式设计</span>
        </div>
      </div>

      <div class="about-section">
        <h2><i class="fas fa-heart"></i> 兴趣爱好</h2>
        <p>除了编程，我还喜欢：</p>
        <ul>
          <li>听二次元音乐（特别是日本动漫歌曲）</li>
          <li>玩电子游戏</li>
        </ul>
      </div>

      <div class="about-section">
        <h2><i class="fas fa-graduation-cap"></i> 学习经历</h2>
        <div class="timeline">
          <div class="timeline-item">
            <div class="timeline-date">2023 - 至今</div>
            <div class="timeline-content">
              <h3>初中</h3>
            </div>
          </div>
          <div class="timeline-item">
            <div class="timeline-date">2017 - 2023</div>
            <div class="timeline-content">
              <h3>小学</h3>
            </div>
          </div>
        </div>
      </div>

      <div class="about-section">
        <h2><i class="fas fa-envelope"></i> 联系我</h2>
        <p>欢迎联系我交流！</p>
        <p>QQ: <strong>3103232089</strong></p>
        
        <div class="social-links">
          <a href="#" class="social-link"><i class="fab fa-github"></i></a>
          <a href="#" class="social-link"><i class="fab fa-qq"></i></a>
          <a href="#" class="social-link"><i class="fab fa-bilibili"></i></a>
          <a href="#" class="social-link"><i class="fas fa-envelope"></i></a>
        </div>
      </div>
    </div>
  </div>
</div>