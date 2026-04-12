---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

# layout: home
# layout: layout
layout: default
---

## CoinPort Exchange - News Blog

Reading, reference and news resources for CoinPort Members

<ul id="post-list">
  {% for post in site.posts %}
    <li>
      <b>{{ post.categories }} - </b> {{ post.date  | date: "%-d %B %Y" }} - <a href="{{ post.url }}" class="post-link">{{ post.title }}</a><br />
      {{ post.description }}<br />
    </li>
  {% endfor %}
</ul>

<script>
  const queryString = window.location.search;
  const urlParams = new URLSearchParams(queryString);
  const theme = urlParams.get('theme');
  const className = theme == 'dark-mode'?'dark-mode':'light-mode';
  document.body.classList.toggle(className);

  const links = document.querySelectorAll('.post-link');
  links.forEach(link => {
    link.href += `?theme=${theme}`;
  });
</script>
