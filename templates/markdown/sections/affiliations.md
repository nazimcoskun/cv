{% extends "section.md" %}

{% block body %}
<table class="table table-sm">
{% for i in items %}
<tr class="row">
  <td class="col-12">{{ i.name }}</td>
</tr>
{% endfor %}
</table>
{% endblock body %}
