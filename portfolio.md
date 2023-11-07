---
layout: default
---

<div class="row">
  <div class=" flex-md-row mb-4 box-shadow">
    <div class="card-body d-flex flex-column align-items-start">
      <h3 class="mb-0">Portfolio</h3> <br>
      <div class="row mb-2">
      {% for item in site.data.portfolio %}
        <div class="crow">
          <div class="card flex-md-row mb-3 box-shadow">
            <div class="text-center">
            <img class="card-img-left " style="width:250px; min-height: 150px;  max-height: 180px; margin-top: 20px;" src="assets/img/{{item.image}}"> 
            </div>
            <div class="card-body d-flex flex-column align-items-start ml-2 mr-2">
              <h6 class="mt-3"><strong>{{item.title}}</strong></h6>
              <div class="mb-2 text-muted"> {{item.description}}</div>
              <h1></h1>
              <div class="row mb-2">
              {%if item.url %}
                <div class="col-md-4"><a href="{{item.url}}" class="btn btn-outline-primary btn-sm">User Manual</a></div>
              {% endif %}
              </div>
            </div>
          </div>
        </div>
      {% endfor %}
      </div>
    </div>
  </div>
</div>
