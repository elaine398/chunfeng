---
layout: default
---

<!-- 1. 🌟 TOP BAR 顶部横带区（锁定在天花板绝不移动） -->
<div class="custom-top-bar">
  <div class="top-bar-left-branding">
    <a class="top-brand-name-link" href="/chunfeng/">椿枫漫笔</a>
    <span class="top-brand-subtitle">Let's not remember years, remember moments</span>
  </div>
  <div class="top-bar-right-menu">
    <a class="top-menu-item active-nav" href="/chunfeng/">主页</a>
    <a class="top-menu-item" href="/chunfeng/about">关于我</a>
  </div>
</div>

<!-- 2. 📰 CORE SPLIT MAGAZINE INTERFACE -->
<div class="magazine-layout-wrapper">

  <!-- 🧭 左边栏：固态310px黄金吸顶悬浮大书架（带整栏独立滚动条，中文字全绛红） -->
  <div class="left-sidebar-menu-panel">
    <div class="sidebar-menu-title">📚 专栏分类</div>
    <div class="sidebar-accordion-group">
      
      <!-- 【第一层分类 1】: 故事专栏 -->
      <details class="category-accordion-box">
        <summary class="accordion-header">
          <span class="header-text">📖 故事专栏</span>
          <span class="header-right-info">
            <span class="badge-count">{{ site.tags["故事"].size | default: 0 }}</span>
            <span class="arrow-icon">▶</span>
          </span>
        </summary>
        <div class="accordion-sub-links-list">
          {% for post in site.tags["故事"] %}
            <div class="sub-article-row-block">
              <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
                ▪ {{ post.title }}
              </a>
            </div>
          {% endfor %}
        </div>
      </details>

      <!-- 【第一层分类 2】: 短文随笔 -->
      <details class="category-accordion-box">
        <summary class="accordion-header">
          <span class="header-text">✍️ 短文随笔</span>
          <span class="header-right-info">
            <span class="badge-count">{{ site.tags["短文"].size | default: 0 }}</span>
            <span class="arrow-icon">▶</span>
          </span>
        </summary>
        <div class="accordion-sub-links-list">
          {% for post in site.tags["短文"] %}
            <div class="sub-article-row-block">
              <!-- Re-anchored to unlock perfect single-page seamless translation -->
              <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">▪ {{ post.title }}</a>
            </div>
          {% endfor %}
        </div>
      </details>

      <!-- 【第一层分类 3】: 游记日记 -->
      <details class="category-accordion-box">
        <summary class="accordion-header">
          <span class="header-text">✈️ 游记日记</span>
          <span class="header-right-info">
            <span class="badge-count">{{ site.tags["游记"].size | default: 0 }}</span>
            <span class="arrow-icon">▶</span>
          </span>
        </summary>
        <div class="accordion-sub-links-list">
          {% for post in site.tags["游记"] %}
            <div class="sub-article-row-block">
              <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
                ▪ {{ post.title }}
              </a>
            </div>
          {% endfor %}
        </div>
      </details>

      <!-- 【第一层分类 4】: 生活日志 -->
      <details class="category-accordion-box">
        <summary class="accordion-header">
          <span class="header-text">📅 生活日志</span>
          <span class="header-right-info">
            <span class="badge-count">{{ site.tags["日志"].size | default: 0 }}</span>
            <span class="arrow-icon">▶</span>
          </span>
        </summary>
        <div class="accordion-sub-links-list">
          {% for post in site.tags["日志"] %}
            <div class="sub-article-row-block">
              <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
                ▪ {{ post.title }}
              </a>
            </div>
          {% endfor %}
        </div>
      </details>

      <!-- 【第一层分类 5】: 读书书摘 -->
      <details class="category-accordion-box">
        <summary class="accordion-header">
          <span class="header-text">📚 读书书摘</span>
          <span class="header-right-info">
            <span class="badge-count">{{ site.tags["书摘"].size | default: 0 }}</span>
            <span class="arrow-icon">▶</span>
          </span>
        </summary>
        <div class="accordion-sub-links-list">
          {% for post in site.tags["书摘"] %}
            <div class="sub-article-row-block">
              <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
                ▪ {{ post.title }}
              </a>
            </div>
          {% endfor %}
        </div>
      </details>

      <!-- 【第一层分类 6】: 个人书斋 -->
      <details class="category-accordion-box">
        <summary class="accordion-header">
          <span class="header-text">🏡 个人书斋</span>
          <span class="header-right-info">
            <span class="badge-count">{{ site.tags["书斋"].size | default: 0 }}</span>
            <span class="arrow-icon">▶</span>
          </span>
        </summary>
        <div class="accordion-sub-links-list">
          {% for post in site.tags["书斋"] %}
            <div class="sub-article-row-block">
              <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
                ▪ {{ post.title }}
              </a>
            </div>
          {% endfor %}
        </div>
      </details>

      <!-- 【第一层分类 7】: 美食私房 -->
      <details class="category-accordion-box">
        <summary class="accordion-header">
          <span class="header-text">🍳 美食私房</span>
          <span class="header-right-info">
            <span class="badge-count">{{ site.tags["美食"].size | default: 0 }}</span>
            <span class="arrow-icon">▶</span>
          </span>
        </summary>
        <div class="accordion-sub-links-list">
          {% for post in site.tags["美食"] %}
            <div class="sub-article-row-block">
              <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
                ▪ {{ post.title }}
              </a>
            </div>
          {% endfor %}
        </div>
      </details>

    </div>
  </div>

  <!-- 📄 右边中央主舞台：精选最近发表的 5 篇摘要流 -->
  <div class="right-articles-flow-panel">
    
    <!-- 🏡 【空间 A】：5 篇最近发表精选随笔流（带原地展开纽扣） -->
    <div class="content-panel-card default-welcome-stream-room">
      <h2 class="magazine-stream-header">✨ 最近发表 · 精选随笔</h2>
      
      {% for post in site.posts limit:5 %}
        <div class="stream-article-item">
          <h3 class="stream-title">{{ post.title }}</h3>
          <div class="stream-meta">📅 {{ post.date | date: "%Y-%m-%d" }} &nbsp;|&nbsp; 🏷️ {{ post.tags | first }}</div>
          
          <details class="readmore-accordion">
            <summary class="readmore-btn-summary">
              <div class="teaser-text-preview">
                {{ post.content | strip_html | truncate: 140 }}
              </div>
              <div class="readmore-badge-trigger">
                <span class="text-expand">[展开阅读全文 ↓]</span>
                <span class="text-collapse">[收起全文 ↑]</span>
              </div>
            </summary>
            
            <div class="full-article-body-expanded">
              {{ post.content }}
            </div>
          </details>
        </div>
      {% endfor %}
    </div>

       <!-- DISPLAY CONTAINER B: Full Text Hub (Replaces State A upon selection with comment boxes enabled! 🌟) -->
    {% for post in site.posts %}
      <div class="content-panel-card article-reading-room" id="post-{{ post.id | slugify }}">
        <h1 class="article-inside-title">{{ post.title }}</h1>
        <div class="article-inside-meta">
          <span>📅 发布时间：{{ post.date | date: "%Y-%m-%d" }}</span>
          <span class="meta-split">|</span>
          <span>🏷️ 分类：{{ post.tags | first }}</span>
          <span class="meta-split">|</span>
          <a class="back-to-home-badge" href="/chunfeng/">返回最近发表 ↩</a>
        </div>
        
        <!-- The Main Essay Body Text -->
        <div class="article-inside-body">{{ post.content }}</div>

        <!-- 💬 GISCUS AUTOMATED COMMENT BOARD: Seamlessly mounts reader messages right below the essay -->
        <div class="article-comments-divider" style="margin-top: 60px; margin-bottom: 30px; border-top: 1px dashed #e8dfcf;"></div>
        <div class="giscus-comment-wrapper" style="width: 100% !important; margin-top: 20px;">
          <script src="https://giscus.app"
                  data-repo="elaine398/chunfeng"
                  data-repo-id="R_kgDOM765qw"
                  data-category="Announcements"
                  data-category-id="DIC_kwDOM765q84CiwX7"
                  data-mapping="pathname"
                  data-strict="0"
                  data-reactions-enabled="1"
                  data-emit-metadata="0"
                  data-input-position="bottom"
                  data-theme="light"
                  data-lang="zh-CN"
                  crossorigin="anonymous"
                  async>
          </script>
        </div>
      </div>
    {% endfor %}

  </div>

