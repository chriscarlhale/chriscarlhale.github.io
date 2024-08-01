---
layout: page
title: Grants
permalink: /grants
---
{% for grant in site.data.grants %}
  <div class="card m-2 p-2" style="">    
    <div class="row">        
      <div class="col">        
        <div class="card-body">
          <!-- <div class="card-text">{{ grant.id}}</div> -->
          <div class="date float-end">{{ grant.date }}</div>
          <div class="card-text"><h2>{{ grant.title }}</h2></div>
          <p class="card-text">{{ grant.desc }}</p>          
        </div>
      </div>      
      {% if grant.image %}
      <div class="col-md-2">
        <img src="{{ grant.image }}" class="pub-image float-end" alt="{{ grant.title }}">
      </div>
      {% endif %}
    </div>
  </div>
{% endfor %}
