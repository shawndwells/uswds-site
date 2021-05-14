---
component:
  status: ready
  package: usa-table
  dependencies:
  variant: borderless
guidancePath: guidance/variants/default
layout: styleguide
lead: Something harvard.
order: 01
parent: Table
title: Harvard
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
  {% for class in site.data.wgu %}
      <tr>
      <th scope="row"><center>{{ class.code }}</center></th>
      <td>{{ class.title }}</td>
      <td><center>{{ class.credits }}</center></td>
    </tr>
  {% endfor %}
  </tbody>
</table>
<!--{% include component-preview-and-code.html level="h3" %}-->
