---
layout: default
---

<!-- 1. 🌟 完美的极简顶栏横带（大名字与主页菜单完美并排） -->
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

<!-- 2. 📰 下方核心双栏大杂志格局 -->
<div class="magazine-layout-wrapper">

  <!-- 🧭 左边栏：7大专栏精致分类方块 -->
  <div class="left-sidebar-menu-panel">
    <div class="sidebar-menu-title">📚 专栏分类</div>
    <div class="sidebar-box-grid">
      <!-- 每一个方块点击后，都指向中间对应分类的“锚点密码” -->
      <a class="sidebar-category-box btn-stories" href="#stories">
        <span class="box-text">📖 故事专栏</span>
        <span class="box-count">({{ site.tags["故事"].size | default: 0 }})</span>
      </a>
      <a class="sidebar-category-box btn-essays" href="#essays">
        <span class="box-text">✍️ 短文随笔</span>
        <span class="box-count">({{ site.tags["短文"].size | default: 0 }})</span>
      </a>
      <a class="sidebar-category-box btn-travels" href="#travels">
        <span class="box-text">✈️ 游记日记</span>
        <span class="box-count">({{ site.tags["游记"].size | default: 0 }})</span>
      </a>
      <a class="sidebar-category-box btn-diaries" href="#diaries">
        <span class="box-text">📅 生活日志</span>
        <span class="box-count">({{ site.tags["日志"].size | default: 0 }})</span>
      </a>
      <a class="sidebar-category-box btn-excerpts" href="#excerpts">
        <span class="box-text">📚 读书书摘</span>
        <span class="box-count">({{ site.tags["书摘"].size | default: 0 }})</span>
      </a>
      <a class="sidebar-category-box btn-library" href="#library">
        <span class="box-text">🏡 个人书斋</span>
        <span class="box-count">({{ site.tags["书斋"].size | default: 0 }})</span>
      </a>
      <a class="sidebar-category-box btn-cooking" href="#cooking">
        <span class="box-text">🍳 美食私房</span>
        <span class="box-count">({{ site.tags["美食"].size | default: 0 }})</span>
      </a>
    </div>
  </div>

  <!-- 📄 右边中央主界面：动态文章目录展示厅（只呈现左边点中的一栏） -->
  <div class="right-articles-flow-panel">
    
    <!-- 目录 1: 故事专栏 (通过 CSS 设定为缺省默认显示 ✨) -->
    <div class="category-display-panel default-show" id="stories">
      <h2 class="flow-header">📖 故事专栏 · 文章目录</h2>
      <div class="articles-list-wrapper">
        {% for post in site.tags["故事"] %}
          <div class="post-row-item">
            <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="post-row-title-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </div>
        {% else %}
          <p class="empty-notice">暂无最新故事随笔...</p>
        {% endfor %}
      </div>
    </div>

    <!-- 目录 2: 短文随笔 -->
    <div class="category-display-panel" id="essays">
      <h2 class="flow-header">✍️ 短文随笔 · 文章目录</h2>
      <div class="articles-list-wrapper">
        {% for post in site.tags["短文"] %}
          <div class="post-row-item">
            <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="post-row-title-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </div>
        {% else %}
          <p class="empty-notice">暂无最新短文随笔...</p>
        {% endfor %}
      </div>
    </div>

    <!-- 目录 3: 游记日记 -->
    <div class="category-display-panel" id="travels">
      <h2 class="flow-header">✈️ 游记日记 · 文章目录</h2>
      <div class="articles-list-wrapper">
        {% for post in site.tags["游记"] %}
          <div class="post-row-item">
            <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="post-row-title-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </div>
        {% else %}
          <p class="empty-notice">暂无最新游记日记...</p>
        {% endfor %}
      </div>
    </div>

    <!-- 目录 4: 生活日志 -->
    <div class="category-display-panel" id="diaries">
      <h2 class="flow-header">📅 生活日志 · 文章目录</h2>
      <div class="articles-list-wrapper">
        {% for post in site.tags["日志"] %}
          <div class="post-row-item">
            <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="post-row-title-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </div>
        {% else %}
          <p class="empty-notice">暂无最新生活日志...</p>
        {% endfor %}
      </div>
    </div>

    <!-- 目录 5: 读书书摘 -->
    <div class="category-display-panel" id="excerpts">
      <h2 class="flow-header">📚 读书书摘 · 文章目录</h2>
      <div class="articles-list-wrapper">
        {% for post in site.tags["书摘"] %}
          <div class="post-row-item">
            <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="post-row-title-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </div>
        {% else %}
          <p class="empty-notice">暂无最新读书书摘...</p>
        {% endfor %}
      </div>
    </div>

    <!-- 目录 6: 个人书斋 -->
    <div class="category-display-panel" id="library">
      <h2 class="flow-header">🏡 个人书斋 · 文章目录</h2>
      <div class="articles-list-wrapper">
        {% for post in site.tags["书斋"] %}
          <div class="post-row-item">
            <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="post-row-title-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </div>
        {% else %}
          <p class="empty-notice">暂无最新书斋藏品...</p>
        {% endfor %}
      </div>
    </div>

    <!-- 目录 7: 美食私房 -->
    <div class="category-display-panel" id="cooking">
      <h2 class="flow-header">🍳 美食私房 · 文章目录</h2>
      <div class="articles-list-wrapper">
        {% for post in site.tags["美食"] %}
          <div class="post-row-item">
            <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="post-row-title-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </div>
        {% else %}
          <p class="empty-notice">暂无最新美食记录...</p>
        {% endfor %}
      </div>
    </div>

  </div>

