---
permalink: /academics-and-certifications/
layout: styleguide
title: Academics and Certifications
category: Academics and Certifications
lead: Some language about continuing education. 
type: docs
subnav:
  - text: Postgraduate
    href: '#postgraduate'
  - text: Undergraduate
    href: '#undergraduate'
  - text: Industry Certifications
    href: '#industry-certifications'
---

{% assign postgradCredentials = site.data.postgrad %}
{% assign undergradCretentials = site.data.undergrad %}
{% assign industryCertifications = site.data.certifications %}


<div class="grid-row grid-gap flex-align-stretch margin-top-4">
  <div class="tablet:grid-col display-flex flex-align-stretch">
    <div class="site-docs-card-link">
      <h3 class="font-lang-lg margin-0">
        <a href="{{ site.baseurl }}/academics/#postgraduate" class="text-no-underline text-primary hover:text-underline block-link">
        Postgraduate</a>
      </h3>
      <p class="margin-top-1"><strong>{{ postgradCredentials.size }}</strong> postgraduate academic credentials.</p>
    </div>
  </div>
  <div class="margin-top-2 tablet:margin-top-0 tablet:grid-col display-flex flex-align-stretch">
    <div class="site-docs-card-link">
      <h3 class="font-lang-lg margin-0">
        <a href="{{ site.baseurl }}/academics/#undergraduate/" class="text-no-underline text-primary hover:text-underline block-link">Undergraduate</a>
      </h3>
      <p class="margin-top-1"><strong>{{ undergradCretentials.size }}</strong> undergraduate academic credentials.</p>
    </div>
  </div>
  <div class="tablet:grid-col margin-top-2 tablet:margin-top-0 display-flex flex-align-stretch">
    <div class="site-docs-card-link">
      <h3 class="font-lang-lg margin-0">
        <a href="{{ site.baseurl }}/academics/#industry-certifications/" class="block-link text-no-underline text-primary hover:text-underline">Industry Certifications</a>
      </h3>
      <p class="margin-top-1"><strong>{{ industryCertifications.size }}</strong> actively maintained industry certifications.</p>
    </div>
  </div>
</div>

{:.border-top-05.border-primary.padding-top-3.margin-top-6}

## Postgraduate
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