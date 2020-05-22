---
title:  "Blogs"
layout: archive
permalink: /Blogs/
author_profile: true
comments: true
---

<font size="2"><i>Learning to be an effective writer is one of my long-term personal goals. This blog documents my writing journey. I hope it is useful to you, too. Please leave a comment if you want to have a discussion about the contents :) </i></font>

<ul>
  {% for post in site.posts %}
    {% unless post.next %}
      <font color="#778899"><h2>{{ post.date | date: '%Y %b' }}</h2></font>
    {% else %}
      {% capture year %}{{ post.date | date: '%Y %b' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y %b' }}{% endcapture %}
      {% if year != nyear %}
        <font color="#778899"><h2>{{ post.date | date: '%Y %b' }}</h2></font>
      {% endif %}

    {% endunless %}
   {% include archive-single.html %}
  {% endfor %}
</ul>

