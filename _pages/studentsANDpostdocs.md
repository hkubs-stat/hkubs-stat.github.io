---
title: "Stat Group - Students and Postdocs"
layout: gridlay
excerpt: "Stat Group: Students and Postdocs"
sitemap: false
permalink: /students_and_postdocs/
---

## Prospective PhD Students

<div style="text-align: justify">
Our statistics (Business Analytics) group has multiple positions for PhD students, Research Assistants, and Postdocs. If you are interested, self-motivated, and have background in statistics, applied mathematics, or computer science, please send an email to our faculty members with your CV, transcripts, and a short description of your research interests. For our Ph.D. program, more details can be found [here](https://fbeo.fbe.hku.hk/phd/). For the three-day face-to-face Ph.D. Recruitment Camp in our faculty, more details can be found [here](https://fbeo.fbe.hku.hk/phd/admissions/recruitment-camp). 
</div>

## Current PhD Students
{% assign number_printed = 0 %}
{% for member in site.data.students %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

{% if number_printed < 7 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <h5> {{ member.email }} </h5>
</div>
{% endif %}

{% if number_printed >= 7 %}
<div class="col-sm-6 clearfix">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} </i>
  <h5> {{ member.email }} </h5>
</div>
{% endif %}

{% if number_printed == 7 %}
</div>
<div class="row">
{% endif %}

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


## Current Postdocs
{% assign number_printed = 0 %}
{% for member in site.data.postdocs %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <h5> {{ member.email }} </h5>
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

## Previous Students
{% assign number_printed = 0 %}
{% for member in site.data.previous_student %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden"> </ul>
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