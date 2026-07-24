{% for link in site.data.navigation.main %}
  {% assign current_url = page.url | remove: '.html' %}
  {% assign link_url = link.url | prepend: '/' | remove: '.html' %}
  {% assign nav_delay = forloop.rindex0 | times: 35 | plus: 50 %}
  <a class="normal {% if current_url == link_url %}active{% endif %}" href="{{ site.baseurl }}/{{ link.url }}" style="--nav-delay: {{ nav_delay }}ms;"{% if current_url == link_url %} aria-current="page"{% endif %}>{{ link.title }}</a>
{% endfor %}
