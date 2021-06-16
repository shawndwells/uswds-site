---
permalink: /presentationa/
layout: styleguide
title: Presentations
category: How to use USWDS
lead: i speka
---

<div class="usa-table-container--scrollable">
  <table class="usa-table usa-table--borderless">
    <caption>Sortable borderless table with various content types</caption>
    <thead>
      <tr>
        <th data-sortable scope="col" role="columnheader">
          Date
        </th>
        <th data-sortable scope="col" role="columnheader">
          Event / Session Name
        </th>
        <th data-sortable scope="col" role="columnheader">
          Title / Topic
        </th>
        <th scope="col" role="columnheader">
          Abstract
        </th>
        <th scope="col" role="columnheader">
          Download
        </th>
      </tr>
    </thead>
    <tbody>
    {% for presentation in site.data.presentations %}
      <tr>
        <th data-sort-value="{{ presentation.sessionDate }}" scope="row" class="font-mono-sm text-tabular text-left">{{ presentation.sessionDate }}</th>
        <td data-sort-value="{{ presentation.sessionName }}" class="font-mono-sm text-tabular text-left">{{ presentation.sessionName }}</td>
        <td data-sort-value="{{ presentation.eventName }}" class="font-mono-sm text-tabular text-left">{{ presentation.eventName }}</td>
        <td data-sort-value="{{ presentation.sessionAbstract | markdownify }}" class="font-mono-sm text-left">{{ presentation.sessionAbstract | markdownify }}</td>
        <td data-sort-value="PDF" class="font-mono-sm text-tabular text-right"><a href="{{ presentation.downloadPDF }}">PDF</a></td>
      </tr>
    {% endfor %}
    </tbody>
  </table>
  <div class="usa-sr-only usa-table__announcement-region" aria-live="polite"></div>
</div>