{% if name.lower() != "none" %}
<div class="h6 text-primary">
{{ name }}
</div>
{% endif %}

{% if legend %}
{{ legend }}
{% endif %}

<div class="container">
{% block body %}
{{ data }}
{% endblock body %}
</div>
