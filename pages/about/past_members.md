---
layout: people
title: Past members
permalink: /about/past_members.html
---

{% assign past_members = site.data.people | values
                                          | where_exp:"item", "item.active == false and item.hidden != true"
                                          | sort: "title"
                                          | last_name_sort: "name" %}


# Past Members

<div class="container-fluid">
<div class="row">
    {% for person in past_members %}
        {% include standard_person_card.md person=person %}
    {% endfor %}
</div>
</div>
