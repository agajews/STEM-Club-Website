{% for file in site.static_files %}
  {% if file.extname == include.extension %}
    {% assign components = file.path | split: '/' %}
    {% if components[1] == include.directory %}
!["{{ file.path }}"]({{ site.urlbase }}{{ file.path }})
    {% endif %}
  {% endif %}
{% endfor %}
