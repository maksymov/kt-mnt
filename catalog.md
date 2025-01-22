---
layout: page
title: Services
permalink: /services/
---

<div class="row">
    {% assign catalog = site.pages | where_exp: "item" , "item.path contains 'catalog/'"%}
    {% for page in catalog %}
        <div class="col col-12 col-md-6 mt-4">
            <div class="card">
                <img src="{{ site.baseurl }}{{ page.img }}" class="card-img-top" alt="...">
                <div class="card-body">
                <h5 class="card-title">{{ page.title }}</h5>
                <p>{{ page.desc }}</p>
                <a href="{{ site.baseurl }}/contacts/" class="btn btn-dark">Request</a>
                </div>
            </div>
        </div>
    {% endfor %}
</div>
