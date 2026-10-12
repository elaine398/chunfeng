---
layout: default
---

<!-- 1. 🌟 TOP BAR 顶部横带区（左侧大字饱满放大，且一键点击秒回首页！） -->
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

  <!-- 🧭 左边栏：固态310px黄金吸顶悬浮柜（7分类两层折叠小抽屉，带整栏独立滚动条） -->
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
              <a class="sub-article-title-link" href="{{ post.url | relative_url }}">
                ▪ {{ post.title }}
              </a>
            </div>
          {% else %}
            <div class="sub-article-row-block"><span class="sub-empty-text">暂无文章...</span></div>
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
              <a class="sub-article-title-link" href="{{ post.url | relative_url }}">
                ▪ {{ post.title }}
              </a>
            </div>
          {% else %}
            <div class="sub-article-row-block"><span class="sub-empty-text">暂无文章...</span></div>
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
              <a class="sub-article-title-link" href="{{ post.url | relative_url }}">
                ▪ {{ post.title }}
              </a>
            </div>
          {% else %}
            <div class="sub-article-row-block"><span class="sub-empty-text">暂无文章...</span></div>
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
              <a class="sub-article-title-link" href="{{ post.url | relative_url }}">
                ▪ {{ post.title }}
              </a>
            </div>
          {% else %}
            <div class="sub-article-row-block"><span class="sub-empty-text">暂无文章...</span></div>
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
              <a class="sub-article-title-link" href="{{ post.url | relative_url }}">
                ▪ {{ post.title }}
              </a>
            </div>
          {% else %}
            <div class="sub-article-row-block"><span class="sub-empty-text">暂无文章...</span></div>
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
              <a class="sub-article-title-link" href="{{ post.url | relative_url }}">
                ▪ {{ post.title }}
              </a>
            </div>
          {% else %}
            <div class="sub-article-row-block"><span class="sub-empty-text">暂无文章...</span></div>
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
              <a class="sub-article-title-link" href="{{ post.url | relative_url }}">
                ▪ {{ post.title }}
              </a>
            </div>
          {% else %}
            <div class="sub-article-row-block"><span class="sub-empty-text">暂无文章...</span></div>
          {% endfor %}
        </div>
      </details>

    </div>
  </div>

  <!-- 📄 右边中央主舞台：精选最近发表的 5 篇摘要流（带[展开/收起]纽扣 ✨） -->
  <div class="right-articles-flow-panel">
    <div class="content-panel-card default-welcome-stream-room" style="display: block !important;">
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
  </div>

</div>