</div>

<!-- 3. 🎨 纯手工独家定制：全动态排版核心样式表 (CSS 魔术) -->
<style>
  header { display: none !important; height: 0 !important; padding: 0 !important; margin: 0 !important; }
  body { margin: 0; padding: 0 40px; background-color: #ffffff; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; }

  /* Top Bar 顶栏 */
  .custom-top-bar { display: flex; justify-content: space-between; align-items: center; padding: 25px 0; border-bottom: 2px solid #e8dfcf; margin-bottom: 40px; margin-top: 20px; }
  .top-brand-name-link { font-size: 1.9em; font-weight: bold; color: #2c3e50 !important; letter-spacing: 1px; margin-right: 15px; text-decoration: none !important; }
  .top-brand-name-link:hover { color: #e67e22 !important; }
  .top-brand-subtitle { font-size: 0.95em; color: #7f8c8d; font-style: italic; }
  .top-bar-right-menu { display: flex; gap: 25px; }
  .top-menu-item { font-size: 1.1em; font-weight: bold; color: #34495e !important; text-decoration: none !important; }
  .top-menu-item:hover, .active-nav { color: #e67e22 !important; }

  /* 布局核心 */
  .magazine-layout-wrapper { display: flex; gap: 50px; align-items: flex-start; }

  /* 左边栏 7 大分类方块 */
  .left-sidebar-menu-panel { flex: 0 0 280px; background-color: #faf9f6; padding: 20px; border-radius: 12px; border: 1px solid #f2ede4; }
  .sidebar-menu-title { font-size: 1.05em; font-weight: bold; color: #2c3e50; padding-bottom: 10px; margin-bottom: 15px; border-bottom: 2px solid #e8dfcf; }
  .sidebar-box-grid { display: flex; flex-direction: column; gap: 10px; }
  .sidebar-category-box { display: flex; justify-content: space-between; align-items: center; padding: 12px 15px; background-color: #ffffff; border: 1px solid #eef0f2; border-radius: 8px; text-decoration: none !important; color: #34495e !important; font-weight: bold; transition: all 0.2s ease; }
  .sidebar-category-box:hover { background: linear-gradient(135deg, #fdfbf7 0%, #f9f5ec 100%); border-color: #e67e22; transform: translateX(4px); color: #e67e22 !important; }
  .box-count { font-size: 0.85em; color: #95a5a6; }

  /* 右边文章流核心魔术 🌟 */
  .right-articles-flow-panel { flex: 1; position: relative; }
  
  /* 【大招】核心规矩：默认把 7 个大目录全部隐藏隐藏！一个都不露！ */
  .category-display-panel {
    display: none;
  }
  
  /* 【大招】核心规矩：如果没有点击任何东西（缺省状态），唯独让第1个“故事专栏”完美显示！ */
  .right-articles-flow-panel:not(:has(:target)) .default-show {
    display: block !important;
  }
  
  /* 【大招】核心规矩：只要左边点击了某个方块（触发锚点 target），对应的分类大厅一秒精准亮起，其余自动隐藏！ */
  .category-display-panel:target {
    display: block !important;
  }

  /* 内部排版样式保持高档精美 */
  .flow-header { font-size: 1.3em; font-weight: bold; color: #2c3e50; margin-top: 0; margin-bottom: 20px; padding-bottom: 10px; border-bottom: 1px solid #f2ede4; color: #e67e22; }
  .articles-list-wrapper { display: flex; flex-direction: column; gap: 15px; }
  .post-row-item { display: flex; align-items: center; gap: 12px; padding-bottom: 12px; border-bottom: 1px dashed #f2ede4; }
  .post-row-date { color: #7f8c8d; font-size: 0.95em; white-space: nowrap; }
  .post-row-title-link { color: #2c3e50 !important; text-decoration: none !important; font-weight: bold; flex-grow: 1; }
  .post-row-title-link:hover { color: #e67e22 !important; text-decoration: underline !important; }
  .empty-notice { font-style: italic; color: #7f8c8d; }

  /* 彻底消除任何底层皮癣 */
  footer, .theme-by, #downloads, .site-footer, section.sidebar { display: none !important; }
</style>
