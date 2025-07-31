---
layout: home
title: Orange Forest
---

# Orange Forest

<div class="hero-section">
{% if site.current_focus == 'apps' %}
  <div class="current-focus">
    <h2>🚀 最新情報</h2>
    <div class="featured-app">
      <h3>新しいアプリをリリースしました！</h3>
      <p>詳細は<a href="/apps/">アプリ開発ページ</a>をご覧ください。</p>
    </div>
  </div>
{% elsif site.current_focus == '3dcg' %}
  <div class="current-focus">
    <h2>🎨 最新情報</h2>
    <div class="featured-3dcg">
      <h3>新しい3DCG作品を公開しました！</h3>
      <p>詳細は<a href="/3dcg/">3DCG制作ページ</a>をご覧ください。</p>
    </div>
  </div>
{% endif %}
</div>

## 私の活動

<div class="services-grid">
  <div class="service-card">
    <h3>📱 モバイルアプリ開発</h3>
    <p>iOS/Androidアプリの企画・開発・リリースを行っています。</p>
    <a href="/apps/" class="btn">詳細を見る</a>
  </div>
  
  <div class="service-card">
    <h3>🎮 電子工作プログラミング講師</h3>
    <p>PCN幕張でプログラミング教室を開催しています。</p>
    <a href="/education/" class="btn">詳細を見る</a>
  </div>
  
  <div class="service-card">
    <h3>🎬 3DCG映像制作</h3>
    <p>高品質な3DCG素材・映像の制作・販売を行っています。</p>
    <a href="/3dcg/" class="btn">詳細を見る</a>
  </div>
</div>

## 最新の投稿

<div class="recent-posts">
{% for post in site.posts limit:3 %}
  <article class="post-preview">
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p class="post-meta">{{ post.date | date: "%Y年%m月%d日" }}</p>
    <p>{{ post.excerpt }}</p>
  </article>
{% endfor %}
</div>

## SNS・動画

<div class="social-feed">
  <div class="twitter-feed">
    <h3>X (Twitter)</h3>
    <div id="twitter-feed">
      <p>最新の投稿を準備中です...</p>
    </div>
  </div>
  
  <div class="youtube-feed">
    <h3>YouTube</h3>
    <div id="youtube-feed">
      <p>最新の動画を準備中です...</p>
    </div>
  </div>
</div>

## お問い合わせ

お仕事のご依頼やご質問は、以下からお気軽にご連絡ください。

<div class="contact-buttons">
  <a href="mailto:{{ site.email }}" class="btn btn-primary">📧 メールで連絡</a>
  <a href="https://twitter.com/{{ site.author.twitter }}" class="btn btn-secondary">🐦 Xで連絡</a>
</div>