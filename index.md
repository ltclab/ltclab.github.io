---
layout: page
---

<div style="text-align: center; padding: 50px 20px; background: linear-gradient(135deg, #4f46e5 0%, #3b82f6 100%); color: white; border-radius: 8px; margin-bottom: 40px;">
  <h1 style="font-size: 3rem; margin: 0 0 10px 0; font-weight: 700; letter-spacing: -0.5px;">Language Technology and Culture Lab</h1>
</div>

<div style="background: #ffffff; padding: 30px; border: 1px solid #e5e7eb; border-radius: 8px; box-shadow: 0 4px 6px -1px rgba(0,0,0,0.05); margin-bottom: 40px;">
  <h2 style="color: #1f2937; margin-top: 0; font-size: 1.75rem; border-bottom: 2px solid #f3f4f6; padding-bottom: 10px; font-weight: 600;">About Our Lab</h2>
  <p style="color: #4b5563; font-size: 1.1rem; line-height: 1.7; text-align: justify; margin-bottom: 0;">
    The lab’s core mission is to promote interdisciplinary collaborative research at the intersection of language, technology, and culture. The lab seeks to conduct research that is theoretically grounded and has practical, real-world relevance. The lab was founded by Nate Ming Curran and the majority of lab members are his current or former students. However, the lab also includes several affiliated researchers who frequently collaborate with the lab. Lab members conduct research collaboratively in a mentorship model that prioritizes academic curiosity, collegiality, and collaboration.
  </p>
</div>

<hr style="border: 0; height: 1px; background: #e5e7eb; margin: 40px 0;">
<h2 style="text-align: center; margin-bottom: 30px; font-weight: 600; color: #1f2937;">Latest Lab Updates</h2>

<ul style="list-style: none; padding: 0; max-width: 750px; margin: 0 auto 50px auto;">
  {% for post in site.posts %}
    <li style="margin-bottom: 25px; padding-bottom: 25px; border-bottom: 1px solid #f3f4f6;">
      <span style="color: #9ca3af; font-size: 0.85rem; text-transform: uppercase; letter-spacing: 1px;">{{ post.date | date: "%b %d, %Y" }}</span>
      <h3 style="margin: 5px 0 10px 0;">
        <a style="color: #2563eb; text-decoration: none; font-weight: 600;" href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      <p style="color: #4b5563; font-size: 0.95rem; line-height: 1.6;">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
    </li>
  {% endfor %}
</ul>

<div style="text-align: center; margin-top: 40px; margin-bottom: 20px;">
  <a href="https://docs.google.com/forms/d/e/1FAIpQLScIqVxnWMpCOGOnpt-M7xhjczy43RUizZDhBEXtmU9NQNpj7Q/viewform" 
     target="_blank" 
     rel="noopener noreferrer" 
     style="display: inline-block; background-color: #0056b3; color: white; padding: 12px 28px; font-size: 1.1rem; font-weight: 600; text-decoration: none; border-radius: 5px; box-shadow: 0 2px 4px rgba(0,0,0,0.1); transition: background-color 0.2s ease;">
    Contact Us
  </a>
</div>