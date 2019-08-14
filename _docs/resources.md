---
layout: default
title: Resources
---

<link href="https://cdn.datatables.net/1.10.19/css/dataTables.bootstrap4.min.css" rel="stylesheet" type="text/css">
<script src="//cdn.datatables.net/1.10.19/js/jquery.dataTables.min.js"></script>
<script src="https://cdn.datatables.net/1.10.19/js/dataTables.bootstrap4.min.js"></script>
<script>
$(document).ready(function() {
  $('#resourcs').DataTable();
});</script>
<div class="card shadow mb-4">
<div class="card-header py-3">
  <h6 class="m-0 font-weight-bold text-primary">Resources</h6>
</div>
<div class="card-body">
  <div class="table-responsive">
    <table class="table table-bordered" id="{{ include.title | slugify }}" width="100%" cellspacing="0"><thead><tr>
<th>Title</th>
<th>Levels</th>
<th>Tags</th>
<th>URL</th>
</tr></thead>
<tfoot><tr>
<th>Title</th>
<th>Levels</th>
<th>Tags</th>
<th>URL</th></tr>
</tfoot>
<tbody>{% for resource in site.resources %}<tr>
<td>{{ resource.title }}</td>
<td>{% for level in resource.levels %}<a href="{{ site.baseurl }}/tags#{{ level }}"><span class="badge badge-success">{{ level }}</span></a>{% endfor %}</td>
<td>{% for tag in resource.tags %}<a href="{{ site.baseurl }}/tags#{{- tag -}}"><span class="badge badge-primary">{{- tag -}}</span></a> {% endfor %}</td>
<td><a href="{{ site.baseurl }}/{{ resource.url }}"><button class="btn btn-primary btn-sm">View</button></a></td>
</tr>{% endfor %}
</tbody>
</table>
   </div>
  </div>
</div>
