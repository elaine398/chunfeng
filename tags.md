---
layout: default
title: "专栏分类"
permalink: /tags/
---

<!-- 1. 🌟 复刻主页最顶部的超级极简顶栏 -->
<div class="custom-top-bar">
  <div class="top-bar-left-branding">
    <span class="top-brand-name">椿枫漫笔</span>
    <span class="top-brand-subtitle">Let's not remember years, remember moments</span>
  </div>
  <div class="top-bar-right-menu">
    <a class="top-menu-item" href="/chunfeng/">主页</a>
    <a class="top-menu-item" href="/chunfeng/tags/">分类</a>
  </div>
</div>

<div class="tags-page-container">
  <h2 class="tags-main-title">📚 椿枫漫笔 · 专栏画廊</h2>
  
  {% comment %} 自动循环抓取全站所有的分类标签 {% endcomment %}
  {% for tag in site.tags %}
    <div class="tag-section-box" id="{{ tag[0] }}">
      <h3 class="tag-section-header">📌 {{ tag[0] }} 专栏 ({{ tag[1].size }}篇)</h3>
      <div class="tag-posts-list">
        {% for post in tag[1] %}
          <div class="tag-post-row">
            <span class="tag-post-date">[{{ post.date | date: "%Y-%m-%d" }}]</span>
            <a class="tag-post-link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </div>
        {% endfor %}
      </div>
    </div>
  {% endfor %}
</div>

<style>
  body { padding: 0 40px; background-color: #ffffff; }
  .custom-top-bar { display: flex; justify-content: space-between; align-items: center; padding: 25px 0; border-bottom: 2px solid #e8dfcf; margin-bottom: 40px; }
  .top-brand-name { font-size: 1.8em; font-weight: bold; color: #2c3e50; letter-spacing: 1px; margin-right: 15px; }
  .top-brand-subtitle { font-size: 0.95em; color: #7f8c8d; font-style: italic; }
  .top-bar-right-menu { display: flex; gap: 25px; }
  .top-menu-item { font-size: 1.1em; font-weight: bold; color: #34495e !important; text-decoration: none !important; }
  .top-menu-item:hover { color: #e67e22 !important; }
  
  .tags-page-container { max-width: 800px; margin: 0 auto; }
  .tags-main-title { font-size: 1.6em; color: #2c3e50; border-bottom: 1px solid #f2ede4; padding-bottom: 15px; margin-bottom: 40px; }
  .tag-section-box { margin-bottom: 40px; scroll-margin-top: 100px; background: #faf9f6; padding: 25px; border-radius: 12px; border: 1px solid #f2ede4; }
  .tag-section-header { font-size: 1.25em; color: #e67e22; margin-top: 0; padding-bottom: 10px; border-bottom: 2px solid #e8dfcf; }
  .tag-posts-list { display: flex; flex-direction: column; gap: 12px; margin-top: 15px; }
  .tag-post-row { display: flex; gap: 15px; }
  .tag-post-date { color: #7f8c8d; }
  .tag-post-link { color: #2c3e50 !important; font-weight: bold; text-decoration: none !important; }
  .tag-post-link:hover { text-decoration: underline !important; color: #e67e22 !important; }
  footer, .theme-by, #downloads, .site-footer { display: none !important; }
</style>
