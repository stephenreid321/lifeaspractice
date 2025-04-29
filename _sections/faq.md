<h1>Frequently Asked Questions</h1>

<div class="accordion" id="faqAccordion">
  {% for item in site.faq_items %}
    <div class="card">
      <div class="card-header" id="heading{{ forloop.index }}">
          <a href="javascript:;" class="{% unless forloop.first %} collapsed{% endunless %}" data-toggle="collapse" data-target="#collapse{{ forloop.index }}">
            {{ item.question }}
          </a>
      </div>
      <div id="collapse{{ forloop.index }}" class="collapse {% if forloop.first %}show{% endif %}" data-parent="#faqAccordion">
        <div class="card-body">
          {{ item.answer }}
        </div>
      </div>
    </div>
  {% endfor %}
</div>