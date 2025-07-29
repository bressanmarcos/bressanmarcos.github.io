---
layout: default
title: Blog
permalink: /blog/
---

# Tech Blog

Welcome to my technical blog! Here I share deep dives into technology, document my learning experiences, and create practical guides for fellow developers and engineers.

## What I Write About

- **Software Development** - Best practices, frameworks, and tools
- **DevOps & Cloud** - AWS, Docker, Kubernetes, CI/CD
- **Machine Learning** - Algorithms, applications, and insights  
- **Distributed Systems** - Microservices, multi-agent systems
- **Learning Notes** - Documentation of my continuous learning journey
- **How-To Guides** - Step-by-step tutorials and instructions

---

{% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}

{% if site.posts.size > 0 %}

## Blog Statistics
- **{{ site.posts.size }}** Total Posts
- **{{ posts_by_year.size }}** Years Writing  
- **{{ site.categories.size }}** Categories

---

{% for year_group in posts_by_year %}
## {{ year_group.name }} ({{ year_group.items.size }} posts)

{% for post in year_group.items %}
### [{{ post.title }}]({{ post.url | relative_url }})
**{{ post.date | date: "%B %d, %Y" }}**{% if post.categories.size > 0 %} • {% for category in post.categories %}{{ category | capitalize }}{% unless forloop.last %}, {% endunless %}{% endfor %}{% endif %}

{% if post.excerpt %}{{ post.excerpt | strip_html | truncate: 150 }}{% endif %}

{% if post.tags.size > 0 %}*Tags: {% for tag in post.tags %}{{ tag }}{% unless forloop.last %}, {% endunless %}{% endfor %}*{% endif %}

[Read Full Article →]({{ post.url | relative_url }})

---
{% endfor %}
{% endfor %}

{% else %}

## Blog Coming Soon!

I'm preparing exciting content about technology, development insights, and learning experiences. Stay tuned for updates!

**Coming Soon:**
- Technical Deep Dives
- Learning Tutorials  
- Industry Insights

{% endif %}

## Stay Updated

Want to be notified when I publish new posts? Connect with me on social media for the latest updates!

- [Follow on LinkedIn](https://www.linkedin.com/in/bressanmarcos/)
- [Star on GitHub](https://github.com/bressanmarcos) 