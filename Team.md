---
title: The Team
layout: Custom
---
<h2 class="custom-heading">
  <span class="icon-title">
    {% include svg/icon/info-circle.svg %}
  </span> Meet the DH Lab
</h2>
<!-- Wrapper to ensure consistent table width -->
<div class="team-table-wrapper">

  <!-- Table for Principal Investigator -->
  <table class="team-table">
    <tbody>
      <tr>
        <td>
          <img src="{{ site.PI[0].image }}" alt="{{ site.PI[0].name }}">
        </td>
        <td>
          <h3><a href="{{ '/PI-Page' | relative_url }}">{{ site.PI[0].name }}</a></h3>
          <h3>{{ site.PI[0].role }}</h3>
          <p>{{ site.PI[0].description }}</p>
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
          <td>
            <img src="{{ member.image }}" alt="{{ member.name }}">
          </td>
          <td>
            <h3>{{ member.name }}</h3>
            <h3>{{ member.role }}</h3>
            <p>{{ member.description }}</p>
          </td>
        </tr>
      </tbody>
    </table>
  {% endfor %}

</div>
