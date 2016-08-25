---
layout: page-layout
---
<header>
  <p>A design firm for good.</p>
</header>

<section id="services">
  <div class="row col_3">
    <div>
      <img src="/svg/research.svg"/>
      <p>Research</p>
    </div>
    <div>
      <img src="/svg/branding.svg"/>
      <p>Branding</p>
    </div>
    <div>
      <img src="/svg/design.svg"/>
      <p>Design</p>
    </div>
  </div>
</section>

<section id="about">
  <h2>About</h2>
  <p>{{ site.description }}</p>
</section>

<section id="work">
  <h2>Work</h2>
  <ul>
    {% for post in site.posts %}
      {% if post.categories contains 'featured' %}
      <li>
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p>{{ post.excerpt }}</p>
      </li>
      {% endif %}
    {% endfor %}
  </ul>
</section>

<section id="team">
  <h2>Team</h2>
  <ul>
    {% for member in site.data.members %}
    <li>
      <h3><a href="{{ member.link }}">{{ member.name }}</a></h3>
      <p>{{ member.story }}</p>
    </li>
    {% endfor %}
  </ul>
</section>
