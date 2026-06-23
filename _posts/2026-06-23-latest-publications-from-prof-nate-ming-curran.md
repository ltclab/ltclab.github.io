---
layout: post
title: Latest publications from the Lab
date: 2026-06-23T15:13
---

Here are some of the latest publications from the LTC Lab:

<div style="display: flex; flex-direction: column; gap: 20px; margin-top: 25px;">
  <!-- Added limit: 20 to the Liquid loop below -->
  {% for pub in site.data.scholar_publications limit: 20 %}
  <div style="background: #fff; padding: 20px; border: 1px solid #e5e7eb; border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.02);">
    <h3 style="margin: 0 0 8px 0; color: #1f2937; font-size: 1.15rem;">
      <a href="{{ pub.link }}" target="_blank" rel="noopener noreferrer" style="color: #2563eb; text-decoration: none;">{{ pub.title }}</a>
    </h3>
    <p style="margin: 0 0 5px 0; font-size: 0.95rem; color: #4b5563;"><strong>Authors:</strong> {{ pub.authors }}</p>
    <p style="margin: 0; font-size: 0.9rem; color: #6b7280;"><em>{{ pub.venue }}</em>, {{ pub.year }}</p>
  </div>
  {% endfor %}
</div>