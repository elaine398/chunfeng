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

  <!-- 🧭 左边栏：固态吸顶悬浮大书架（带整栏独立高级滚动条 🌟） -->
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
            <span class="badge-count holiday-adjust">{{ site.tags["短文"].size | default: 0 }}</span>
            <span class="arrow-icon">▶</span>
          </span>
        </summary>
        <div class="accordion-sub-links-list">
          {% for post in site.tags["短文"] %}
            <div class="sub-article-row-block">
              <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
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
              <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
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
              <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
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
              <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
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
              <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
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
              <a class="sub-article-title-link" href="#post-{{ post.id | slugify }}">
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

  <!-- 📄 右边中央主舞台：展示段落分明的详细正文 -->
  <div class="right-articles-flow-panel">
    
    <!-- 🏡 缺省默认欢迎室 -->
    <div class="content-inside-card default-welcome-room">
      <h1 class="welcome-main-title">欢迎来到“椿枫漫笔”独立书斋</h1>
      <p class="welcome-p">这里是一片完全属于文字的净土。没有多余的喧嚣与广告，有且仅有关于生活感悟、读书摘录、以及东欧与纽约旅行的真实足迹。</p>
      <p class="welcome-p">💡 <strong>阅读指南</strong>：请用鼠标点击左侧的【专栏分类】展开您的固态书架，轻点任意一篇随笔标题，即可在这里直接享受高质感、段落分明的优雅无缝阅读。</p>
      <div class="welcome-decor-line"></div>
    </div>

    <!-- 📖 全量文章详细正文隐藏展厅 -->
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
        
        <div class="article-inside-body">
          {{ post.content }}
        </div>
      </div>
    {% endfor %}

  </div>

</div>

<!-- 3. 🎨 纯手工完全自定义全屏视觉控制皮肤 (CSS 终极完美大收官魔术) -->
<style>
  header { display: none !important; height: 0 !important; padding: 0 !important; margin: 0 !important; }
  body { margin: 0; padding: 0 40px; background-color: #ffffff; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; }

  /* Top Bar 顶栏 */
  .custom-top-bar { display: flex; justify-content: space-between; align-items: center; padding: 25px 0; border-bottom: 2px solid #e8dfcf; margin-bottom: 40px; margin-top: 20px; }
  .top-brand-name-link { font-size: 1.9em; font-weight: bold; color: #2c3e50 !important; letter-spacing: 1px; margin-right: 15px; text-decoration: none !important; transition: color 0.2s; }
  .top-brand-name-link:hover { color: #e67e22 !important; }
  .top-brand-subtitle { font-size: 0.95em; color: #7f8c8d; font-style: italic; }
  .top-bar-right-menu { display: flex; gap: 25px; }
  .top-menu-item { font-size: 1.1em; font-weight: bold; color: #34495e !important; text-decoration: none !important; }
  .top-menu-item:hover, .active-nav { color: #e67e22 !important; }

  /* 双栏杂志大排版外壳 */
  .magazine-layout-wrapper { display: flex; gap: 50px; align-items: flex-start; margin-bottom: 60px; }

  /* 🧭 🧭 🧭 【全新蜕变】左边栏：固态全屏吸顶悬浮大书架 🧭 🧭 🧭 */
  .left-sidebar-menu-panel { 
    flex: 0 0 310px; 
    background-color: #faf9f6; 
    padding: 20px; 
    border-radius: 12px; 
    border: 1px solid #f2ede4; 
    
    /* 核心魔法 1：开启吸顶跟随模式，当右边文章往下拉时，左边像磁铁一样死死吸在左侧！ */
    position: sticky !important; 
    top: 25px !important; 
    
    /* 核心魔法 2：高能锁死！强行命令整个左边栏的外壳总高度，绝对不能超过读者屏幕的显示高度！ */
    max-height: calc(100vh - 90px) !important; 
    
    /* 核心魔法 3：当抽屉拉开撑满时，不准往下挤，直接在左边栏自己内部强行亮起整栏大滚动条！ */
    overflow-y: auto !important; 
    overflow-x: hidden !important;
  }
  
  .sidebar-menu-title { font-size: 1.05em; font-weight: bold; color: #2c3e50; padding-bottom: 10px; margin-bottom: 15px; border-bottom: 2px solid #e8dfcf; letter-spacing: 0.5px; }
  .sidebar-accordion-group { display: flex; flex-direction: column; gap: 12px; }

