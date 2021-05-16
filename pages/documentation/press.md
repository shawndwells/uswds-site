---
permalink: /press-and-media/
layout: styleguide
title: Press and Media
category: How to use USWDS
lead: Media coverage
---

Opening paragraph TBD.

 <div>
  <h3 class="site-preview-heading tablet:margin-top-0">Media thumbnail</h3>
  <ul class="usa-collection">
{% for article in site.data.press %}
    <li class="usa-collection__item">
      <img class="usa-collection__img" src="{{ site.baseurl }}/{{ article.img }}" alt="Article Logo">
      <div class="usa-collection__body">
        <h3 class="usa-collection__heading">
          <a class="usa-link" href="{{ article.url }}">{{ article.title }}</a>
        </h3>
        <p class="usa-collection__description">{{ article.description }}</p>
        <ul class="usa-collection__meta" aria-label="More information">
          <li class="usa-collection__meta-item">By {{ article.author }}</li>
          <li class="usa-collection__meta-item"><time datetime="2019-11-12T12:00:00+01:00">{{ article.published }}</time></li>
        </ul>
      </div>
    </li>
{% endfor %} 
  </ul> 
</div>

      
