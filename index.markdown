---
layout: application
---

<header class="px-lg-5 my-5">
  <div class="jumbotron container text-center bg-transparent">
    <h1>
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
    <a class="btn btn-primary btn-lg d-lg-none" id="header-apply-button" target="_blank" href="https://airtable.com/appxD3blgx0uJJ35b/pag8aRYP7rzvoZDCL/form">Apply</a>
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
