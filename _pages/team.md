---
layout: page
title: team
permalink: /team/
description: 
nav: true
nav_order: 1
display_categories: [postdoc, phd, rse, msc, ra, honours]
horizontal: true
---

<!-- pages/team.md -->
<div class="projects">
<div class="people">

  <!-- Display categorized projects -->
  {% for category in page.display_categories %}

    {%- assign peops = site.data.people | where: "position", category | where: "current", true -%}
    {%- assign psize = peops | size -%}

    {% if psize > 0%}
        <h2 class="category">
        {% if category == "phd" %} PhD students 
        {% elsif category == "postdoc" %} Postdocs 
        {% elsif category == "msc" %} Master students 
        {% elsif category == "ra" %} Research assistants 
        {% elsif category == "honours" %} Honours students (Bsc) 
        {% else %} Visitors {% endif %} 
        </h2>

        <div class="labmember">
        {% if page.horizontal %}
            <div class="container">
                <div class="row row-cols-1">
                    {%- for person in peops -%}
                        {% include people_horizontal.html %}
                    {%- endfor %}
                </div>
            </div>
        {% else %}
            <div class="grid">
                {%- for person in peops -%}
                    {% include people.html %}
                {%- endfor %}
            </div>
        {% endif %}
        </div>

        
    {% endif %}

  {%- endfor -%}
</div>

<br><br>
<h2> Alumni </h2>
<hr>

<div class="projects">
  {% for category in page.display_categories %}

    {%- assign peops = site.data.people | where: "position", category | where: "current", false -%}
    {%- assign psize = peops | size -%}

    {% if psize > 0%}
        <h2 class="category">
        {% if category == "phd" %} PhD students 
        {% elsif category == "postdoc" %} Postdocs 
        {% elsif category == "msc" %} Master students 
        {% elsif category == "ra" %} Research assistants 
        {% elsif category == "honours" %} Honours students (Bsc) 
        {% elsif category == "rse" %} Research engineers 
        {% else %} Visitors {% endif %} 
        </h2>

        <div class="labmember">
        {% if page.horizontal %}
            <div class="container">
                <div class="row row-cols-1">
                    {%- for person in peops -%}
                        {% include people_horizontal.html %}
                    {%- endfor %}
                </div>
            </div>
        {% else %}
            <div class="grid">
                {%- for person in peops -%}
                    {% include people.html %}
                {%- endfor %}
            </div>
        {% endif %}
        </div>

        
    {% endif %}

  {%- endfor -%}

</div>
</div>