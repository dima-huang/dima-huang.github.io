---
title: The Team
layout: Custom
---

<h2 class="custom-heading">
Meet the DH Lab
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
{% assign sorted_members = site.Lab-Members | sort: 'date' %}
{% for member in sorted_members %}
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

          {% if member.email %}

<p style="display: inline-flex; align-items: center; color: rgba(67, 67, 67, 0.85); margin: 0;">
  <span style="width: 1.4em; height: 1.4em; margin-right: 0.3em; display: inline-flex; align-items: center;">
    {% include svg/icon/social/mail.svg %}
  </span>
  <a href="mailto:{{ member.email }}">{{ member.email }}</a>
</p>


          {% endif %}
        </td>
      </tr>
    </tbody>
  </table>
{% endfor %}



</div>
