---
layout: page
title: team
permalink: /team/
description: 
nav: true
nav_order: 1
display_categories: [postdoc, phd, msc, ra, honours]
horizontal: false
---

<!-- pages/team.md -->
<div class="projects">

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

        {% if page.horizontal %}
            <div class="container">
                <div class="row row-cols-2">
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

        
    {% endif %}

  {%- endfor -%}

  ## Alumni

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
        {% else %} Visitors {% endif %} 
        </h2>

        {% if page.horizontal %}
            <div class="container">
                <div class="row row-cols-2">
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

        
    {% endif %}

  {%- endfor -%}

</div>