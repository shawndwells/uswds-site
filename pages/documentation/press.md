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
<div class="usa-table--stacked">
  <table class="usa-table usa-table--borderless">
    <caption>Televised interviews from national and local outlets.</caption>
    <thead>
      <tr>
        <th data-sortable scope="col" role="columnheader" class="text-center">
          Date<br/>(yyyy-mm-dd)
        </th>
        <th data-sortable scope="col" role="columnheader">
          Outlet
        </th>
        <th role="columnheader">
          Title
        </th>
        <th role="columnheader">
          Description
        </th>
      </tr>
    </thead>
    <tbody>
      {% assign articles = site.data.press | sort:"published" | reverse %}
      {% for article in articles %}
      {% if article.type == "tv" %}
      <tr>
        <th class="text-center" data-sort-value="{{ article.published }}">
          <span style="display: inline-block; width: 7em;">{{ article.published }}</span>
        </th>
        <td class="text-left" data-sort-value="{{ article.outlet }}">
          {{ article.outlet }}
        </td>
        <td class="text-tabular text-left"><a href="{{ article.url }}">{{ article.title }}</a></td>
        <td class="text-tabular text-left">{{ article.description }}</td>
        
      </tr>
      {% endif %}
      {% endfor %} 
    </tbody>
  </table>
  <div class="usa-sr-only usa-table__announcement-region" aria-live="polite"></div>
</div>

## Radio & Podcasts
<div class="usa-table--stacked">
  <table class="usa-table usa-table--borderless">
    <caption>National radio and major podcast interviews.</caption>
    <thead>
      <tr>
        <th data-sortable scope="col" role="columnheader" class="text-center">
          Date<br/>(yyyy-mm-dd)
        </th>
        <th data-sortable scope="col" role="columnheader">
          Outlet
        </th>
        <th role="columnheader">
          Title
        </th>
        <th role="columnheader">
          Description
        </th>
      </tr>
    </thead>
    <tbody>
      {% assign articles = site.data.press | sort:"published" | reverse %}
      {% for article in articles %}
      {% if article.type == "radio" %}
      <tr>
        <th class="text-center" data-sort-value="{{ article.published }}">
          <span style="display: inline-block; width: 7em;">{{ article.published }}</span>
        </th>
        <td class="text-left" data-sort-value="{{ article.outlet }}">
          {{ article.outlet }}
        </td>
        <td class="text-tabular text-left"><a href="{{ article.url }}">{{ article.title }}</a></td>
        <td class="text-tabular text-left">{{ article.description }}</td>
        
      </tr>
      {% endif %}
      {% endfor %} 
    </tbody>
  </table>
  <div class="usa-sr-only usa-table__announcement-region" aria-live="polite"></div>
</div>

## Press

<div class="usa-table--stacked">
  <table class="usa-table usa-table--borderless">
    <caption>Press interviews and authored articles.</caption>
    <thead>
      <tr>
        <th data-sortable scope="col" role="columnheader" class="text-center">
          Date<br/>(yyyy-mm-dd)
        </th>
        <th data-sortable scope="col" role="columnheader">
          Outlet
        </th>
        <th role="columnheader">
          Title
        </th>
        <th role="columnheader">
          Description
        </th>
      </tr>
    </thead>
    <tbody>
      {% assign articles = site.data.press | sort:"published" | reverse %}
      {% for article in articles %}
      {% if article.type == "press" %}
      <tr>
        <th class="text-center" data-sort-value="{{ article.published }}">
          <span style="display: inline-block; width: 7em;">{{ article.published }}</span>
        </th>
        <td class="text-left" data-sort-value="{{ article.outlet }}">
          {{ article.outlet }}
        </td>
        <td class="text-tabular text-left"><a href="{{ article.url }}">{{ article.title }}</a></td>
        <td class="text-tabular text-left">{{ article.description }}</td>
        
      </tr>
      {% endif %}
      {% endfor %} 
    </tbody>
  </table>
  <div class="usa-sr-only usa-table__announcement-region" aria-live="polite"></div>
</div>
      
