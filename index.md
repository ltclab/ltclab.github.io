---
layout: page
title: Home
---

<!-- 1. Wix-Style Hero Banner Section -->
<div style="text-align: center; padding: 60px 20px; background: linear-gradient(135deg, #74ebd5 0%, #9fa8da 100%); color: white; border-radius: 8px; margin-bottom: 40px;">
  <h1 style="font-size: 3rem; margin-weight: 700; margin-bottom: 10px;">LTC Lab</h1>
  <p style="font-size: 1.3rem; opacity: 0.9; max-width: 600px; margin: 0 auto;">Innovating, testing, and building the future of web experiences. Welcome to our digital laboratory.</p>
</div>

<!-- 2. Visual Grid Columns -->
<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin-bottom: 50px;">
  
  <div style="padding: 20px; border: 1px solid #eee; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.05); text-align: center;">
    <h3 style="color: #333;">Our Research</h3>
    <p style="color: #666; font-size: 0.95rem;">Exploring novel development tools, cloud architectures, and user-first digital products.</p>
  </div>

  <div style="padding: 20px; border: 1px solid #eee; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.05); text-align: center;">
    <h3 style="color: #333;">The Blog</h3>
    <p style="color: #666; font-size: 0.95rem;">Read regular logs, code snippets, and behind-the-scenes thoughts straight from our laboratory.</p>
  </div>

</div>

<!-- 3. Wix-Style Centered Blog Feed Section -->
<hr style="border: 0; height: 1px; background: #eee; margin-bottom: 40px;">

<h2 style="text-align: center; margin-bottom: 30px; font-weight: 600; color: #222;">Latest Updates</h2>

<ul style="list-style: none; padding: 0; max-width: 700px; margin: 0 auto;">
  {% for post in site.posts %}
    <li style="margin-bottom: 25px; padding-bottom: 25px; border-bottom: 1px solid #fafafa;">
      <span style="color: #999; font-size: 0.85rem; text-transform: uppercase; letter-spacing: 1px;">{{ post.date | date: "%b %d, %Y" }}</span>
      <h3 style="margin: 5px 0 10px 0;">
        <a style="color: #333; text-decoration: none; font-weight: 600;" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      <p style="color: #666; font-size: 0.95rem; line-height: 1.6;">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    </li>
  {% endfor %}
</ul>