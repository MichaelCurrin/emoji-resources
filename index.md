# Emoji Resources homepage 😄 📚
> Find services, add-ons and actual emojis to help with all your emoji needs

[![MichaelCurrin - emoji-resources](https://img.shields.io/static/v1?label=MichaelCurrin&message=emoji-resources&color=blue&logo=github)](https://github.com/MichaelCurrin/emoji-resources)


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

