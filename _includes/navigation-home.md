{% for link in site.data.navigation.main %}
  {% assign current_url = page.url | remove: '.html' %}
  {% assign link_url = link.url | prepend: '/' | remove: '.html' %}
  
  {% if link.right %}
    <a class="normal right {% if current_url == link_url %}active{% endif %}" href="{{ link.url | prepend: '/' | prepend: site.baseurl }}">{{ link.title }}</a>
  {% else %}
    <a class="normal {% if current_url == link_url %}active{% endif %}" href="{{ link.url | prepend: '/' | prepend: site.baseurl }}">{{ link.title }}</a>
  {% endif %}
{% endfor %}
