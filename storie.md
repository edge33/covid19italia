---
lang: it
layout: page
title: Buone Notizie
permalink: /storie/
---

In questa pagina raccontiamo le principali storie di successo che questo progetto è riuscito a realizzare. Tante piccole cose che, messe insieme, speriamo offrano un contributo utile.

{% assign storie = site.storie | sort: 'date' %}

<div class="posts">
  {% for post in storie reversed%}
      <article class="post">
        <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

        <div class="entry">
          {{ post.excerpt }}
        </div>

        <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Leggi tutto</a>
      </article>
      <p class="post-meta">
        Posted on {{ post.date | date: "%B %-d, %Y" }}
      </p>
  {% endfor %}
</div>
