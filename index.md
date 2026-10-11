---
layout: default
---

<!-- 1. 🌟 TOP BAR 顶部横带区 -->
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

  <!-- 🧭 左边栏：7大分类点击锁定方块 -->
  <div class="left-sidebar-menu-panel">
    <div class="sidebar-menu-title">📚 专栏分类</div>
    <div class="sidebar-box-grid">
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

  <!-- 📄 右边中央主界面：动态内容大舞台（点击可在“子目录”与“文章正文”之间一秒完美无缝切换） -->
  <div class="right-articles-flow-panel">
    
    <!-- ==================== PART A: 7 大栏目的子目录分区 ==================== -->
    
    <!-- 目录 1: 故事专栏 (缺省默认显示) -->
    <div class="content-panel-card default-show-room" id="stories">
      <h2 class="flow-header">📖 故事专栏 · 文章目录</h2>
      <div class="articles-list-wrapper">
        {% for post in site.tags["故事"] %}
          <div class="post-row-item">
            <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="post-row-title-link" href="#post-{{ post.id | slugify }}">{{ post.title }}</a>
          </div>
        {% else %}
          <p class="empty-notice">暂无最新故事随笔...</p>
        {% endfor %}
      </div>
    </div>

    <!-- 目录 2: 短文随笔 -->
    <div class="content-panel-card" id="essays">
      <h2 class="flow-header">✍️ 短文随笔 · 文章目录</h2>
      <div class="articles-list-wrapper">
        {% for post in site.tags["短文"] %}
          <div class="post-row-item">
            <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="post-row-title-link" href="#post-{{ post.id | slugify }}">{{ post.title }}</a>
          </div>
        {% else %}
          <p class="empty-notice">暂无最新短文随笔...</p>
        {% endfor %}
      </div>
    </div>

    <!-- 目录 3: 游记日记 -->
    <div class="content-panel-card" id="travels">
      <h2 class="flow-header">✈️ 游记日记 · 文章目录</h2>
      <div class="articles-list-wrapper">
        {% for post in site.tags["游记"] %}
          <div class="post-row-item">
            <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="post-row-title-link" href="#post-{{ post.id | slugify }}">{{ post.title }}</a>
          </div>
        {% else %}
          <p class="empty-notice">暂无最新游记日记...</p>
        {% endfor %}
      </div>
    </div>

    <!-- 目录 4: 生活日志 -->
    <div class="content-panel-card" id="diaries">
      <h2 class="flow-header">📅 生活日志 · 文章目录</h2>
      <div class="articles-list-wrapper">
        {% for post in site.tags["日志"] %}
          <div class="post-row-item">
            <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="post-row-title-link" href="#post-{{ post.id | slugify }}">{{ post.title }}</a>
          </div>
        {% else %}
          <p class="empty-notice">暂无最新生活日志...</p>
        {% endfor %}
      </div>
    </div>

    <!-- 目录 5: 读书书摘 -->
    <div class="content-panel-card" id="excerpts">
      <h2 class="flow-header">📚 读书书摘 · 文章目录</h2>
      <div class="articles-list-wrapper">
        {% for post in site.tags["书摘"] %}
          <div class="post-row-item">
            <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="post-row-title-link" href="#post-{{ post.id | slugify }}">{{ post.title }}</a>
          </div>
        {% else %}
          <p class="empty-notice">暂无最新读书书摘...</p>
        {% endfor %}
      </div>
    </div>

    <!-- 目录 6: 个人书斋 -->
    <div class="content-panel-card" id="library">
      <h2 class="flow-header">🏡 个人书斋 · 文章目录</h2>
      <div class="articles-list-wrapper">
        {% for post in site.tags["书斋"] %}
          <div class="post-row-item">
            <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="post-row-title-link" href="#post-{{ post.id | slugify }}">{{ post.title }}</a>
          </div>
        {% else %}
          <p class="empty-notice">暂无最新书斋藏品...</p>
        {% endfor %}
      </div>
    </div>

    <!-- 目录 7: 美食私房 -->
    <div class="content-panel-card" id="cooking">
      <h2 class="flow-header">🍳 美食私房 · 文章目录</h2>
      <div class="articles-list-wrapper">
        {% for post in site.tags["美食"] %}
          <div class="post-row-item">
            <span class="post-row-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="post-row-title-link" href="#post-{{ post.id | slugify }}">{{ post.title }}</a>
          </div>
        {% else %}
          <p class="empty-notice">暂无最新美食记录...</p>
        {% endfor %}
      </div>
    </div>


    <!-- ==================== PART B: 全量文章正文隐藏展厅（点哪个大门，哪个就无缝绽放） ==================== -->
    {% for post in site.posts %}
      <div class="content-panel-card article-reading-room" id="post-{{ post.id | slugify }}">
        <!-- 文章页头：大标题、日期与所属专栏 -->
        <h1 class="article-inside-title">{{ post.title }}</h1>
        <div class="article-inside-meta">
          <span>📅 发布日期：{{ post.date | date: "%Y-%m-%d" }}</span>
          <span class="article-meta-split">|</span>
          <span>✍️ 作者：{{ post.author | default: "Elaine" }}</span>
          <span class="article-meta-split">|</span>
          <a class="back-to-list-badge" href="#{{ post.tags | first | default: 'stories' }}">返回目录 ↩</a>
        </div>
        
        <!-- 文章正文核心区：注入段落分明、极具呼吸感的舒畅排版皮肤 -->
        <div class="article-inside-body markdown-rendered-content">
          {{ post.content }}
        </div>
      </div>
    {% endfor %}

  </div>

