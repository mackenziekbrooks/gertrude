---
title: Gertrude Digital Edition Platform Demo
layout: default
---

<blockquote>“In the next fifty years the entirety of our inherited archive of cultural works will have to be reedited within a network of digital storage, access, and dissemination”.
<br />
<span id="blockquoteCitation">-Jerome McGann, A New Republic of Letters: Memory and Scholarship in the Age of Digital Reproduction, 2014.</span></blockquote>

<div class="row">
  <div class="col-md-6" markdown="1">
Gertrude is platform for creating lightweight and **sustainable digital editions** with accompanying [documentation]() and course materials. Gertrude was designed within the small liberal arts college context in which project teams are small, but may include technologists, librarians, scholars, and students. The platform combines [TEI-XML](https://tei-c.org/) encoded documents, the static site generator [Jekyll](https://jekyllrb.com/), and the JavaScript library [CETEIcean](https://www.github.com/TEIC/CETEIcean) to publish standards-compliant editions via a minimal computing method. Critically, the project includes detailed documentation for setting up and customizing the platform, as well as an undergraduate-level syllabus for a course on digital editions. 

Gertrude is named after Gertrude Jekyll, a garden designer of the Arts and Crafts movement. Like gardening, the process of creating a digital edition is slow, iterative, and privileges maintenance over innovation. 

</div>
<div class="col-md-6">
<div class="card" style="max-width: 600px;">
  <div class="row g-0">
    <div class="col-md-4"><a href="">
      <img src="assets/img/jekyll-morell.png" class="img-fluid rounded-start" alt="..."></a>
    </div>
    <div class="col-md-8">
      <div class="card-body"><a href="">
        <h3 class="card-title">Gertrude Documentation</h3></a>
        <p class="card-text">In-depth documentation on setting up and using this platform is available on the Gertrude documentation site.</p>
      </div>
    </div>
  </div>
</div></div>


</div>


<!-- The card feature works by creating a variable called 'featured' consisting of pages that have featured: true in the YAML metadata. For each page that matches those conditions, a Bootstrap card is created and info from the page is filled in. --> 

<div class="row">
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