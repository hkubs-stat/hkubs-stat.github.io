---
title: "Stat Group - Students and Postdocs"
layout: gridlay
excerpt: "Stat Group: Students and Postdocs"
sitemap: false
permalink: /students_and_postdocs/
---

## Prospective PhD Students

Our statistics (Business Analystics) group has multiple positions for PhD students, Research Assistants, and Postdocs. If you are interested in our Ph.D. program, please see [here](https://fbeo.fbe.hku.hk/phd/admissions/admission-application-and-tuition-fee/) for how to apply, application deadlines. The HKU Business School is organising a three-day face-to-face Recruitment Camp, please see [here](https://fbeo.fbe.hku.hk/phd/admissions/recruitment-camp). If you are interested, self-motivated, and have background in statistics, applied mathematics, or computer science, please send me an email to (dyanghku@hku.hk) with your CV, transcripts, and a short description of your research interests. 

## Current PhD Students
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden"> </ul>
  <ul> {{ member.email }} </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


