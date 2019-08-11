---
title: Students
layout: wide
---
<!-- TODO use unminified version, customize style-->
<style>
.page-item.active .page-link {
  background-color: none !important;
  border-color: none !important;
}
</style>

<link href="https://cdn.datatables.net/1.10.19/css/dataTables.bootstrap4.min.css" rel="stylesheet" type="text/css">
<script src="//cdn.datatables.net/1.10.19/js/jquery.dataTables.min.js"></script>
<script src="https://cdn.datatables.net/1.10.19/js/dataTables.bootstrap4.min.js"></script>
<script>
$(document).ready(function() {
  $('#students').DataTable();
});</script>
<div class="card shadow mb-4">
<div class="card-header py-3">
  <h6 class="m-0 font-weight-bold text-primary">Students</h6>
</div>
<div class="card-body">
  <div class="table-responsive">
    <table class="table table-bordered" id="students" width="100%" cellspacing="0"><thead><tr>
<th>Name</th>
<th>Institution</th>
<th>Program</th>
<th>Interests</th>
<th>URL</th>
</tr></thead>
<tfoot><tr>
<th>Name</th>
<th>Institution</th>
<th>Program</th>
<th>Interests</th>
<th>URL</th></tr>
</tfoot>
<tbody>{% for student in site.people %}{% if student.status == "student" %}<tr>
<td>{{ student.name }}</td>
<td>{{ student.institution }}</td>
<td>{{ student.program }}</td>
<td>{{ student.interests }}</td>
<td><a href="{{ site.baseurl }}/{{ student.url }}"><button class="btn btn-primary btn-sm">Profile</button></a></td>
</tr>{% endif %}{% endfor %}
</tbody>
</table>
 </div>
</div>
</div>
