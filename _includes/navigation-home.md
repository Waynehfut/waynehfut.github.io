{% for link in site.data.navigation.main %}
  {% assign current_url = page.url | remove: '.html' %}
  {% assign link_url = link.url | prepend: '/' | remove: '.html' %}
  <a class="normal {% if current_url == link_url %}active{% endif %}" href="{{ site.baseurl }}/{{ link.url }}">{{ link.title }}</a>
{% endfor %}
