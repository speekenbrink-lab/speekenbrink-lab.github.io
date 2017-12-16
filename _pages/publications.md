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
{{ pub.apa_reference }} {% if pub.doi %}<a href="https://doi.org/{{ pub.doi }}"><i class="ai ai-doi ai-1x"></i></a>{% endif %}{% if pub.arxiv %}<a href="{{ pub.arxiv }}"><i class="ai ai-arxiv ai-1x"></i></a>{% endif %}{% if pub[1].osf %}<a href="https://osf.io/{{ pub.osf }}"><i class="ai ai-osf ai-1x"></i></a>{% endif %}
{% endfor %}
</div>
</div>
{% endfor %}
