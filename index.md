---
layout: default
---

<!-- 1. 🌟 TOP BAR 顶部横带区（名字与菜单完美并排） -->
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

  <!-- 🧭 左边栏：固雅310px黄金悬浮柜（7分类小方块整齐平铺 ✨） -->
  <div class="left-sidebar-menu-panel">
    <div class="sidebar-menu-title">📚 专栏分类</div>
    <div class="sidebar-box-grid">
      <!-- 直接跳转到我们建好的精美专栏分类大厅，彻底消灭内页乱码 -->
      <a class="sidebar-category-box" href="/chunfeng/tags/#故事">
        <span class="box-text">📖 故事专栏</span>
        <span class="box-count">({{ site.tags["故事"].size | default: 0 }})</span>
      </a>
      <a class="sidebar-category-box" href="/chunfeng/tags/#短文">
        <span class="box-text">✍️ 短文随笔</span>
        <span class="box-count">({{ site.tags["短文"].size | default: 0 }})</span>
      </a>
      <a class="sidebar-category-box" href="/chunfeng/tags/#游记">
        <span class="box-text">✈️ 游记日记</span>
        <span class="box-count">({{ site.tags["游记"].size | default: 0 }})</span>
      </a>
      <a class="sidebar-category-box" href="/chunfeng/tags/#日志">
        <span class="box-text">📅 生活日志</span>
        <span class="box-count">({{ site.tags["日志"].size | default: 0 }})</span>
      </a>
      <a class="sidebar-category-box" href="/chunfeng/tags/#书摘">
        <span class="box-text">📚 读书书摘</span>
        <span class="box-count">({{ site.tags["书摘"].size | default: 0 }})</span>
      </a>
      <a class="sidebar-category-box" href="/chunfeng/tags/#书斋">
        <span class="box-text">🏡 个人书斋</span>
        <span class="box-count">({{ site.tags["书斋"].size | default: 0 }})</span>
      </a>
      <a class="sidebar-category-box" href="/chunfeng/tags/#美食">
        <span class="box-text">🍳 美食私房</span>
        <span class="box-count">({{ site.tags["美食"].size | default: 0 }})</span>
      </a>
    </div>
  </div>

  <!-- 📄 右边栏：行云流水、宽敞舒畅的中文历史随笔长轴流 -->
  <div class="right-articles-flow-panel">
    <h2 class="flow-header">📖 我的历史随笔</h2>
    
    <div class="articles-list-wrapper">
      {% for post in site.posts %}
        <div class="post-row-item">
          <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
          <a class="post-row-title-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
          <span class="post-row-tag">#{{ post.tags | first | default: "随笔" }}</span>
        </div>
      {% else %}
        <p class="empty-notice">💡 储藏室盘点中，请稍等片刻刷新...</p>
      {% endfor %}
    </div>
  </div>

</div>

<!-- 3. 🎨 纯手工完全自定义全屏视觉控制皮肤 (横向并排稳固防线版) -->
<style>
  html, body, .wrapper, #main_content_wrap, section.main-content, .container, main, .markdown-body {
    max-width: 100% !important;   
    width: 100% !important;
    padding: 0 !important;
    margin: 0 !important;
  }
  header, .site-header { display: none !important; height: 0 !important; }
  
  body { 
    background-color: #ffffff; 
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    padding: 0 40px !important; 
    box-sizing: border-box !important;
  }

  /* Top Bar 顶栏 */
  .custom-top-bar { display: flex; justify-content: space-between; align-items: center; padding: 25px 0; border-bottom: 2px solid #e8dfcf; margin-bottom: 40px; margin-top: 20px; }
  .top-brand-name-link { font-size: 1.9em; font-weight: bold; color: #2c3e50 !important; letter-spacing: 1px; text-decoration: none !important; transition: color 0.2s; }
  .top-brand-name-link:hover { color: #e67e22 !important; }
  .top-brand-subtitle { font-size: 0.95em; color: #7f8c8d; font-style: italic; margin-left: 15px; }
  .top-bar-right-menu { display: flex; gap: 25px; }
  .top-menu-item { font-size: 1.1em; font-weight: bold; color: #34495e !important; text-decoration: none !important; }
  .top-menu-item:hover, .active-nav { color: #e67e22 !important; }

  /* 🔒 【双栏永久死锁并排】：无论文章拉得多长，绝对横向并肩而坐，一万年也禁止换行塌陷！ */
  .magazine-layout-wrapper { 
    display: flex !important; 
    flex-direction: row !important; 
    flex-wrap: nowrap !important;       
    gap: 45px !important; 
    align-items: flex-start !important; 
    width: 100% !important;
    box-sizing: border-box !important;
  }

  /* 🧭 左边栏：310px黄金身材，再也不会受任何影响 */
  .left-sidebar-menu-panel { 
    flex: 0 0 310px !important; width: 310px !important; min-width: 310px !important;
    background-color: #faf9f6; padding: 20px; border-radius: 12px; border: 1px solid #f2ede4; 
    position: sticky !important; top: 25px !important; box-sizing: border-box !important;
  }
  .sidebar-menu-title { font-size: 1.05em; font-weight: bold; color: #2c3e50; padding-bottom: 10px; margin-bottom: 15px; border-bottom: 2px solid #e8dfcf; }
  
  .sidebar-box-grid { display: flex; flex-direction: column; gap: 10px; }
  .sidebar-category-box { display: flex; justify-content: space-between; align-items: center; padding: 13px 15px; background-color: #ffffff; border: 1px solid #eef0f2; border-radius: 8px; text-decoration: none !important; color: #34495e !important; font-weight: bold; transition: all 0.2s ease; }
  .sidebar-category-box:hover { background-color: #fdf6ec; border-color: #e67e22; color: #e67e22 !important; transform: translateX(4px); }
  .box-count { font-size: 0.85em; color: #95a5a6; }

  /* 右边大厅历史流 */
  .right-articles-flow-panel { flex: 1 !important; min-width: 0 !important; word-break: break-word !important; }
  .flow-header { font-size: 1.3em; font-weight: bold; color: #2c3e50; margin-top: 0; margin-bottom: 20px; padding-bottom: 10px; border-bottom: 1px solid #f2ede4; }
  .articles-list-wrapper { display: flex; flex-direction: column; gap: 15px; }
  .post-row-item { display: flex; align-items: center; gap: 12px; padding-bottom: 12px; border-bottom: 1px dashed #f2ede4; }
  .post-row-date { color: #7f8c8d; font-size: 0.95em; white-space: nowrap; }
  
  .post-row-title-link { color: #2c3e50 !important; text-decoration: none !important; font-weight: bold; flex-grow: 1; }
  .post-row-title-link:hover { color: #e67e22 !important; text-decoration: underline !important; }
  .post-row-tag { font-size: 0.85em; color: #e67e22; background-color: #fdf6ec; padding: 2px 8px; border-radius: 4px; }

  footer, .theme-by, #downloads, .site-footer, section.sidebar { display: none !important; }
</style>
