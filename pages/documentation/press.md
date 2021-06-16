---
permalink: /press-and-media/
layout: styleguide
title: Press and Media
#category: Curriculum Vitae
category: Press and Media
lead: Media coverage including televised interviews, radio shows, press coverage, and authored articles.
type: docs
subnav:
  - text: Television
    href: '#television'
  - text: Radio & Podcasts
    href: '#radio-podcasts'
  - text: Press
    href: '#press'
---

## Television
...

## Radio & Podcasts
...

## Press

<div class="usa-table--stacked">
  <table class="usa-table usa-table--borderless">
    <caption>Press interviews and authored articles.</caption>
    <thead>
      <tr>
        <th data-sortable scope="col" role="columnheader" class="text-center">
          Date<br/>(yyyy-mm-dd)
        </th>
        <th role="columnheader">
          Title
        </th>
        <th role="columnheader">
          Description
        </th>
        <th data-sortable scope="col" role="columnheader">
          Outlet
        </th>
      </tr>
    </thead>
    <tbody>
      {% for article in site.data.press %}
      <tr>
        <th class="text-center" data-sort-value="{{ article.published }}">
          <span style="display: inline-block; width: 7em;">{{ article.published }}</span>
        </th>
        <td class="text-tabular text-left"><a href="{{ article.url }}">{{ article.title }}</a></td>
        <td class="text-tabular text-left">{{ article.description }}</td>
        <td class="text-left" data-sort-value="{{ article.outlet }}">
          {{ article.outlet }}
        </td>
      </tr>
      {% endfor %} 
    </tbody>
  </table>
  <div class="usa-sr-only usa-table__announcement-region" aria-live="polite"></div>
</div>

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

      
