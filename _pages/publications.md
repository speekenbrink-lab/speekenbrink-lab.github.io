---
title: "Speekenbrink lab - Publications"
layout: default
excerpt: "Speekenbrink lab - Publications"
sitemap: false
permalink: /publications/
---

{% assign years_pubs = site.data.publications | group_by: 'year' | sort: 'name' | reverse %}
{% for year in years_pubs %}
<div class="row">
<div class="col12 col-sm-12 col-lg-12">
<h2>{{ year.name }}</h2>
{% assign sorted_pubs = year.items | sort: 'apa_reference' %}
{% for pub in sorted_pubs %}
<a name="{{pub.tag}}"></a>{{ pub.apa_reference }} {% include publicationlinks.html %}
{% endfor %}
</div>
</div>
{% endfor %}
