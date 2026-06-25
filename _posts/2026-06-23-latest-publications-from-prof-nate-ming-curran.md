---
layout: post
title: Latest publications from the Lab
date: 2026-06-23T15:13
---

Here are the publications from the LTC Lab since 2023:

<div style="display: flex; flex-direction: column; gap: 20px; margin-top: 25px;">
  {% for pub in site.data.scholar_publications %}
    {% assign pub_year = pub.year | plus: 0 %}
    {% if pub_year >= 2023 %}
    <div style="background: #fff; padding: 20px; border: 1px solid #e5e7eb; border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.02); line-height: 1.6;">
      <span style="font-size: 1.05rem; color: #1f2937;">
        {{ pub.authors }} ({{ pub.year }}). 
        
        {% if pub.link and pub.link != "#" %}
          <a href="{{ pub.link }}" target="_blank" rel="noopener noreferrer" style="color: #2563eb; text-decoration: none; font-weight: 500;" onmouseover="this.style.textDecoration='underline'" onmouseout="this.style.textDecoration='none'">{{ pub.title }}</a>.
        {% else %}
          <strong>{{ pub.title }}</strong>.
        {% endif %}
        
        {% if pub.venue and pub.venue != "Journal/Conference" %}
          <em style="color: #4b5563;">{{ pub.venue }}</em>.
        {% endif %}
      </span>
    </div>
    {% endif %}
  {% endfor %}
</div>