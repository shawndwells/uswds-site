---
component:
  status: ready
  package: usa-table
  dependencies:
  variant: scrollable
guidancePath: guidance/variants/scrollable
layout: styleguide
lead: Examined emerging technologies, policies, economics, finance, management, and behavioral science that will transform how we obtain, distribute, store, and use energy.
order: 02
parent: Table
title: Stanford
---
<table class="usa-table usa-table--borderless usa-table--striped">
  <caption>Borderless table with horizontal stripes</caption>
  <thead>
    <tr>
      <th scope="col">Course Code</th>
      <th scope="col">Course Name</th>
      <th scope="col">Credits</th>
    </tr>
  </thead>
  <tbody>
  {% for class in site.data.stanford-energy %}
      <tr>
      <th scope="row"><center>{{ class.code }}</center></th>
      <td>{{ class.title }}</td>
      <td><center>{{ class.credits }}</center></td>
    </tr>
  {% endfor %}
  </tbody>
</table>
<!--{% include component-preview-and-code.html level="h3" %}-->
