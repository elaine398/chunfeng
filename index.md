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

  <!-- 🧭 左边栏：固态全屏吸顶悬浮大书架（坚不可摧的 310px 黄金身材 🛡️） -->
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

  <!-- 📄 右边中央主舞台：精选最近发表的 5 篇摘要流（原地无缝展开收起 ✨） -->
  <div class="right-articles-flow-panel">
    <div class="content-panel-card default-welcome-stream-room" style="display: block !important;">
      <h2 class="magazine-stream-header">✨ 最近发表 · 精选随笔</h2>
      
      {% for post in site.posts limit:5 %}
        <div class="stream-article-item">
          <h3 class="stream-title">{{ post.title }}</h3>
          <div class="stream-meta">📅 {{ post.date | date: "%Y-%m-%d" }} &nbsp;|&nbsp; 🏷️ {{ post.tags | first }}</div>
          
          <details class="readmore-accordion">
            <summary class="readmore-btn-summary">
              <!-- 纯文字安全摘要截取 -->
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

<!-- 3. 🎨 纯手工完全自定义全屏视觉控制皮肤 (CSS 终极无缝并排死锁版) -->
<style>
  html, body, .wrapper, #main_content_wrap, section.main-content, .container, main {
    max-width: 100% !important;   
    width: 100% !important;
    padding: 0 !important;
    margin: 0 !important;
  }

  header { display: none !important; height: 0 !important; padding: 0 !important; margin: 0 !important; }
  
  body { 
    background-color: #ffffff; 
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    padding: 0 40px !important; 
    box-sizing: border-box !important;
  }

  /* Top Bar 顶栏 */
  .custom-top-bar { display: flex; justify-content: space-between; align-items: center; padding: 25px 0; border-bottom: 2px solid #e8dfcf; margin-bottom: 40px; margin-top: 20px; width: 100% !important; box-sizing: border-box; }
  .top-brand-name-link { font-size: 1.9em; font-weight: bold; color: #2c3e50 !important; letter-spacing: 1px; text-decoration: none !important; transition: color 0.2s; }
  .top-brand-name-link:hover { color: #e67e22 !important; }
  .top-brand-subtitle { font-size: 0.95em; color: #7f8c8d; font-style: italic; margin-left: 15px; }
  .top-bar-right-menu { display: flex; gap: 25px; }
  .top-menu-item { font-size: 1.1em; font-weight: bold; color: #34495e !important; text-decoration: none !important; }
  .top-menu-item:hover, .active-nav { color: #e67e22 !important; }

  /* 🔒 【双栏永久死锁并排骨架】：无论发生什么切换，左右两边绝对横向并排坐，100%禁止换行塌陷！ */
  .magazine-layout-wrapper { 
    display: flex !important; 
    flex-direction: row !important; 
    flex-wrap: nowrap !important;       /* 彻底封死换行机制 */
    gap: 45px !important; 
    align-items: flex-start !important; 
    width: 100% !important;
    box-sizing: border-box !important;
  }

  /* 🧭 左边栏：固态310px黄金吸顶悬浮柜（整栏自带独立小滚动条 🌟） */
  .left-sidebar-menu-panel { 
    flex: 0 0 310px !important; 
    width: 310px !important; 
    min-width: 310px !important;
    background-color: #faf9f6; 
    padding: 20px; 
    border-radius: 12px; 
