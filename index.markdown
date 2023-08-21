---
layout: default
title: "home"
---

<section>
    <h3>about</h3>
    <div>
        {{ site.about | markdownify }}
    </div>
</section>

{% if site.posts.size > 0 %}
<section>
    <h3>writing</h3>
    {% for post in site.posts %}
    <div id="writing">
        <a href="{{ post.url }}">
            {{ post.title }}
        </a>
        {{ post.date | date_to_long_string: "ordinal" | downcase }}
    </div>
    {% endfor %}
</section>
{% endif %}
