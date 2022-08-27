---
layout: page
title: Robots
icon: fas fa-tag
order: 3
panel: false
---

<div class="row">
{% for robot in site.robots %}
<div class="col-sm-6">
  <div class="card text-white bg-dark">
    <div class="card-header">
        <p>{{robot.name}}</p>
    </div>
    <img class="card-img-top bg-white" src="../assets/img/robots/{{ robot.img }}" alt="{{ robot.name }}">
    <div class="card-body">
        <h1 class="card-title">{{robot.name}}</h1>
        <h4 class="card-subtitle mb-2 text-muted">{{robot.competition}} - {{robot.year}}</h4>
        <p class="card-text">{{robot.description}}</p>
    </div>
    <div class="card-footer">
        <a href="{{robot.link}}" class="btn btn-primary">Plus d'informations</a>
    </div>
  </div>
</div>
{% endfor %}
</div>