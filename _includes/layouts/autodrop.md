<li class="nav-item dropdown px-4">
<a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false" style="color: #fff;">{{ include.title }}</a>
<div class="dropdown-menu" aria-labelledby="navbarDropdown">

{% assign items = include.what | sort: 'weight' %}

{% for item in items %}
{% if item.level != 0  %}{% continue %}{% endif %}
{% if item.div %}<div class="dropdown-divider"></div>{% endif %}

<a class="dropdown-item" href="{{ item.url | relative_url }}">{{ item.title }}</a>
{% endfor %}
</div>
</li>
