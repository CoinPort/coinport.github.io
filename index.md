---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

# layout: home
layout: layout
#layout: default
---
## CoinPort Exchange - News Blog

Reading, reference and news resources for CoinPort Members.3

<button id="All" onclick="filterUsingCategory('All')">
  *Show All Posts*
</button>
{% assign categories = site.categories | sort %}
{% for category in categories %}
  {% assign cat = category | first %}
  <button id="{{ cat }}" onclick="filterUsingCategory(this.id)">
    {{ cat }}
  </button>
{% endfor %}
