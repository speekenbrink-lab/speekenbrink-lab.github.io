---
title: "Speekenbrink lab - People"
layout: default
excerpt: "Speekenbrink lab: Team members"
sitemap: false
permalink: /people/
---

# Current lab members

{% assign by_current_members = site.data.people | group_by: 'current' %}
{% for current_item in by_current_members %}
{% if current_item.name == '1' %}
{% assign position_members = current_item.items | group_by: 'position' %}
{% for position in position_members %}
{% if position.name != 'collaborator' %}
{% assign members = position.items %}
{% for  member in  members %}
<div class="row">
<hr style="width: 100%; color: black; height: 10px; padding:2px;" />
<div class="col2 col-sm-2 col-lg-2">
{% if member.photo %}<img src="{{ site.url }}{{ site.baseurl }}/images/people/{{ member.photo }}" width="80%" />{% endif %}
</div>
<div class="col10 col-sm-10 col-lg-10">
<h3>{{member.name}}</h3>
<h4>{{member.position}}</h4>
<p>{{member.blurb}}</p>
{% include personlinks.html %}
</div>
</div>
{% endfor %}
{% endif %}
{% endfor %}
{% endif %}
{% endfor %}

# Lab alumni


{% assign by_current_members = site.data.people | group_by: 'current' %}
{% for current_item in by_current_members %}
{% if current_item.name == '0' %}
{% assign position_members = current_item.items | group_by: 'position' %}
{% for position in position_members %}
{% if position.name == 'PhD student' or position.name == 'Visiting PhD student' %}
{% assign members = position.items %}
{% for  member in  members %}
<div class="row">
<hr style="width: 100%; color: black; height: 10px; padding:2px;" />
<div class="col10 col-sm-10 col-lg-10">
<h3>{{member.name}}</h3>
<h4>{{member.position}} ({{member.start_year}} - {{member.end_year}})</h4>
<p>{{member.movingon_blurb}}</p>
{% include personlinks.html %}
</div>
<div class="col2 col-sm-2 col-lg-2">
{% if member.photo %}<img src="{{ site.url }}{{ site.baseurl }}/images/people/{{ member.photo }}" width="80%" />{% endif %}
</div>
</div>
{% endfor %}
{% endif %}
{% endfor %}
{% endif %}
{% endfor %}


<div class="row">
<hr style="width: 100%; color: black; height: 10px; padding:2px;" />
<div class="col6 col-sm-6 col-lg-6">
{% assign by_current_members = site.data.people | group_by: 'current' %}
{% for current_item in by_current_members %}
{% if current_item.name == '0' %}
{% assign position_members = current_item.items | group_by: 'position' %}
{% for position in position_members %}
{% if position.name == 'MSc student' %}
{% assign year_members = position.items | sort: 'end_year' | reverse | group_by: 'end_year' %}
{% for year in year_members %}
{% assign members = year.items | sort: 'name' %}
{% for member in members %}
<h4>{{member.name}} ({{ member.start_year }}-{{ member.end_year }}, {{ member.position}})</h4>
<p>{{member.movingon_blurb}}</p>
{% endfor %}
{% endfor %}
{% endif %}
{% endfor %}
{% endif %}
{% endfor %}
</div>

<div class="col6 col-sm-6 col-lg-6">
{% assign by_current_members = site.data.people | group_by: 'current' %}
{% for current_item in by_current_members %}
{% if current_item.name == '0' %}
{% assign position_members = current_item.items | group_by: 'position' %}
{% for position in position_members %}
{% if position.name == 'BSc student' %}
{% assign year_members = position.items | sort: 'end_year' | reverse | group_by: 'end_year' %}
{% for year in year_members %}
{% assign members = year.items | sort: 'name' %}
{% for member in members %}
<h4>{{member.name}} ({{ member.start_year }}-{{ member.end_year }}, {{ member.position}})</h4>
<p>{{member.movingon_blurb}}</p>
{% endfor %}
{% endfor %}
{% endif %}
{% endfor %}
{% endif %}
{% endfor %}</div>

</div>

# Collaborators

<div class="row">

<div class="col6 col-sm-6 col-lg-6">
{% assign by_current_members = site.data.people | group_by: 'current' %}
{% for current_item in by_current_members %}
{% if current_item.name == '1' %}
{% assign position_members = current_item.items | group_by: 'position' %}
{% for position in position_members %}
{% if position.name == 'collaborator' %}
{% assign members = position.items | sort: 'name' %}
{% for member in members %}
<a href="{{member.url}}">{{member.name}} ({{ member.organization }})</a><br />
{% endfor %}
{% endif %}
{% endfor %}
{% endif %}
{% endfor %}
</div>



<div class="col6 col-sm-6 col-lg-6">
{% assign by_current_members = site.data.people | group_by: 'current' %}
{% for current_item in by_current_members %}
{% if current_item.name == '0' %}
{% assign position_members = current_item.items | group_by: 'position' %}
{% for position in position_members %}
{% if position.name == 'collaborator' %}
{% assign members = position.items | sort: 'name' %}
{% for member in members %}
<a href="{{member.url}}">{{member.name}} ({{ member.organization }})</a><br />
{% endfor %}
{% endif %}
{% endfor %}
{% endif %}
{% endfor %}

</div>

</div>
