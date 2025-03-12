---
layout: people
title: About
permalink: contact.html
---


# Link to the anonymous mail box - (mail goes to only USCMS chair/deputy)

# Click [here] (https://uscms-anonymous-box.web.cern.ch/)for anonymous mail box (mail goes to only USCMS chair/deputy)(requires CERN login)


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

{% comment %}
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
{% endcomment %}

<br>
<hr>
<br> 
## Past Members

For a list of the past members [click here]({% link pages/about/past_members.md %})
