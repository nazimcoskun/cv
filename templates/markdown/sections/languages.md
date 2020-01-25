{% extends "section.md" %}

{% block body %}
<table class="table table-sm">
{% for item in items %}
<tr class="row">
  <td class="col-3 col-md-2">{{ item.language }}</td>
  <td class="col-9 col-md-10">
  {{ item.level }}
    <!-- {% if item.certificates %}
      <br>
      {% for certificate in item.certificates %}
        {{ certificate.test }}<br>
      {% endfor %}
    {% endif %} -->
  </td>
</tr>
{% endfor %}
</table>
{% endblock body %}
