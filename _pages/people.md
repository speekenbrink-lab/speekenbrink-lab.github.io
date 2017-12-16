---
title: "Speekenbrink lab - People"
layout: default
excerpt: "Speekenbrink lab: Team members"
sitemap: false
permalink: /people/
---

# Current lab members

{% for member in site.data.people %}
{% if member[1].current == 1 and member[1].position != "collaborator"%}
<div class="row">
<hr style="width: 100%; color: black; height: 10px; padding:2px;" />
<div class="col2 col-sm-2 col-lg-2">
{% if member[1].photo %}<img src="{{ site.url }}{{ site.baseurl }}/images/people/{{ member[1].photo }}" width="80%" />{% endif %}
</div>
<div class="col10 col-sm-10 col-lg-10">
<h3>{{member[1].name}}</h3>
<h4>{{member[1].position}}</h4>
<p>{{member[1].blurb}}</p>
{% include personlinks.html %}
</div>
</div>
{% endif %}
{% endfor %}


# Lab alumni

{% for member in site.data.people %}
{% if member[1].current == 0 %}
{% if member[1].position == "PhD student" or member[1].position == "Visiting PhD student" %}
<div class="row">
<hr style="width: 100%; color: black; height: 10px; padding:2px;" />
<div class="col10 col-sm-10 col-lg-10">
<h3>{{member[1].name}}</h3>
<h4>{{member[1].position}} ({{member[1].start_year}} - {{member[1].end_year}})</h4>
<p>{{member[1].movingon_blurb}}</p>
{% include personlinks.html %}
</div>
<div class="col2 col-sm-2 col-lg-2">
{% if member[1].photo %}<img src="{{ site.url }}{{ site.baseurl }}/images/people/{{ member[1].photo }}" width="80%" />{% endif %}
</div>
</div>
{% endif %}
{% endif %}
{% endfor %}

<div class="row">
<hr style="width: 100%; color: black; height: 10px; padding:2px;" />
<div class="col6 col-sm-6 col-lg-6">
{% for member in site.data.people %}
{% if member[1].current == 0 %}
{% if member[1].position == "MSc student" %}
<h4>{{member[1].name}} ({{ member[1].start_year }}-{{ member[1].end_year }}, {{ member[1].position}})</h4>
<p>{{member[1].movingon_blurb}}</p>
{% endif %}
{% endif %}
{% endfor %}
</div>

<div class="col6 col-sm-6 col-lg-6">
{% for member in site.data.people %}
{% if member[1].current == 0 %}
{% if member[1].position == "BSc student" %}
<h4>{{member[1].name}} ({{ member[1].start_year }}-{{ member[1].end_year }}, {{ member[1].position}})</h4>
{% endif %}
{% endif %}
{% endfor %}
</div>
</div>

# Collaborators

<div class="row">

<div class="col6 col-sm-6 col-lg-6">
{% for member in site.data.people %}
{% if member[1].position == "collaborator" %}
{% if member[1].current == 1 %}
<a href="{{member[1].url}}">{{member[1].name}} ({{ member[1].organization }})</a><br />
{% endif %}
{% endif %}
{% endfor %}
</div>

<div class="col6 col-sm-6 col-lg-6">
{% for member in site.data.people %}
{% if member[1].position == "collaborator" %}
{% if member[1].current == 0 %}
<a href="{{member[1].url}}">{{member[1].name}} ({{ member[1].organization }})</a><br />
{% endif %}
{% endif %}
{% endfor %}
</div>

</div>
