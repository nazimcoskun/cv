{% extends "section.md" %}

{% block body %}
<table class="table table-sm">
  <tbody>
    {% for school in items %}
      <tr class="row">
        <td class="col-3 col-md-2">{{ school.dates }}</td>
        <td class="col-9 col-md-10">
          {% if school.degree %}
            {{ school.degree }},
            {% if school.overallGPA %}
              ({{ school.overallGPA }})
            {% endif %}
          {% endif %}
          {{ school.school }},
          {{ school.location }}
        </td>
      </tr>
    {% endfor %}
  </tbody>
</table>
{% endblock body %}
