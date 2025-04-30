<div class="accordion" id="faqAccordion">
  {% for item in site.faq_items %}
    <div class="card">
      <div class="card-header" id="heading{{ forloop.index }}">
          <a href="javascript:;" class="collapsed" data-toggle="collapse" data-target="#collapse{{ forloop.index }}">
            {{ item.question }}
          </a>
      </div>
      <div id="collapse{{ forloop.index }}" class="collapse" data-parent="#faqAccordion">
        <div class="card-body">
          {{ item.answer }}
        </div>
      </div>
    </div>
  {% endfor %}
</div>