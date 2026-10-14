---
layout: default
title: "关于我"
---

<!-- 1. 🌟 TOP BAR 顶部横带区（锁定在天花板绝不移动） -->
<div class="custom-top-bar">
  <div class="top-bar-left-branding">
    <a class="top-brand-name-link" href="/chunfeng/">椿枫漫笔</a>
    <span class="top-brand-subtitle">Let's not remember years, remember moments</span>
  </div>
  <div class="top-bar-right-menu">
    <a class="top-menu-item" href="/chunfeng/">主页</a>
    <a class="top-menu-item active-nav" href="/chunfeng/about">关于我</a>
  </div>
</div>

<!-- 2. 📰 MAGAZINE SINGLE COLUMN CANVAS（拿掉左栏负重，正文完美独立居中） -->
<div class="magazine-layout-wrapper">

  <!-- 📄 中央主舞台 -->
  <div class="right-articles-flow-panel">
    <div class="content-panel-card" style="display: block !important;">
      <h1 class="article-inside-title">✨ 关于我 </h1>
      
      <div class="article-inside-meta">
        <span>📅 空间修筑时间：{{ "now" | date: "%Y-%m-%d" }}</span>
        <span class="meta-split">|</span>
        <span>✍️ 馆长：Elaine</span>
      </div>

      <!-- ✒️ 请在这里自由挥洒你的“关于我”真实正文 ✒️ -->
      <div class="article-inside-body">
        <p>欢迎来到我的博客!</p>
        
        <p>我家后院的香椿树和枫树，见证了我的很多美好时光，还有我的这些读书摘录，故事，短文，游记等等。</p>
        
        <p>感谢在此驻足！随意挑选一本我的生活游记或故事随笔。愿我的文字能在这个嘈杂的网络世界里，为你送去一丝松弛与安宁。</p>
      </div>
      
    </div>
  </div>

</div>

<!-- 3. 🎨 纯手工完全自定义全屏视觉控制皮肤（让关于我内页与主页1:1完全严丝合缝、血统一致！ 🌟） -->
<style>
  html, body, .wrapper, #main_content_wrap, section.main-content, .container, main, .markdown-body {
    max-width: 100% !important; 
    width: 100% !important; 
    padding: 0 !important; 
    margin: 0 !important;
    position: relative !important;
  }
  header, .site-header, footer, .site-footer, .theme-by, #downloads { display: none !important; height: 0 !important; padding: 0 !important; margin: 0 !important; }
  
  body { 
    background-color: #ffffff; 
    padding: 0 40px !important; 
    box-sizing: border-box !important; 
  }

  /* 🔒 TOP BAR 顶栏：绝对死锁吸顶在天花板上，1:1 克隆主页大招牌格式 */
  .custom-top-bar { 
    position: fixed !important;
    top: 0 !important;
    left: 0 !important;
    width: 100% !important;
    height: 85px !important; 
    background-color: #ffffff !important; 
    display: flex !important; 
    justify-content: space-between !important; 
    align-items: center !important; 
    padding: 0 40px !important; 
    border-bottom: 2px solid #e8dfcf; 
    z-index: 99999 !important; 
    box-sizing: border-box !important;
  }
  
  /* 🌟 华丽复活：让关于我页面的大招牌字号、国风宋体字链全部和主页对齐！ */
  .top-brand-name-link { font-size: 2.2em !important; font-weight: bold !important; color: #2c3e50 !important; letter-spacing: 1px !important; text-decoration: none !important; transition: color 0.2s ease; display: inline-block; font-family: "STSong", "Songti SC", "SimSun", serif !important; }
  .top-brand-name-link:hover { color: #e67e22 !important; }
  .top-brand-subtitle { font-size: 0.95em; color: #7f8c8d; font-style: italic; margin-left: 15px; font-family: "STSong", "Songti SC", "SimSun", serif !important; }
  
  .top-bar-right-menu { display: flex; gap: 25px; }
  .top-menu-item { font-size: 1.1em; font-weight: bold; color: #34495e !important; text-decoration: none !important; }
  .top-menu-item:hover, .active-nav { color: #e67e22 !important; }

  /* 🛡️ 单栏无损平铺布局底座：精确向下留空 115 像素，完美防止被吸顶菜单遮挡 */
  .magazine-layout-wrapper { 
    display: block !important;
    margin-top: 115px !important; 
    margin-bottom: 40px !important; 
    width: 100% !important;
    box-sizing: border-box !important; 
  }

  /* 📄 限制正文阅读的最大黄金宽度，防止全屏平铺太宽导致眼睛看酸 */
  .right-articles-flow-panel { 
    width: 100% !important;
    max-width: 800px !important; 
    margin: 0 auto !important;
    word-break: break-word !important; 
    overflow-wrap: break-word !important;
  }

  /* 📖 正文内页深度深度优化排版 */
  .article-reading-room { background-color: #ffffff; width: 100%; }
  .article-inside-title { font-size: 2.3em; color: #2c3e50; font-weight: bold; line-height: 1.35; margin-top: 0; margin-bottom: 15px; letter-spacing: 0.5px; }
  .article-inside-meta { font-size: 0.9em; color: #7f8c8d; margin-bottom: 35px; padding-bottom: 15px; border-bottom: 1px solid #f2ede4; display: flex; align-items: center; gap: 12px; }
  .meta-split { color: #e8dfcf; }

  /* 砚细腻墨香字芯：强制拉开 1.6em 黄金书籍大留白 ✨ */
  .article-inside-body { font-size: 1.16em; color: #2c3e50; line-height: 1.95; letter-spacing: 0.5px; text-align: justify; }
  .article-inside-body p { margin-top: 0 !important; margin-bottom: 1.6em !important; }
</style>
