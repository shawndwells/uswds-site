---
category: Components
component:
  status: ready
  package: usa-collection
  dependencies:
layout: component
lead: A collection displays a compact list of multiple related items like articles or events. The list links each item to its original source.
permalink: /components/collection/
redirect_from:
- /collection/
- /components/collections/
subnav:
- text: Preview
  href: '#collection-preview'
- text: Code
  href: '#collection-code'
- text: Guidance
  href: '#collection-guidance'
- text: Package
  href: '#collection-package'
title: Collection
type: component
variants:
  - variant: "`usa-collection--condensed`"
    description: A more condensed item presentation with less space between items.
---

The collection component offers users a way to view short descriptions of related content, providing a simple way to access the original source to learn more. It’s useful when you want to highlight information like articles, events, or documents that appear elsewhere on your website or from other sources.

Each item in the collection includes a headline that links to another page and (optionally) a small image, descriptive text, and metadata such as date, time, byline, and tags.

Items in a collection should be related. This could be by publication date (for instance, all the content was posted in the last week), by content type (all articles, events, or blog posts), or by subject (all items relate to the same topic or theme). Be selective about what content you show in each collection. Consider limiting the number of items in each collection to six or fewer.

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

      
