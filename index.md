---
layout: default
---
<!-- News -->
<div class="row">
  <div class=" flex-md-row mb-4 box-shadow">
    <div class="card-body d-flex flex-column align-items-start">
      <h3 class="mb-0">News</h3> <br>
      <ul>
      {% for item in site.data.news %}
        {% if item.link%}
          <li><strong>{{item.date}} : </strong> <a href="{{item.link}}"> {{ item.event }}</a></li>
        {% else %}
          <li><strong>{{item.date}} : </strong> {{ item.event }}</li>
        {% endif %}
      {% endfor %}
      </ul>
    </div>
  </div>
</div>
<!-- Publications -->
<div class=" flex-md-row mb-4 box-shadow">
  <div class="card-body d-flex flex-column align-items-start">
    <h3 class="mb-0">Publications</h3> <br>
    {% for item in site.data.publications %}
      <!-- <div class="col-md-12"> -->
      <div class="row">
        <div class="card flex-md-row mb-3 box-shadow">
          <div class="text-center">
          <img class="card-img-left " style="width:250px; min-height: 150px;  max-height: 180px; margin-top: 20px;" src="assets/img/{{item.image}}"> 
          </div>
          <div class="card-body d-flex flex-column align-items-start ml-1 mr-1">
            <h6 class="mt-3" ><strong>{{item.title}}</strong></h6>
            <div class="mb-1 text-muted"> Authors: {{item.authors}}</div>
            <div class="">{{item.conference}}</div> <br>
            <div class="text-center">
              <span class="actions">
                <ul>
                  <li><a href="{{item.pdf}}" class="btn btn-outline-primary btn-sm">PDF</a></li>
                  {% if item.code %}
                  <li><a href="{{item.code}}" class="btn btn-outline-success btn-sm">Code</a></li>
                  {% endif%}
                  {% if item.video %}
                  <li><a href="{{item.video}}" class="btn btn-outline-info btn-sm">Video</a></li>
                  {% endif%}
                </ul>
              </span>
            </div>
          </div>
        </div>
      </div>
      <!-- </div> -->
    {% endfor %}
  </div>
</div>
<!-- Teaaching -->
<!-- <div class="col-md-12">
  <div class=" flex-md-row mb-4 box-shadow">
    <div class="card-body d-flex flex-column align-items-start">
      <h3 class="mb-0">Teaching</h3> <br>
      <ul>
      {% for item in site.data.teaching %}
        <li><strong>{{item.semester}} : </strong> {{item.job}}</li>
      {% endfor %}
      </ul>
    </div>
  </div>
</div> -->
<!-- Services -->
<div class="col-md-12">
  <div class=" flex-md-row mb-4 box-shadow">
    <div class="card-body d-flex flex-column align-items-start">
      <h3 class="mb-0">Services</h3> <br>
      <h5 class="mb-0">Review conferences</h5> <br>
      <ul>
      {% for item in site.data.review_conf %}
        <li><a href="{{item.link}}">{{item.conf}}</a></li>
      {% endfor %}
      </ul>
      <h5 class="mb-0">Review Journals</h5> <br>
      <ul>
      {% for item in site.data.review_journal %}
        <li><a href="{{item.link}}">{{item.journal}}</a></li>
      {% endfor %}
      </ul>
    </div>
  </div>
</div>
<!-- Articles -->
<!-- <div class="col-md-12">
  <div class=" flex-md-row mb-4 box-shadow">
    <div class="card-body d-flex flex-column align-items-start">
      <h3 class="mb-0">Articles</h3> <br>
      <ul>
      {% for item in site.data.articles %}
        <li><a href="assets/articles/{{item.link}}">{{item.title}}</a></li>
      {% endfor %}
      </ul>
    </div>
  </div>
</div> -->


