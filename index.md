---
layout: default
---

# Marcos **Bressan**

This is my personal website where I share my journey as a **Software Engineer** and technology enthusiast. Here you'll find my professional background, technical blog posts, and insights about **Programming**, **DevOps**, **Cloud Technologies**, and **Distributed Systems**.

---

# About Me

Software Engineer with a background in Electrical Engineering, holding a double degree from the Federal University of Ceará (Brazil) and École CentraleSupélec (France). 

Passionate about Machine Learning, Distributed Computing, and Smart Grid technologies. Currently focused on cloud infrastructure, DevOps practices, and building scalable software solutions.

---

## Recent Blog Posts

{% assign recent_posts = site.posts | slice: 0, 3 %}
{% if recent_posts.size > 0 %}
{% for post in recent_posts %}
### [{{ post.title }}]({{ post.url | relative_url }})
**{{ post.date | date: "%B %d, %Y" }}**{% if post.categories.size > 0 %} • {% for category in post.categories %}{{ category | capitalize }}{% unless forloop.last %}, {% endunless %}{% endfor %}{% endif %}

{% if post.excerpt %}{{ post.excerpt | strip_html | truncate: 120 }}{% endif %}

[Read More →]({{ post.url | relative_url }})

---
{% endfor %}

**[View All Blog Posts →](/blog)**
{% else %}
**🚀 New Blog Coming Soon!**

I'm excited to start sharing insights about technology, learning experiences, and tutorials. Check back soon for new content!

**[Visit Blog Section →](/blog)**
{% endif %}

---
