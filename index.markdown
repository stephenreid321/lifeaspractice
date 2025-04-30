---
layout: application
---

<header class="px-lg-5">
  <div class="jumbotron container text-center bg-transparent mb-0 pb-0">
    <h1 class="mb-0">
      Where Daily Life
      <br />
      Meets Deep Practice
    </h1>
    <p class="lead my-4">
      A Yearlong Group Mentorship
      <br />
      with Stephen Reid and Laura Gottlieb
      <br />
      Sep 2025 – Aug 2026
    </p>
    <p class="mb-3">
      First time running this programme!
      <br />
      Previous offerings: <a target="_blank" href="https://dandelion.events/u/stephenreid321#feedback">4.7/5 from 168 reviews</a>
    </p>
    <p class="lead mb-3 star-rating">
     <a target="_blank" href="https://dandelion.events/u/stephenreid321#feedback">
        <span class="stars-background">
          <i class="bi bi-star"></i><i class="bi bi-star"></i><i class="bi bi-star"></i><i class="bi bi-star"></i><i class="bi bi-star"></i>
        </span>
        <span class="stars-foreground" style="width: 94%;">
          <i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i><i class="bi bi-star-fill"></i>
        </span>
      </a>
    </p>
    <p>
      <a class="btn btn-primary btn-lg d-lg-none" id="header-apply-button" target="_blank" href="https://airtable.com/appxD3blgx0uJJ35b/pag8aRYP7rzvoZDCL/form">Apply</a>
    </p>
  </div>
</header>

{% for section in site.sections %}
  <section id="{{ section.id }}" class="section">
    <div class="container">
      <h1 class="pt-5">{{ section.divider }}<br />{{ section.title }}</h1>
      {% capture section_content %}{% include_relative _sections/{{ section.id }}.md %}{% endcapture %}
      {{ section_content | markdownify }}
    </div>
  </section>  
{% endfor %}
