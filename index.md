---
title: sf9to5 | Journey of a Salesforce Geek
---

<div style="background-color: #fff3cd; border-left: 5px solid #ffc107; color: #333; padding: 14px 18px; margin: 16px 0 28px 0; border-radius: 4px;">
  <strong>Note:</strong> I no longer maintain the sf9to5.com site as of 2027. This serves as an archive for all the content I published over the years.
</div>

<style>
  .archive-list {
    list-style: none;
    padding-left: 0;
  }
  .archive-item {
    display: flex;
    align-items: baseline;
    margin-bottom: 10px;
    line-height: 1.5;
  }
  .archive-date {
    font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;
    color: #555;
    min-width: 120px;
    flex-shrink: 0;
    margin-right: 16px;
  }
</style>

<ul class="archive-list">
  {% for post in site.posts %}
    <li class="archive-item">
      <span class="archive-date">{{ post.date | date: "%Y-%m-%d" }}</span>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

