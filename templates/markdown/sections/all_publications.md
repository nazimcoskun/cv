<div class="h6 text-primary">
Publications
<!-- <a href="https://scholar.google.com/citations?user={{ scholar_id }}" class="btn btn-outline-primary btn-sm float-right">Google Scholar</a> -->
</div>

{% for p in content %}

<div class="h6">
{{ p.title }}
</div>

<table class="table table-sm mb-4">
{{ p.details }}
</table>

{% endfor %}
