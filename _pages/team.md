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

<div class="alert alert-primary" role="alert">
  <strong> POSTDOC OPENING: Probabilistic programming for coupling digital twins in geophysics</strong> <br><br>

  <strong>Problem description</strong>
  Arguably the most valuable tool one can create from Big Data is a digital twin that supports policymakers in understanding and interacting with various systems, ranging from industrial products to natural systems. Distilling twins of large-scale systems that consist of many interacting subsystems is, however, a major challenge. For example, a digital twin of a river estuary needs to combine different interacting subsystems (e.g., atmosphere, soil, groundwater, waterways, barriers, and coastal waters) and its overall success depends on the ability to couple the subsystems with each other and data. Unfortunately, naively coupling the existing subsystems into a ‘monster twin’ is computationally infeasible. Probabilistic programming may offer a way to avoid this by reducing the coupled system to its essence. <br><br>

  <strong>Position description</strong>
  The postdoctoral researcher will investigate the use of probabilistic programming to couple digital twins and simulators. Probabilistic programming has witnessed significant success in modelling and inverting scientific simulators. Your project will investigate how those techniques can be applied to problems when multiple simulators (digital twins) are present. <br><br>

 <strong>Requirements</strong>
We are looking for a candidate with one of the following profiles:
<ul>
    <li>Background in probabilistic artificial intelligence, and preferably probabilistic programming</li>
    <li>Background in one or multiple disciplines of geophysics in the broadest sense, e.g., hydrology, oceanography, and solid earth, with a strong and demonstrable experience with probabilistic methods and/or numerical modelling</li>
</ul>
We are looking for candidates that have a PhD in one of these areas or are going to obtain it soon. <br><br>

<strong>Practicalities</strong>
<ul>
    <li>Appointment length: 1 year</li>
    <li>Start date: as soon as possible</li>
    <li>Application process: no fixed deadline, send an email to Sebastijan Dumancic (s.dumancic@tudelft.nl) with a CV and a short motivation</li>
    <li>Questions: direct them to Sebastijan Dumancic</li>
</ul>
</div>


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

</div>