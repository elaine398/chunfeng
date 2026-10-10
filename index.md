---
layout: default
---

<!-- 1. 🌟 完美的 TOP BAR 顶栏横带区 -->
<div class="custom-top-bar">
  <div class="top-bar-left-branding">
    <span class="top-brand-name">椿枫漫笔</span>
    <span class="top-brand-subtitle">Let's not remember years, remember moments</span>
  </div>
  <div class="top-bar-right-menu">
    <a class="top-menu-item" href="/chunfeng/">主页</a>
    <a class="top-menu-item" href="/chunfeng/about">关于我</a>
  </div>
</div>

<!-- 2. 📰 下方核心双栏大杂志格局 -->
<div class="magazine-layout-wrapper">

  <!-- 🧭 左边栏：紧贴最左侧的 7 大专栏精致方块 -->
  <div class="left-sidebar-menu-panel">
    <div class="sidebar-menu-title">📚 专栏分类</div>
    <div class="sidebar-box-grid">
      {% for category in site.sidebar-categories %}
        <a class="sidebar-category-box" href="/chunfeng/tags/#{{ category.tag }}">
          <span class="box-text">{{ category.name }}</span>
          <span class="box-count">({{ site.tags[category.tag].size | default: 0 }})</span>
        </a>
      {% endfor %}
    </div>
  </div>

  <!-- 📄 右边栏：行云流水、宽敞舒畅的中文历史随笔流 -->
  <div class="right-articles-flow-panel">
    <h2 class="flow-header">📖 我的历史随笔</h2>
    
    <div class="articles-list-wrapper">
      {% for post in site.posts %}
        <div class="post-row-item">
          <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
          <a class="post-row-title-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <span class="post-row-tag">#{{ post.tags | first }}</span>
        </div>
      {% else %}
        <p class="empty-notice">💡 储藏室盘点中，请稍等片刻刷新...</p>
      {% endfor %}
    </div>
  </div>

</div>

<!-- 3. 🎨 纯手工完全自定义全屏视觉控制皮肤 (CSS) -->
<style>
  /* 全局去边距，让全屏自由呼吸 */
  body {
    margin: 0;
    padding: 0 40px;
    background-color: #ffffff;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
  }

  /* 🌟 TOP BAR 顶部横带核心样式：强制单线条高档宣纸风 */
  .custom-top-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 25px 0;
    border-bottom: 2px solid #e8dfcf; /* 素雅的泥金单边底线 */
    margin-bottom: 40px;
  }
  .top-brand-name {
    font-size: 1.8em;
    font-weight: bold;
    color: #2c3e50;
    letter-spacing: 1px;
    margin-right: 15px;
  }
  .top-brand-subtitle {
    font-size: 0.95em;
    color: #7f8c8d;
    font-style: italic;
  }
  .top-bar-right-menu {
    display: flex;
    gap: 25px;
  }
  .top-menu-item {
    font-size: 1.1em;
    font-weight: bold;
    color: #34495e !important;
    text-decoration: none !important;
    transition: color 0.2s;
  }
  .top-menu-item:hover {
    color: #e67e22 !important;
  }

  /* 📰 下方大杂志双栏容器排版 */
  .magazine-layout-wrapper {
    display: flex;
    gap: 50px;
    align-items: flex-start;
  }

  /* 左边栏：7大分类方块完美靠左悬挂 */
  .left-sidebar-menu-panel {
    flex: 0 0 280px; /* 固定280像素高档宽度 */
    background-color: #faf9f6;
    padding: 20px;
    border-radius: 12px;
    border: 1px solid #f2ede4;
  }
  .sidebar-menu-title {
    font-size: 1.05em;
    font-weight: bold;
    color: #2c3e50;
    padding-bottom: 10px;
    margin-bottom: 15px;
    border-bottom: 2px solid #e8dfcf;
  }
  .sidebar-box-grid {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  .sidebar-category-box {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 12px 15px;
    background-color: #ffffff;
    border: 1px solid #eef0f2;
    border-radius: 8px;
    text-decoration: none !important;
    color: #34495e !important;
    font-weight: bold;
    transition: all 0.2s ease;
  }
  .sidebar-category-box:hover {
    background: linear-gradient(135deg, #fdfbf7 0%, #f9f5ec 100%);
    border-color: #e67e22;
    transform: translateX(4px);
    color: #e67e22 !important;
  }
  .box-count {
    font-size: 0.85em;
    color: #95a5a6;
  }

  /* 右边栏：历史随笔流舒畅铺开 */
  .right-articles-flow-panel {
    flex: 1;
  }
  .flow-header {
    font-size: 1.3em;
    font-weight: bold;
    color: #2c3e50;
    margin-top: 0;
    margin-bottom: 20px;
    padding-bottom: 10px;
    border-bottom: 1px solid #f2ede4;
  }
  .articles-list-wrapper {
    display: flex;
    flex-direction: column;
    gap: 15px;
  }
  .post-row-item {
    display: flex;
    align-items: center;
    gap: 12px;
    padding-bottom: 12px;
    border-bottom: 1px dashed #f2ede4;
  }
  .post-row-date {
    color: #7f8c8d;
    font-size: 0.95em;
    white-space: nowrap;
  }
  .post-row-title-link {
    color: #2c3e50 !important;
    text-decoration: none !important;
    font-weight: bold;
    flex-grow: 1;
  }
  .post-row-title-link:hover {
    color: #e67e22 !important;
    text-decoration: underline !important;
  }
  .post-row-tag {
    font-size: 0.85em;
    color: #e67e22;
    background-color: #fdf6ec;
    padding: 2px 8px;
    border-radius: 4px;
  }

  /* 🧼 隐藏原皮肤残留的一切底层英文牛皮癣和多余横线 */
  footer, .theme-by, #downloads, .site-footer {
    display: none !important;
  }
</style>
