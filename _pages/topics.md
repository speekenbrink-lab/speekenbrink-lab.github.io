---
title: "Speekenbrink lab - Topics"
layout: default
excerpt: "Speekenbrink lab: Topics"
sitemap: false
permalink: /topics/
---

# Our research

The goal of our research is to understand the learning and decision processes which allow humans to function effectively in an uncertain and dynamic world. By developing computational models and assessing how they compare to human behaviour in experimental tasks, we hope to gain deeper insight into how information is processed and represented during learning and decision making.

<hr>

<p></p>

{% assign filtered_topics = site.researchtopics | where: 'current', 1 %}
{% for topic in filtered_topics %}
{% assign mod = forloop.index | modulo: 3 %}
{% if mod == 0 %}
<!-- last column -->
<div class="col4 col-sm-4 col-lg-4">
<h2>{{ topic.title }}</h2>
<p>{{ topic.blurb }}</p>
{% if topic.image %}
<img src="{{site.url}}{{site.baseurl}}/images/research/{{ topic.image }}" class="img-responsive" width="100%">
{% endif %}
<a href="{{ topic.url }}" class="btn btn-default">Read more</a>
</div>
</div>
{% elsif mod == 2 %}
<!-- middle column -->
<div class="col4 col-sm-4 col-lg-4">
<h2>{{ topic.title }}</h2>
<p>{{ topic.blurb }}</p>
{% if topic.image %}
<img src="{{site.url}}{{site.baseurl}}/images/research/{{ topic.image }}" class="img-responsive" width="100%">
{% endif %}
<a href="{{ topic.url }}" class="btn btn-default">Read more</a>
</div>
{% if forloop.last %}
</div>
{% endif %}
{% else %}
<!-- first column -->
<div class="row">
<div class="col4 col-sm-4 col-lg-4">
<h2>{{ topic.title }}</h2>
<p>{{ topic.blurb }}</p>
{% if topic.image %}
<img src="{{site.url}}{{site.baseurl}}/images/research/{{ topic.image }}" class="img-responsive" width="100%">
{% endif %}
<a href="{{ topic.url }}" class="btn btn-default">Read more</a>
{% if forloop.last %}
</div>
{% endif %}
</div>
{% endif %}
{% endfor %}
