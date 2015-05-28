---
layout: archivo
---
{% for post in site.posts reversed %}
  {% assign m = post.date | date: "%-m" %}
  * {{ post.date | date: "%-d de " }}
  {% case m %}
    {% when '1' %}Enero
    {% when '2' %}Febrero
    {% when '3' %}Marzo
    {% when '4' %}Abril
    {% when '5' %}Mayo
    {% when '6' %}Junio
    {% when '7' %}Julio
    {% when '8' %}Agosto
    {% when '9' %}Septiembre
    {% when '10' %}Octubre
    {% when '11' %}Noviembre
    {% when '12' %}Diciembre
  {% endcase %}{{ post.date | date: " de %Y" }} &nbsp; &raquo; [ {{ post.title }} ]({{site.baseurl}}{{ post.url }})
{% endfor %}
