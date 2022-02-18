---
layout: people
title: About
permalink: /about/contact.html
---

<h1>Email Contact</h1>

uscms-dei@cern.ch


{% assign members = site.data.people | values
                                     | where_exp:"item", "item.active and item.hidden != true"
                                     | sort: "title"
                                     | last_name_sort: "name" %}


<h1>Full Team</h1><br>

<div class="container-fluid">
<div class="row">
{% for person in members %}
    {% include standard_person_card.md person=person %}
{% endfor %}
</div>
</div>
