---
title: "InspiringGroup - Publications"
layout: gridlay
excerpt: "InspiringGroup -- Publications."
sitemap: false
permalink: /publications/
---

## Publications

### Group highlights

<div class="largefont">
(For a full list go to [Google Scholar](https://scholar.google.com/citations?user=F8gi4rcAAAAJ&hl=en) or see a selected list [below](#selected-publications))
</div>

{% assign number_printed = 0 %}
{% for publi in site.data.projects %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit class="largefont">{{ publi.name }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="90%" style="float:right;margin-bottom:18px;" />

  <ul style="overflow: hidden">
	{% if publi.number_desc == 1 %}   
	<li> {{ publi.desc1}} </li> 
	{% endif %}                        

	{% if publi.number_desc == 2 %}   
	<li> {{ publi.desc1}} </li> 
	<li> {{ publi.desc2}} </li> 
	{% endif %}                        

	{% if publi.number_desc == 3 %}   
	<li> {{ publi.desc1}} </li> 
	<li> {{ publi.desc2}} </li> 
	<li> {{ publi.desc3}} </li> 
	{% endif %}                        

	{% if publi.number_desc == 4 %}   
	<li> {{ publi.desc1}} </li> 
	<li> {{ publi.desc2}} </li> 
	<li> {{ publi.desc3}} </li> 
	<li> {{ publi.desc4}} </li> 
	{% endif %}                        
  </ul>
 </div>
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

---

### Selected Publications

{% for publi in site.data.publist %}

  <b>{{ publi.title }}</b><br />
  <em>{{ publi.authors }} </em><br />
  {{publi.conference}}<br />
  {%- if publi.pdf != nil -%}
  <a href="{{ publi.pdf }}">[pdf]</a>
  {% endif %}
  {%- if publi.doi != nil -%}
  <a href="{{ publi.doi }}">[doi]</a>
  {% endif %}
  {%- if publi.slides != nil -%}
  <a href="{{ publi.slides }}">[slides]</a>
  {% endif %}
  {%- if publi.codes != nil -%}
  <a href="{{ publi.codes }}">[codes]</a>
  {% endif %}
  {%- if publi.patent != nil -%}
  <a href="{{ publi.patent }}">[patent]</a>
  {% endif %}

<a href="{{ publi.link.url }}">{{ publi.link.display }}</a>
{% endfor %}
<br />
