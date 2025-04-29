---
layout: application
---

<header class="px-lg-5 my-5">
  <div class="jumbotron container text-center bg-transparent">
    <h1 class="display-4 pb-0">
      Where Daily Life
      <br />
      Meets Deep Practice
    </h1>
    <p class="lead mb-3">
      A Yearlong Group Mentorship
      <br />
      with Stephen Reid and Laura Gottlieb
      <br />
      Sep 2025 – Aug 2026
    </p>
  </div>
</header>

{% for section in site.sections %}
  <section id="{{ section.id }}" class="section">
    <div class="container">
      <h1 class="mt-5">{{ section.divider }}<br />{{ section.title }}</h1>
      {% capture section_content %}{% include_relative _sections/{{ section.id }}.md %}{% endcapture %}
      {{ section_content | markdownify }}
    </div>
  </section>  
{% endfor %}
