# Emoji Resources 😄 📚
> Find services, add-ons and actual emojis to help with all your emoji needs

{% assign pages = site.pages | sort: 'name' %}

<ul>
{% for p in pages %}
{% unless page == p %}
<li>
    <a href="{{ p.url | relative_url }}">
        {{ p.title }}
    </a>
</li>
{% endunless %}
{% endfor %}
</ul>
