---
layout: page
title: Papers
permalink: /papers
---
{% for paper in site.data.papers %}
  <div class="card m-2 p-2" style="">    
    <div class="row">        
      <div class="col">        
        <div class="card-body">
          <!-- Uncomment For Debugging Data <div class="card-text">{{paper.id}}</div> -->
          <div class="card-text py-2">{{ paper.journal }}<div class="date float-end">{{ paper.date }}</div></div>
          <h4 class="card-title">{{ paper.title }}</h4>
          <h5 class="card-title">{{ paper.subtitle }}</h5>
          <p class="card-text">{{ paper.desc }}</p>
          <p class="card-text">{{ paper.author }}</p>
          {% for url in paper.urls %}
            <a href="{{ url.href }}" target="_blank" class="btn btn-primary">{{ url.site }}</a>
          {% endfor %}    
        </div>
      </div>      
      {% if paper.image %}
      <div class="col-md-2">
        <img src="{{ paper.image }}" class="pub-image float-end" alt="{{ paper.title }}">
      </div>
      {% endif %}
    </div>
  </div>
{% endfor %}