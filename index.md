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

  <!-- 🧭 左边栏：高级两层递进风琴折叠书架 -->
  <div class="left-sidebar-menu-panel">
    <div class="sidebar-menu-title">📚 专栏画廊</div>
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
        <!-- 【第二层子目录】: 展开隐藏的随笔列表 -->
        <div class="accordion-sub-links-list">
          {% for post in site.tags["故事"] %}
            <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
              ▪ {{ post.title }}
            </a>
          {% else %}
            <span class="sub-empty-text">暂无文章...</span>
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
            <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
              ▪ {{ post.title }}
            </a>
          {% else %}
            <span class="sub-empty-text">暂无文章...</span>
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
            <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
              ▪ {{ post.title }}
            </a>
          {% else %}
            <span class="sub-empty-text">暂无文章...</span>
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
            <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
              ▪ {{ post.title }}
            </a>
          {% else %}
            <span class="sub-empty-text">暂无文章...</span>
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
            <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
              ▪ {{ post.title }}
            </a>
          {% else %}
            <span class="sub-empty-text">暂无文章...</span>
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
            <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
              ▪ {{ post.title }}
            </a>
          {% else %}
            <span class="sub-empty-text">暂无文章...</span>
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
            <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
              ▪ {{ post.title }}
            </a>
          {% else %}
            <span class="sub-empty-text">暂无文章...</span>
          {% endfor %}
        </div>
      </details>

    </div>
  </div>

  <!-- 📄 右边中央主舞台：跟随左侧子目录的点击，无缝绽放段落分明的详细正文 -->
  <div class="right-articles-flow-panel">
    
    <!-- 🏡 缺省默认欢迎室：读者没点任何文章时，中央静静展示的温情大开场 -->
    <div class="content-inside-card default-welcome-room">
      <h1 class="welcome-main-title">欢迎来到“椿枫漫笔”独立书斋</h1>
      <p class="welcome-p">这里是一片完全属于文字的净土。没有多余的喧嚣与广告，有且仅有关于生活感悟、读书摘录、以及东欧与纽约旅行的真实足迹。</p>
      <p class="welcome-p">💡 <strong>阅读指南</strong>：请用鼠标点击左侧的【专栏分类】展开您的私人书架，轻点任意一篇随笔标题，即可在这里直接享受高质感、段落分明的优雅无缝阅读。</p>
      <div class="welcome-decor-line"></div>
    </div>

    <!-- 📖 全量文章详细正文隐藏展厅（点哪个标题，哪个就一秒在右边完美拆开） -->
    {% for post in site.posts %}
      <div class="content-inside-card article-reading-room" id="post-{{ post.id | slugify }}">
        <h1 class="article-inside-title">{{ post.title }}</h1>
        <div class="article-inside-meta">
          <span>📅 发布时间：{{ post.date | date: "%Y-%m-%d" }}</span>
          <span class="meta-split">|</span>
          <span>✍️ 作者：{{ post.author | default: "Elaine" }}</span>
          <span class="meta-split">|</span>
          <span>🏷️ 分类：{{ post.tags | first }}</span>
        </div>
        
        <!-- 文章详细内容区：高档墨黑字、宽敞行距、完美段落分明 -->
        <div class="article-inside-body">
          {{ post.content }}
        </div>
      </div>
    {% endfor %}

  </div>

</div>

<!-- 3. 🎨 纯手工两层风琴折叠大厅控制皮肤 (CSS 终极成型魔术) -->
<style>
  header { display: none !important; height: 0 !important; padding: 0 !important; margin: 0 !important; }
  body { margin: 0; padding: 0 40px; background-color: #ffffff; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; }

  /* Top Bar 顶栏样式 */
  .custom-top-bar { display: flex; justify-content: space-between; align-items: center; padding: 25px 0; border-bottom: 2px solid #e8dfcf; margin-bottom: 40px; margin-top: 20px; }
  .top-brand-name-link { font-size: 1.9em; font-weight: bold; color: #2c3e50 !important; letter-spacing: 1px; margin-right: 15px; text-decoration: none !important; transition: color 0.2s; }
  .top-brand-name-link:hover { color: #e67e22 !important; }
  .top-brand-subtitle { font-size: 0.95em; color: #7f8c8d; font-style: italic; }
  .top-bar-right-menu { display: flex; gap: 25px; }
  .top-menu-item { font-size: 1.1em; font-weight: bold; color: #34495e !important; text-decoration: none !important; }
  .top-menu-item:hover, .active-nav { color: #e67e22 !important; }

  /* 核心杂志双栏框架 */
  .magazine-layout-wrapper { display: flex; gap: 50px; align-items: flex-start; margin-bottom: 60px; }

  /* 🧭 左边栏：高级折叠式大书架 */
  .left-sidebar-menu-panel { flex: 0 0 300px; background-color: #faf9f6; padding: 20px; border-radius: 12px; border: 1px solid #f2ede4; position: sticky; top: 30px; }
  .sidebar-menu-title { font-size: 1.05em; font-weight: bold; color: #2c3e50; padding-bottom: 10px; margin-bottom: 15px; border-bottom: 2px solid #e8dfcf; letter-spacing: 0.5px; }
  .sidebar-accordion-group { display: flex; flex-direction: column; gap: 12px; }

  /* 📜 HTML 原生伸缩手风琴高级精装 */
  .category-accordion-box { background-color: #ffffff; border: 1px solid #eef0f2; border-radius: 8px; overflow: hidden; transition: border-color 0.2s; }
  .category-accordion-box[open] { border-color: #e67e22; box-shadow: 0 3px 10px rgba(230,126,34,0.04); }
  
  /* 隐藏原装极简难看的黑色小三角箭头 */
  .accordion-header::-webkit-details-marker { display: none; }
  .accordion-header { display: flex; justify-content: space-between; align-items: center; padding: 14px 15px; font-weight: bold; color: #34495e; cursor: pointer; user-select: none; outline: none; }
  .accordion-header:hover { background-color: #fdfbf7; color: #e67e22; }
  
  .header-right-info { display: flex; align-items: center; gap: 8px; }
  .badge-count { font-size: 0.8em; color: #95a5a6; background-color: #f4f6f7; padding: 1px 6px; border-radius: 10px; }
  .arrow-icon { font-size: 0.7em; color: #bdc3c7; transition: transform 0.25s ease; display: inline-block; }
  
  /* 【核心魔法】当展开抽屉时，命令右侧的小箭头瞬间原地倒立顺时针旋转 90 度变成朝下！ 🌟 */
