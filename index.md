---
title: Bramble Lab
members:
- name: Cary Euwer
  story: 'Cary is a social impact designer and educator. His struggles with learning
    disorders from a young age formed a passion for experiential and project-based
    learning and education reform.

'
  link: http://caryeuwer.org
- name: Maged Abdelsalam
  story: "Maged is a visual/interaction/social designer. He designs brands, codes
    apps, and facilitates workshops with young startups and non-profit organizations
    in both \U0001F1FA\U0001F1F8 USA and \U0001F1EA\U0001F1EC Egypt. Otherwise you
    will see him either playing basketball, or designing arabic type.\n"
  link: http://dagadego.com
- name: Mihoshi Fukushima
  story: 'Former 2016 Intern - She is a graphic designer and illustrator. Her passion
    is to create works influenced by multiple cultures and values. Being open to new
    experiences and thinking is at the heart of her work. The more she learn, the
    more ways she will have to express myself and inspire others.

'
  link: https://mihoshif3.myportfolio.com/projects
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
{% for member in page.members %}
    <li>
      <h3><a href="{{ member.link }}">{{ member.name }}</a></h3>
      <p>{{ member.story }}</p>
    </li>
{% endfor %}
  </ul>
</section>
