---
title: Gertrude Digital Editions
layout: default
---

<blockquote>“In the next fifty years the entirety of our inherited archive of cultural works will have to be reedited within a network of digital storage, access, and dissemination”.
<br />
<span id="blockquoteCitation">-Jerome McGann, A New Republic of Letters: Memory and Scholarship in the Age of Digital Reproduction, 2014.</span></blockquote>

Digital Editions at W&L is an effort of [Leyburn Library](http://library.wlu.edu), [Digital Humanities](http://digitalhumanities.wlu.edu), and the [Digital Culture and Information minor](http://go.wlu.edu/dci) to publish edited and annotated texts from our Special Collections and Archives and the collections of our community partners. 
<div class="row">

<!-- The card feature works by creating a variable called 'featured' consisting of pages that have featured: true in the YAML metadata. For each page that matches those conditions, a Bootstrap card is created and info from the page is filled in. --> 

{% assign featured = site.documents | where:"featured","true"  %}

  {% for card in featured  %}

<div class="card">
  <a href="{{card.url | relative_url }}"><img src="{{ site.baseurl }}{{card.image}}" class="card-img-top" alt="..."></a>
  <div class="card-body">
    <h3 class="card-title">{{ card.title }}</h3>
    <p class="card-text">{{ card.author }}</p>
    <p class="card-text">{{ card.description }}</p>
    <a href="{{card.url | relative_url }}" class="btn btn-info">Read it</a>
  </div>
</div>
{% endfor %}
</div>