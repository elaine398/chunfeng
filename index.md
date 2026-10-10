---
layout: default
---

<div class="magazine-container">

  <!-- 🧭 左边竖栏：7大分类直达小方块 -->
  <div class="left-sidebar-menu">
    <div class="sidebar-menu-title">📚 专栏分类</div>
    <div class="sidebar-box-grid">
      {% for category in site.sidebar-categories %}
        <a class="sidebar-category-box" href="#{{ category.tag }}">
          <span class="box-text">{{ category.name }}</span>
          <span class="box-count">({{ site.tags[category.tag].size | default: 0 }})</span>
        </a>
      {% endfor %}
    </div>
  </div>

  <!-- 📄 右边竖栏：真实的历史文章流 -->
  <div class="right-articles-flow">
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

<!-- 🎨 专属顶级杂志双栏排版皮肤控制 (CSS) -->
<style>
  /* Split layout into a gorgeous asymmetrical double column */
  .magazine-container {
    display: flex;
    flex-wrap: wrap;
    gap: 40px;
    margin-top: 30px;
    align-items: flex-start;
  }

  /* Left Column: Fixed structural width for your 7 blocks */
  .left-sidebar-menu {
    flex: 1;
    min-width: 260px;
    background-color: #faf9f6;
    padding: 20px;
    border-radius: 12px;
    border: 1px solid #f2ede4;
  }
  .sidebar-menu-title {
    font-size: 1.1em;
    font-weight: bold;
    color: #2c3e50;
    padding-bottom: 12px;
    margin-bottom: 15px;
    border-bottom: 2px solid #e8dfcf;
    letter-spacing: 1px;
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
    font-weight: 500;
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

  /* Right Column: Expansive area for your articles list */
  .right-articles-flow {
    flex: 2;
    min-width: 320px;
  }
  .flow-header {
    font-size: 1.4em;
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
    font-size: 1.05em;
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
    white-space: nowrap;
  }
</style>
