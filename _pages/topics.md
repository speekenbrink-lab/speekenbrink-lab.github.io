---
title: "Speekenbrink lab - Topics"
layout: default
excerpt: "Speekenbrink lab: Topics"
sitemap: false
permalink: /topics/
---

{% for topic in site.data.topics %}
{% if topic.current == 1 %}

## {{topic.name}}

_{{topic.blurb}}_

<div class="row">
{% capture thecycle %}{% cycle 'odd', 'even' %}{% endcapture %}
{% if thecycle == 'odd' %}
<div class="col4 col-sm-4 col-lg-4">
{% if topic.image %}<img src="{{ site.url }}{{ site.baseurl }}/images/research/{{ topic.image }}" width="80%" align="left" />{% endif %}
</div>
{% endif %}

<div class="col8 col-sm-8 col-lg-8">




{{topic.description}}

</div>

{% if thecycle == 'even' %}
<div class="col4 col-sm-4 col-lg-4">
{% if topic.image %}<img src="{{ site.url }}{{ site.baseurl }}/images/research/{{ topic.image }}" width="80%" align="right" />{% endif %}
</div>
{% endif %}

</div>
{% endif %}
{% endfor %}
