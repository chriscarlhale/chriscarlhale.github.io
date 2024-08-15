---
layout: page
title: Publications
permalink: /publications
---
{% for pub in site.data.publications %}
  <div class="card m-2 p-2" style="">    
    <div class="row">        
      <div class="col">        
        <div class="card-body">
          <div class="card-text"><small class="text-muted">{{ pub.publisher }} {{ pub.date }}</small></div>
          <h4 class="card-title">{{ pub.name.title }}</h4>
          <h5 class="card-title">{{ pub.name }}</h5>
          <p class="card-text">{{ pub.desc }}</p>
          <p class="card-text">By: 
            {% for auth in pub.author %}
              {{ auth.name }}{% if forloop.last %}{% else %}, {% endif %}
            {% endfor %}    
          </p>
          {% for url in pub.urls %}
            <a href="{{ url.href }}" target="_blank" class="btn btn-primary">{{ url.site }}</a>
          {% endfor %}    
        </div>
      </div>      
      {% if pub.image %}
      <div class="col-md-2">
        <img src="{{ pub.image }}" class="pub-image float-end" alt="{{ pub.name }}">
      </div>
      {% endif %}
    </div>
  </div>
{% endfor %}


