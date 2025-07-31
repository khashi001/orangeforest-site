---
layout: page
title: モバイルアプリ開発
permalink: /apps/
---

# 📱 モバイルアプリ開発

iOS・Androidアプリの企画から開発、リリースまでを一貫して行っています。
ユーザビリティを重視し、最新技術を活用したアプリを制作しています。

{% assign featured_apps = site.data.apps.apps | where: "featured", true %}
{% if featured_apps.size > 0 %}
## 🌟 注目のアプリ

{% for app in featured_apps %}
<div class="featured-app">
  <div class="app-header">
    <h3>{{ app.name }}</h3>
    <span class="app-status">{{ app.status }}</span>
  </div>
  
  <p class="app-description">{{ app.description }}</p>
  
  <div class="app-details">
    <p><strong>プラットフォーム:</strong> {{ app.platforms | join: ", " }}</p>
    <p><strong>リリース日:</strong> {{ app.release_date }}</p>
    <p><strong>バージョン:</strong> {{ app.version }}</p>
    {% if app.technologies %}
    <p><strong>使用技術:</strong> {{ app.technologies | join: ", " }}</p>
    {% endif %}
  </div>
  
  {% if app.links %}
  <div class="app-links">
    {% if app.links.app_store %}
      <a href="{{ app.links.app_store }}">📱 App Store</a>
    {% endif %}
    {% if app.links.google_play %}
      <a href="{{ app.links.google_play }}">🤖 Google Play</a>
    {% endif %}
    {% if app.links.github %}
      <a href="{{ app.links.github }}">📂 GitHub</a>
    {% endif %}
  </div>
  {% endif %}
  
  {% if app.development_story %}
  <details>
    <summary>📝 開発ストーリー</summary>
    <div>
      {{ app.development_story | markdownify }}
    </div>
  </details>
  {% endif %}
</div>
{% endfor %}
{% endif %}

## 📚 全てのアプリ

{% for app in site.data.apps.apps %}
  {% unless app.featured %}
  <div class="app-card">
    <h4>{{ app.name }}</h4>
    <p>{{ app.description }}</p>
    <div class="app-meta">
      <span>{{ app.platforms | join: ", " }}</span>
      <span>{{ app.release_date }}</span>
    </div>
  </div>
  {% endunless %}
{% endfor %}

## 📞 アプリ開発のご相談

新しいアプリのアイデアや既存アプリの改善など、お気軽にご相談ください。

<div class="contact-section">
  <a href="mailto:{{ site.email }}">📧 メールで相談</a>
  <a href="https://twitter.com/{{ site.author.twitter }}">🐦 Xで相談</a>
</div>