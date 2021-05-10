# Emoji Resources homepage 😄 📚
> Find services, add-ons and actual emojis to help with all your emoji needs

[![MichaelCurrin - emoji-resources](https://img.shields.io/static/v1?label=MichaelCurrin&message=emoji-resources&color=blue&logo=github)](https://github.com/MichaelCurrin/emoji-resources)

{% comment %} For some reason, GitHub's style page appears as a page rather than a static asset, so it must be excluded from the menu. {% endcomment %}

{% assign pages = site.pages | sort: 'name' %}

<ul>
{% for p in pages %}
{% unless page == p or p.name == 'style.css' %}
<li>
    <a href="{{ p.url | relative_url }}">
        {{ p.title }}
    </a>
</li>
{% endunless %}
{% endfor %}
</ul>