</div>

<!-- 3. 🎨 纯手工完全自定义全屏视觉控制皮肤 (地平线切齐死锁版) -->
<style>
  /* 🔒 彻底粉碎官方底部的任何留白杂质残留，确保平整对齐地平线 */
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

  /* 🔒 TOP BAR 顶栏：绝对死锁吸顶 */
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
  
   .top-brand-name-link { 
    font-size: 2.2em !important;        /* 👈 Adjusted from 2.2em to 2.5em to make it significantly bigger */
    font-weight: bold !important; 
    color: #8c1623 !important;          /* 👈 Changed to #8c1623 to lock in that elegant Crimson/绛红色 */
    letter-spacing: 1px !important; 
    text-decoration: none !important; 
    transition: color 0.2s ease; 
    display: inline-block; 
    font-family: "STSong", "Songti SC", "SimSun", serif !important; 
  }
  .top-brand-name-link:hover { color: #e67e22 !important; }
  .top-brand-subtitle { font-size: 0.95em; color: #7f8c8d; font-style: italic; margin-left: 15px; font-family: "STSong", "Songti SC", "SimSun", serif !important; }
  .top-bar-right-menu { display: flex; gap: 25px; }
  .top-menu-item { font-size: 1.1em; font-weight: bold; color: #34495e !important; text-decoration: none !important; }
  .top-menu-item:hover, .active-nav { color: #e67e22 !important; }

  /* 🛡️ 网格死锁矩阵防线：向下精确留白，底部收尾留空 40 像素确保整齐 */
  .magazine-layout-wrapper { 
    display: flex !important; 
    flex-direction: row !important;
    flex-wrap: nowrap !important;
    gap: 45px !important; 
    align-items: flex-start !important; 
    width: 100% !important; 
    margin-top: 115px !important; 
    margin-bottom: 40px !important; /* 👈 精准地平线：让左右两边在底部留出高档相等的白边切齐 */
    box-sizing: border-box !important; 
  }

  /* 🧭 左边栏外壳：全尺寸绝对吸顶悬浮柜 */
  .left-sidebar-menu-panel { 
    flex: 0 0 310px !important; width: 310px !important; min-width: 310px !important;
    background-color: #faf9f6; 
    padding: 20px; 
    border-radius: 12px; 
    border: 1px solid #f2ede4; 
    position: sticky !important; 
    top: 115px !important; 
    max-height: calc(100vh - 155px) !important; /* 👈 高度微调：确保触底停靠时完美卡死，绝不凸出多余盲区 */
    overflow-y: auto !important; 
    overflow-x: hidden !important; 
    box-sizing: border-box !important; 
  }
  
  .sidebar-menu-title { font-size: 1.05em; font-weight: bold; color: #8c1623; padding-bottom: 10px; margin-bottom: 15px; border-bottom: 2px solid #e8dfcf; }
  .sidebar-accordion-group { display: flex; flex-direction: column; gap: 12px; }
  .category-accordion-box { background-color: #ffffff; border: 1px solid #eef0f2; border-radius: 8px; overflow: hidden !important; width: 100% !important; }
  .category-accordion-box[open] { border-color: #8c1623; }
  
  /* 🍷 绛红色 7 大方块题目死锁 */
  .left-sidebar-menu-panel summary,
  .accordion-header,
  .header-text { 
    display: flex !important; 
    justify-content: space-between !important; 
    align-items: center !important; 
    padding: 14px 15px !important; 
    font-weight: bold !important; 
    color: #8c1623 !important;                     
    -webkit-text-fill-color: #8c1623 !important;   
    cursor: pointer; 
    white-space: nowrap !important; 
  }
  .accordion-header:hover { background-color: #fdfbf7; color: #e67e22 !important; -webkit-text-fill-color: #e67e22 !important; }
  .accordion-header::-webkit-details-marker { display: none; }
  
  .header-right-info { display: flex; align-items: center; gap: 8px; }
  .badge-count { font-size: 0.8em; color: #95a5a6; background-color: #f4f6f7; padding: 1px 6px; border-radius: 10px; -webkit-text-fill-color: #95a5a6 !important; }
  .arrow-icon { font-size: 0.7em; color: #bdc3c7; transition: transform 0.25s ease; display: inline-block; -webkit-text-fill-color: #bdc3c7 !important; }
  .category-accordion-box[open] .arrow-icon { transform: rotate(90deg); color: #8c1623; -webkit-text-fill-color: #8c1623 !important; }

  /* 垂直小抽屉箱 */
  .accordion-sub-links-list { display: block !important; background-color: #faf9f6; border-top: 1px solid #f9f6f0; padding: 6px 0; max-height: 200px !important; overflow-y: auto !important; }
  .sub-article-row-block { display: block !important; width: 100% !important; }
  .sub-article-title-link { font-size: 0.92em; font-weight: bold; color: #555555 !important; padding: 11px 18px; text-decoration: none !important; display: block !important; line-height: 1.4; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; -webkit-text-fill-color: #555555 !important; }
  .sub-article-title-link:hover { background-color: #fdf6ec; color: #e67e22 !important; -webkit-text-fill-color: #e67e22 !important; }
  
  .left-sidebar-menu-panel::-webkit-scrollbar, .accordion-sub-links-list::-webkit-scrollbar { width: 5px !important; }
  .left-sidebar-menu-panel::-webkit-scrollbar-thumb, .accordion-sub-links-list::-webkit-scrollbar-thumb { background-color: #dcd6cd !important; border-radius: 10px !important; }

  /* 右边大厅量子隔离防护舱 */
  .right-articles-flow-panel { flex: 1 !important; min-width: 0 !important; contain: inline-size !important; word-break: break-word !important; overflow-wrap: break-word !important; }
  .content-panel-card { display: none; }
  
  /* 单页原地内容置换引擎枢纽 */
  html:not(:has(:target)) .default-welcome-stream-room { display: block !important; }
  .content-panel-card:target { display: block !important; animation: fadeInPaper 0.4s ease-out; }
  html:has(:target) .default-welcome-stream-room { display: none !important; }

  /* 正文排版与书籍级大段落留白 */
  .magazine-stream-header { font-size: 1.3em; font-weight: bold; color: #2c3e50; padding-bottom: 12px; border-bottom: 2px solid #e8dfcf; margin-bottom: 30px; margin-top: 0; }
  .stream-article-item { margin-bottom: 35px; padding-bottom: 30px; border-bottom: 1px dashed #e8dfcf; }
  .stream-title { font-size: 1.5em; color: #2c3e50; font-weight: bold; margin-top: 0; margin-bottom: 10px; }
  .stream-meta { font-size: 0.88em; color: #7f8c8d; margin-bottom: 15px; }
  .readmore-accordion { background-color: transparent; }
  .readmore-btn-summary { list-style: none; outline: none; cursor: pointer; }
  .readmore-btn-summary::-webkit-details-marker { display: none; }
  .teaser-text-preview { font-size: 1.12em; color: #555555; line-height: 1.85; text-align: justify; margin-bottom: 12px; }
  .readmore-badge-trigger { display: inline-block; font-size: 0.93em; font-weight: bold; color: #e67e22; background-color: #fdf6ec; padding: 4px 12px; border-radius: 20px; margin-top: 5px; }
  .readmore-accordion .text-collapse { display: none; }
  .readmore-accordion[open] .text-expand { display: none; }
  .readmore-accordion[open] .text-collapse { display: inline; }
  .readmore-accordion[open] .teaser-text-preview { display: none; }

  .article-reading-room { background-color: #ffffff; width: 100%; }
  .article-inside-title { font-size: 2.3em; color: #2c3e50; font-weight: bold; line-height: 1.35; margin-top: 0; margin-bottom: 15px; letter-spacing: 0.5px; }
  .article-inside-meta { font-size: 0.9em; color: #7f8c8d; margin-bottom: 35px; padding-bottom: 15px; border-bottom: 1px solid #f2ede4; display: flex; align-items: center; gap: 12px; }
  .meta-split { color: #e8dfcf; }
  .back-to-home-badge { font-size: 0.9em; font-weight: bold; background-color: #fdf6ec; color: #e67e22 !important; padding: 2px 12px; border-radius: 20px; text-decoration: none !important; }
  .full-article-body-expanded, .article-inside-body { font-size: 1.16em; color: #2c3e50; line-height: 1.95; letter-spacing: 0.5px; }
  .full-article-body-expanded p, .article-inside-body p { margin-top: 0 !important; margin-bottom: 1.6em !important; text-align: justify; }
  @keyframes fadeInPaper { from { opacity: 0; transform: translateY(6px); } to { opacity: 1; transform: translateY(0); } }
</style>
