---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

# layout: home
layout: layout
# layout: default
---
## CoinPort Exchange - News Blog 4

<link rel="stylesheet" href="/style.css" />
    <script>
        const queryString = window.location.search;
        const urlParams = new URLSearchParams(queryString);
        const theme = urlParams.get('theme');
        const className = theme=='dark-mode'?'dark-mode':'light-mode';
        document.body.classList.toggle(className);
    </script>

Reading, reference and news resources for CoinPort Members

<ul>
  {% for post in site.posts %}
    <li>
      <b>{{ post.categories }} - </b> {{ post.date  | date: "%-d %B %Y" }} - 
      <a href="{{ post.url }}">{{ post.title }}</a><br>
      {{ post.description }}<br>
    </li>
  {% endfor %}
</ul>
