---
title: The Team
layout: Custom
---

## Meet the DH Lab

<!-- Wrapper to ensure consistent table width -->
<div class="team-table-wrapper">

  <!-- Table for Principal Investigator -->
  <table class="team-table">
    <tbody>
      <tr>
        <td><h3>{{ site.PI[0].role }}</h3></td> <!-- Role as h3 -->
        <td><img src="{{ site.PI[0].image }}" alt="{{ site.PI[0].name }}"></td>
        <td>
          <!-- Name linked to PI-Page.md -->
          <h3><a href="{{ '/PI-Page' | relative_url }}">{{ site.PI[0].name }}</a></h3> <!-- Name linked to PI-Page -->
          <p>{{ site.PI[0].description }}</p> <!-- Description as normal text -->

          <!-- Link Button below description -->
          <a href="{{ '/PI-Page' | relative_url }}" class="link-button">Learn More</a>
        </td>
      </tr>
    </tbody>
  </table>

  <!-- Table for Lab Members -->
  {% for member in site.Lab-Members %}
    <table class="team-table">
      <tbody>
        <tr>
          <td><h3>{{ member.role }}</h3></td> <!-- Role as h3 -->
          <td><img src="{{ member.image }}" alt="{{ member.name }}"></td>
          <td>
            <h3>{{ member.name }}</h3> <!-- Name as h3 -->
            <p>{{ member.description }}</p> <!-- Description as normal text -->
          </td>
        </tr>
      </tbody>
    </table>
  {% endfor %}

</div>
