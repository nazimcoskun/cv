{% extends "section.md" %}

{% block body %}
<table class="table table-sm">
{% for i in items %}
<tr class="row">
  <td class="col-3 col-md-2">{{ i.dates }}</td>
  <td class="col-9 col-md-10">{{ i.title }}, {{ i.place }}, {{ i.location }}</td>
</tr>
<tr>
  {#
  <td colspan="100%">
    <ul>
      {% for detail in i.details %}
        <li markdown="1">
        {{ detail }}
        </li>
      {% endfor %}
    </ul>
  </td>
  #}
</tr>
{% endfor %}
</table>
{% endblock body %}