<!-- 3. 🎨 纯手工完全自定义全屏视觉控制皮肤 (CSS 终极双轴独立滚动防拉扯版) -->
<style>
  html, body, .wrapper, #main_content_wrap, section.main-content, .container, main, .markdown-body {
    max-width: 100% !important;   
    width: 100% !important;
    padding: 0 !important;
    margin: 0 !important;
  }
  header, .site-header { display: none !important; height: 0 !important; padding: 0 !important; margin: 0 !important; }
  
  body { 
    background-color: #e7d7af; 
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    padding: 0 40px !important; 
    box-sizing: border-box !important;
  }

  /* Top Bar 顶栏 */
  .custom-top-bar { display: flex; justify-content: space-between; align-items: center; padding: 25px 0; border-bottom: 2px solid #77404f; margin-bottom: 40px; margin-top: 20px; width: 100% !important; box-sizing: border-box; }
  
  /* 🌟 核心放大：将左上角的“椿枫漫笔”大字狠狠放大至 2.2em，并做成高质感的可点击主页链接 */
  .top-brand-name-link { font-size: 2.2em !important; font-weight: bold !important; color: #893333 !important; letter-spacing: 1px !important; text-decoration: none !important; transition: color 0.2s ease; display: inline-block; }
  .top-brand-name-link:hover { color: #e67e22 !important; }
  
  .top-brand-subtitle { font-size: 0.95em; color: #8e5744; font-style: italic; margin-left: 15px; }
  .top-bar-right-menu { display: flex; gap: 25px; }
  .top-menu-item { font-size: 1.1em; font-weight: bold; color: #893333 !important; text-decoration: none !important; }
  .top-menu-item:hover, .active-nav { color: #16183f !important; }

  .sidebar-menu-title { 
  font-size: 1.05em; 
  font-weight: bold; 
  color: #5c0d12; /* 👈 就是这一句，控制“专栏分类”四个字变酱红 */
  padding-bottom: 10px; 
  margin-bottom: 15px; 
  border-bottom: 2px solid #e8dfcf; 

   /* 🍷 终极降维打击：直接锁死 summary 组件真名，强行让7个题目变成绛红色 */
  .left-sidebar-menu-panel details summary,
  .category-accordion-box summary,
  .accordion-header,
  .header-text {
    color: #8c1623 !important;             /* 👈 完美的绛红色 */
    -webkit-text-fill-color: #8c1623 !important; /* 强行让 Safari 浏览器必须听话换色 */
  }
  }
}

   /* 🔒 【双栏永久死锁并排骨架】：核心钢筋！永远左右并肩，禁止换行塌陷！ */
  .magazine-layout-wrapper { 
    display: flex !important; 
    flex-direction: row !important; 
    flex-wrap: nowrap !important;       
    gap: 45px !important; 
    align-items: flex-start !important; 
    width: 100% !important;
    box-sizing: border-box !important;
  }

  
  /* 🧭 左边栏外壳：全尺寸绝对吸顶悬浮柜 */
  .left-sidebar-menu-panel { 
    flex: 0 0 310px !important; 
    width: 310px !important; 
    min-width: 310px !important;
    background-color: #faf9f6; 
    padding: 20px; 
    border-radius: 12px; 
    border: 1px solid #f2ede4; 
    position: sticky !important; 
    top: 25px !important; 
    max-height: calc(100vh - 90px) !important; 
    overflow-y: auto !important; 
    overflow-x: hidden !important; 
    box-sizing: border-box !important;
  }
  
  /* 🍷 换装：控制左栏最上方小标题“专栏分类”变为古典“绛红色” */
  .sidebar-menu-title { font-size: 1.05em; font-weight: bold; color: #8c1623; padding-bottom: 10px; margin-bottom: 15px; border-bottom: 2px solid #e8dfcf; }
  .sidebar-accordion-group { display: flex; flex-direction: column; gap: 12px; }

  .category-accordion-box { background-color: #ffffff; border: 1px solid #eef0f2; border-radius: 8px; overflow: hidden !important; width: 100% !important; box-sizing: border-box !important; }
  .category-accordion-box[open] { border-color: #8c1623; }
  
  /* 🍷 【真名死锁换色重锤】：强控浏览器将 7 个方块的大题目一律彻底刷成华丽的“绛红色”(#8c1623) */
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

  /* 垂直单行列表小抽屉箱 */
  .accordion-sub-links-list { display: block !important; background-color: #faf9f6; border-top: 1px solid #f9f6f0; padding: 6px 0; max-height: 200px !important; overflow-y: auto !important; }
  .sub-article-row-block { display: block !important; width: 100% !important; }
  .sub-article-title-link { font-size: 0.92em; font-weight: bold; color: #555555 !important; padding: 11px 18px; text-decoration: none !important; display: block !important; line-height: 1.4; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; -webkit-text-fill-color: #555555 !important; }
  .sub-article-title-link:hover { background-color: #fdf6ec; color: #e67e22 !important; -webkit-text-fill-color: #e67e22 !important; }
  
  .left-sidebar-menu-panel::-webkit-scrollbar, .accordion-sub-links-list::-webkit-scrollbar { width: 5px !important; }
  .left-sidebar-menu-panel::-webkit-scrollbar-thumb, .accordion-sub-links-list::-webkit-scrollbar-thumb { background-color: #dcd6cd !important; border-radius: 10px !important; }
  .left-sidebar-menu-panel::-webkit-scrollbar-track, .accordion-sub-links-list::-webkit-scrollbar-track { background-color: transparent !important; }

  /* 右边大厅 */
  .right-articles-flow-panel { flex: 1 !important; min-width: 0 !important; word-break: break-word !important; }
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

  /* 正文排版：段落分明 1.6em 黄金书籍留白 */
  .full-article-body-expanded { font-size: 1.16em; color: #2c3e50; line-height: 1.95; letter-spacing: 0.5px; }
  .full-article-body-expanded p { margin-top: 0 !important; margin-bottom: 1.6em !important; text-align: justify; }
</style>