</div>

<!-- 3. 🎨 SOLID CLICK-TO-LOCK STYLESHEET (CSS CORE) -->
<style>
  header { display: none !important; height: 0 !important; padding: 0 !important; margin: 0 !important; }
  body { margin: 0; padding: 0 40px; background-color: #ffffff; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; }

  /* Top Bar Header Layout */
  .custom-top-bar { display: flex; justify-content: space-between; align-items: center; padding: 25px 0; border-bottom: 2px solid #e8dfcf; margin-bottom: 40px; margin-top: 20px; }
  .top-brand-name-link { font-size: 1.9em; font-weight: bold; color: #2c3e50 !important; letter-spacing: 1px; margin-right: 15px; text-decoration: none !important; transition: color 0.2s; }
  .top-brand-name-link:hover { color: #e67e22 !important; }
  .top-brand-subtitle { font-size: 0.95em; color: #7f8c8d; font-style: italic; }
  .top-bar-right-menu { display: flex; gap: 25px; }
  .top-menu-item { font-size: 1.1em; font-weight: bold; color: #34495e !important; text-decoration: none !important; transition: color 0.2s; }
  .top-menu-item:hover, .active-nav { color: #e67e22 !important; }

  /* 双栏杂志大排版外壳 */
  .magazine-layout-wrapper { display: flex; gap: 50px; align-items: flex-start; margin-bottom: 60px; }

  /* 左边栏 7 大分类固定面板 */
  .left-sidebar-menu-panel { flex: 0 0 280px; background-color: #faf9f6; padding: 20px; border-radius: 12px; border: 1px solid #f2ede4; position: sticky; top: 30px; }
  .sidebar-menu-title { font-size: 1.05em; font-weight: bold; color: #2c3e50; padding-bottom: 10px; margin-bottom: 15px; border-bottom: 2px solid #e8dfcf; }
  .sidebar-box-grid { display: flex; flex-direction: column; gap: 10px; }
  .sidebar-category-box { display: flex; justify-content: space-between; align-items: center; padding: 12px 15px; background-color: #ffffff; border: 1px solid #eef0f2; border-radius: 8px; text-decoration: none !important; color: #34495e !important; font-weight: bold; transition: all 0.2s ease; }
  .sidebar-category-box:hover { background-color: #fdfbf7; border-color: #e67e22; color: #e67e22 !important; transform: translateX(3px); }
  .box-count { font-size: 0.85em; color: #95a5a6; }

  /* 右边大舞台核心中央调度器 */
  .right-articles-flow-panel { flex: 1; min-width: 0; }

  /* 🔒 终极动态调度机制：默认让所有的目录卡片和文章正文面板全部隐藏 */
  .content-panel-card { 
    display: none; 
  }

  /* 🔒 默认进门状态：如果没有点击任何锚点，有且仅有第一个“故事专栏目录”亮起 */
  html:not(:has(:target)) .default-show-room { 
    display: block !important; 
  }

  /* 🔒 触碰锚点机制：无论是点击了7大子目录，还是点击了具体的文章正文，对应的卡片一秒精准锁死显现 */
  .content-panel-card:target { 
    display: block !important; 
  }
  
  /* 🔒 动态大驱逐：只要有任意一个锚点被激活（不管是看分类还是看文章），必须强制将默认的故事目录一秒完全熄灭 */
  html:has(:target) .default-show-room {
    display: none !important;
  }

