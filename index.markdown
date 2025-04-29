---
layout: application
---

{% for section in site.sections %}
  <div class="divider">{{ section.divider }}</div>
  <section id="{{ section.id }}" class="section">
    <div class="container">
      {% capture section_content %}{% include_relative _sections/{{ section.id }}.md %}{% endcapture %}
      {{ section_content | markdownify }}
    </div>
  </section>  
{% endfor %}
