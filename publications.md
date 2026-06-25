---
layout: page
title: Lab Publications
permalink: /publications/
---

<div style="display: flex; flex-direction: column; gap: 20px; margin-top: 25px;">
  {% for pub in site.data.scholar_publications %}
    {% assign pub_year = pub.year | plus: 0 %}
    {% if pub_year >= 2023 %}
    <div style="background: #fff; padding: 20px; border: 1px solid #e5e7eb; border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.02); line-height: 1.6; text-align: left; display: flex; gap: 15px; align-items: start;">
      
      <span style="font-weight: bold; color: #2563eb; font-size: 1.05rem; min-width: 25px;">
        {{ forloop.index }}.
      </span>

      <span style="font-size: 1.05rem; color: #1f2937;">
        {{ pub.authors }} ({{ pub.year }}). 
        
        {{ pub.title }}. 
        
        <em style="color: #1f2937;">{{ pub.venue }}</em>{% if pub.volume or pub.pages %},{% else %}.{% endif %}
        
        {% if pub.volume %}
          <em style="color: #1f2937;"> {{ pub.volume }}</em>{% if pub.issue %}({{ pub.issue }}){% endif %}{% if pub.pages %}, {{ pub.pages }}.{% else %}.{% endif %}
        {% else %}
          {% if pub.issue %}({{ pub.issue }}){% endif %}{% if pub.pages %} {{ pub.pages }}.{% endif %}
        {% endif %}
        
        {% if pub.doi %}
          <br>
          <a href="{{ pub.doi }}" target="_blank" rel="noopener noreferrer" style="color: #2563eb; text-decoration: none; font-size: 0.95rem;" onmouseover="this.style.textDecoration='underline'" onmouseout="this.style.textDecoration='none'">{{ pub.doi }}</a>
        {% endif %}
      </span>
    </div>
    {% endif %}
  {% endfor %}
</div>