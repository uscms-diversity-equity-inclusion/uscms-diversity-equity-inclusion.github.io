---
layout: people
title: About
permalink: /about/contact.html
---


# Email Contact

[uscms-dei@cern.ch](mailto:uscms-dei@cern.ch)

{% assign members = site.data.people | values
                                     | where_exp:"item", "item.active and item.hidden != true"
                                     | sort: "title"
                                     | last_name_sort: "name" %}

{% assign past_members = site.data.people | values
                                          | where_exp:"item", "item.active == false and item.hidden != true"
                                          | sort: "title"
                                          | last_name_sort: "name" %}

# Present Members

<div class="container-fluid">
<div class="row">
{% for person in members %}
    {% include standard_person_card.md person=person %}
{% endfor %}
</div>
</div>

{% if past_members.size > 0 %}
<br>
<hr>
<br> 
# Past Members

<div class="container-fluid">
<div class="row">
    {% for person in past_members %}
        {% include standard_person_card.md person=person %}
    {% endfor %}
</div>
</div>
{% endif %}