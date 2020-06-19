---
layout: default
sidebar_link: true
title: Team
group: members
---

<h1>Sogin Lab Team</h1>

 {% include team-head.html %}

The Sogin lab welcomes people of any race, religion, national origin, gender identity, caregiver and family commitments, political affiliation, sexual orientation, and eligible age or ability.<br>
<h5>See our<a href="/compact/"> lab compact and philosophy</a>.</h5>

<div class="lab-wrapper">
    <ul class="lab-list">
    <!-- Current PIs -->
    {% for member in site.data.team %}
        {% if member.is_current and member.is_pi %}
            {% if member.name and member.bio %}
                {% include member.html %}
            {% endif %}
        {% endif %}
    {% endfor %}
    <!-- Current non-PIs -->
    {% for member in site.data.team %}
        {% if member.is_current and member.is_pi == false %}
            {% if member.name and member.bio %}
                {% include member.html %}
            {% endif %}
        {% endif %}
    {% endfor %}
    </ul>
</div>


