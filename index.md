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

<!-- 2. 📰 核心大杂志联动大盒（鼠标划过的终极感应舞台） -->
<div class="magazine-interactive-outer">

  <!-- 🧭 左边栏外壳：7大专栏方块 -->
  <div class="left-sidebar-menu-panel">
    <div class="sidebar-menu-title">📚 专栏分类</div>
    <div class="sidebar-box-grid">
      
      <!-- 每一个方块代表一个感属性的“感应雷达” -->
      <div class="radar-box trigger-stories">
        <a class="sidebar-category-box" href="/chunfeng/tags/#故事">
          <span class="box-text">📖 故事专栏</span>
          <span class="box-count">({{ site.tags["故事"].size | default: 0 }})</span>
        </a>
      </div>

      <div class="radar-box trigger-essays">
        <a class="sidebar-category-box" href="/chunfeng/tags/#短文">
          <span class="box-text">✍️ 短文随笔</span>
          <span class="box-count">({{ site.tags["短文"].size | default: 0 }})</span>
        </a>
      </div>

      <div class="radar-box trigger-travels">
        <a class="sidebar-category-box" href="/chunfeng/tags/#游记">
          <span class="box-text">✈️ 游记日记</span>
          <span class="box-count">({{ site.tags["游记"].size | default: 0 }})</span>
        </a>
      </div>

      <div class="radar-box trigger-diaries">
        <a class="sidebar-category-box" href="/chunfeng/tags/#日志">
          <span class="box-text">📅 生活日志</span>
          <span class="box-count">({{ site.tags["日志"].size | default: 0 }})</span>
        </a>
      </div>

      <div class="radar-box trigger-excerpts">
        <a class="sidebar-category-box" href="/chunfeng/tags/#书摘">
          <span class="box-text">📚 读书书摘</span>
          <span class="box-count">({{ site.tags["书摘"].size | default: 0 }})</span>
        </a>
      </div>

      <div class="radar-box trigger-library">
        <a class="sidebar-category-box" href="/chunfeng/tags/#书斋">
          <span class="box-text">🏡 个人书斋</span>
          <span class="box-count">({{ site.tags["书斋"].size | default: 0 }})</span>
        </a>
      </div>

      <div class="radar-box trigger-cooking">
        <a class="sidebar-category-box" href="/chunfeng/tags/#美食">
          <span class="box-text">🍳 美食私房</span>
          <span class="box-count">({{ site.tags["美食"].size | default: 0 }})</span>
        </a>
      </div>

    </div>
  </div>

  <!-- 📄 右边中央主界面：感应式文章目录大厅（跟随左侧鼠标悬停自动一秒换幕） -->
  <div class="right-articles-flow-panel">
    
    <!-- 目录 1: 故事专栏 (通过 CSS 设定为缺省默认显示 ✨) -->
    <div class="category-display-panel panel-stories">
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
    <div class="category-display-panel panel-essays">
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
    <div class="category-display-panel panel-travels">
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
    <div class="category-display-panel panel-diaries">
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
    <div class="category-display-panel panel-excerpts">
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
    <div class="category-display-panel panel-library">
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
    <div class="category-display-panel panel-cooking">
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

<!-- 3. 🎨 鼠标触碰联动核心样式表 (CSS 感应魔术) -->
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

  /* 双栏布局大壳 */
  .magazine-interactive-outer { display: flex; gap: 50px; align-items: flex-start; }

  /* 左边栏 7 大分类方块 */
  .left-sidebar-menu-panel { flex: 0 0 280px; background-color: #faf9f6; padding: 20px; border-radius: 12px; border: 1px solid #f2ede4; }
  .sidebar-menu-title { font-size: 1.05em; font-weight: bold; color: #2c3e50; padding-bottom: 10px; margin-bottom: 15px; border-bottom: 2px solid #e8dfcf; }
  .sidebar-box-grid { display: flex; flex-direction: column; gap: 10px; }
  
  .sidebar-category-box { display: flex; justify-content: space-between; align-items: center; padding: 12px 15px; background-color: #ffffff; border: 1px solid #eef0f2; border-radius: 8px; text-decoration: none !important; color: #34495e !important; font-weight: bold; transition: all 0.2s ease; cursor: pointer; }
  .box-count { font-size: 0.85em; color: #95a5a6; }

  /* 右边中央主界面 */
  .right-articles-flow-panel { flex: 1; }

  /* 🌌 【悬停感应核心魔术代码】 🌌 */
  
  /* 规矩一：默认状态下，只显示第一个“故事专栏”的目录，其余6个通通完全隐藏！ */
  .category-display-panel { display: none; }
  .panel-stories { display: block; }

  /* 规矩二：当整个大盒子被触碰时，先让默认的故事目录淡出隐藏，腾出舞台位置 */
  .magazine-interactive-outer:hover .category-display-panel { display: none; }

  /* 规矩三：只要鼠标滑入对应的雷达盒子(Hover)，对应大厅就会瞬间百分之百强制亮起！ */
  .trigger-stories:hover ~ .right-articles-flow-panel .panel-stories,
  .magazine-interactive-outer:not(:hover) .panel-stories { display: block !important; }
  
  .magazine-interactive-outer:has(.trigger-stories:hover) .panel-stories { display: block !important; }
  .magazine-interactive-outer:has(.trigger-essays:hover) .panel-essays { display: block !important; }
  .magazine-interactive-outer:has(.trigger-travels:hover) .panel-travels { display: block !important; }
  .magazine-interactive-outer:has(.trigger-diaries:hover) .panel-diaries { display: block !important; }
  .magazine-interactive-outer:has(.trigger-excerpts:hover) .panel-excerpts { display: block !important; }
  .magazine-interactive-outer:has(.trigger-library:hover) .panel-library { display: block !important; }
  .magazine-interactive-outer:has(.trigger-cooking:hover) .panel-cooking { display: block !important; }

