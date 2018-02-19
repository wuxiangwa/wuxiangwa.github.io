---
layout: default
---

<!-- Page Header -->
<header class="intro-header" style="background-image: url('{{ site.baseurl }}/{% if page.header-img %}{{ page.header-img }}{% else %}{{ site.header-img }}{% endif %}')">
  <div class="container">
    <div class="row">
      <div class="col-lg-8 col-lg-offset-2 col-md-10 col-md-offset-1">
        <div class="site-heading">
          <h1>{% if page.title %}{{ page.title }}{% else %}{{ site.title }}{% endif %}</h1>
          <!--<hr class="small">-->
          <span class="subheading">{{ page.description }}</span>
        </div>
      </div>
    </div>
  </div>
</header>

<!-- Main Content -->
<div class="container">
  <div class="row">
    <div class="col-lg-8 col-lg-offset-1
                col-md-8 col-md-offset-1
                col-sm-12
                col-xs-12
                postlist-container">
                {{ content }}

    <!-- 俩种处理方式 此处理方式也还是需要页面渲染-->
    <!-- {% for item_hash in site.data.array %}
    {% assign item = item_hash[1] %}
      <div class="post-preview">
        <a href="/2017/09/18/hello-world/">
        <h2 class="post-title"> {{ item.title }}
        </h2>
        </a>
        <p class="post-meta"> {{ item.time }}</p>
      </div>
      <hr>
    {% endfor %} -->

    </div>
    <div class="col-lg-3 col-lg-offset-0
                col-md-3 col-md-offset-0
                col-sm-12
                col-xs-12
                sidebar-container
            ">
            侧边栏 {{site.data.demo.name}}
      <ul>
        {% for item_hash in site.data.array %}
        {% assign item = item_hash[1] %}
          <li>
            {{ item.name }}
          </li>
        {% endfor %}
      </ul>
    </div>
  </div>
</div>
