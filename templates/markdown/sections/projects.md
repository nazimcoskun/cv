{% extends "section.md" %}

{% block body %}
<table class="table table-sm">
{% for item in items %}
<tr class="row">
  <td class="col-3 col-md-2">{{ item.name }}</td>
  <td class="col-9 col-md-10">
    {{ item.description }}
    <a target="_blank" href="https://{{ item.url }}">[link]</a> 
  </td>
</tr>
{% endfor %}
</table>
{% endblock body %}
