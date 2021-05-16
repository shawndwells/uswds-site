---
permalink: /academics/
layout: styleguide
title: Academics
category: How to use USWDS
lead: school stuffs.
---

## Get started with USWDS

<div class="grid-row grid-gap flex-align-stretch margin-top-4">
  <div class="tablet:grid-col display-flex flex-align-stretch">
    <div class="site-docs-card-link">
      <h3 class="font-lang-lg margin-0">
        <a href="{{ site.baseurl }}/getting-started/developers/" class="text-no-underline text-primary hover:text-underline block-link">Post Graduate</a>
      </h3>
      <p class="margin-top-1">postgrad certs.</p>
    </div>
  </div>
  <div class="margin-top-2 tablet:margin-top-0 tablet:grid-col display-flex flex-align-stretch">
    <div class="site-docs-card-link">
      <h3 class="font-lang-lg margin-0">
        <a href="{{ site.baseurl }}/getting-started/designers/" class="text-no-underline text-primary hover:text-underline block-link">Undergraduate</a>
      </h3>
      <p class="margin-top-1">basic.</p>
    </div>
  </div>
  <div class="tablet:grid-col margin-top-2 tablet:margin-top-0 display-flex flex-align-stretch">
    <div class="site-docs-card-link">
      <h3 class="font-lang-lg margin-0">
        <a href="https://github.com/uswds/uswds/wiki" class="block-link text-no-underline text-primary hover:text-underline">Industry Certifications</a>
      </h3>
      <p class="margin-top-1">dem certs.</p>
    </div>
  </div>
</div>

{:.border-top-05.border-primary.padding-top-3.margin-top-6}

## Post Graduate
<p>sample text</p><br/>
<ul class="usa-card-group">
{% for degree in site.data.postgrad %}
{% assign tags = component.tags | join: " " %}
  <li class="tablet:grid-col-6 usa-card usa-card--flag">
    <div class="usa-card__container">
      <header class="usa-card__header">
        <h2 class="usa-card__heading">{{ degree.degreeName }}</h2>
      </header>
      <div class="usa-card__media">
        <div >
          <center>
            <img src="{{ site.baseurl }}/{{ degree.schoolLogo }}" alt="{{degree.schoolName }} Logo">
          </center>
        </div>
      </div>
      <div class="usa-card__body">
        <p>{{degree.degreeDescr | markdownify }}</p>
      </div>
      <div class="usa-card__footer">
        <button class="usa-button">Details</button>
      </div>
    </div>
  </li>
{% endfor %}
</ul>


{:.border-top-05.border-primary.padding-top-3.margin-top-6}

## Undergraduate
<p>sample text</p><br/>
<ul class="usa-card-group">
{% for degree in site.data.undergrad %}
{% assign tags = component.tags | join: " " %}
  <li class="tablet:grid-col-6 usa-card usa-card--flag">
    <div class="usa-card__container">
      <header class="usa-card__header">
        <h2 class="usa-card__heading">{{ degree.degreeName }}</h2>
      </header>
      <div class="usa-card__media">
        <div >
          <center>
            <img src="{{ site.baseurl }}/{{ degree.schoolLogo }}" alt="{{degree.schoolName }} Logo">
          </center>
        </div>
      </div>
      <div class="usa-card__body">
        <p>{{degree.degreeDescr | markdownify }}</p>
      </div>
      <div class="usa-card__footer">
        <button class="usa-button">Details</button>
      </div>
    </div>
  </li>
{% endfor %}
</ul>


{:.border-top-05.border-primary.padding-top-3.margin-top-6}

## Industry Certifications

<ul class="usa-card-group">
{% for cert in site.data.certifications %}
{% assign tags = component.tags | join: " " %}
  <li class="tablet:grid-col-6 usa-card usa-card--flag">
    <div class="usa-card__container">
      <header class="usa-card__header">
        <h2 class="usa-card__heading">{{ cert.certName }}</h2>
      </header>
      <div class="usa-card__media">
        <div >
          <center>
            <img src="{{ site.baseurl }}/{{ cert.certLogo }}" alt="{{cert.certName }} Logo">
          </center>
        </div>
      </div>
      <div class="usa-card__body">
        <p>{{ cert.certDescription | markdownify }}</p>
        <p>Certification ID: <a href="{{ cert.certVerificationURL }}" target="_blank">{{ cert.certNumber }}</a></p>
      </div>
      <div class="usa-card__footer">
        <button class="usa-button">Details</button>
      </div>
    </div>
  </li>
{% endfor %}
</ul>