---
title: "Speekenbrink lab - Publications"
layout: default
excerpt: "Speekenbrink lab - Publications"
sitemap: false
permalink: /publications/
---

{% assign years_pubs = site.data.publications | group_by: 'year' | sort: 'name' | reverse %}
<div class="row">
<div class="col12 col-sm-12 col-lg-12">
<h2>Working papers</h2>
{% for year in years_pubs %}
{% assign sorted_pubs = year.items | sort: 'apa_reference' %}
{% for pub in sorted_pubs %}
{% if pub.type == 'preprint' %}
<a name="{{pub.tag}}"></a>{{ pub.apa_reference }} {% include publicationlinks.html %}
{% endif %}
{% endfor %}
{% endfor %}
</div>
</div>

{% for year in years_pubs %}
<div class="row">
<div class="col12 col-sm-12 col-lg-12">
<h2>{{ year.name }}</h2>
{% assign sorted_pubs = year.items | sort: 'apa_reference' %}
{% for pub in sorted_pubs %}
{% if pub.type != 'preprint' %}
<a name="{{pub.tag}}"></a>{{ pub.apa_reference }} {% include publicationlinks.html %}
{% endif %}
{% endfor %}
</div>
</div>
{% endfor %}
