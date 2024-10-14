---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

# layout: home
layout: layout
#layout: default
---
## CoinPort Exchange - News Blog

Reading, reference and news resources for CoinPort Members.2

{% assign counter=0 %}
<main id="page" role="main">
{% for category in site.categories %}
<div class="col pane ui-layout-{% assign counter=counter | plus:1 %}" id="{{ page.id }}">
    <div class="colheader">
        <div class="bar"></div>
        <p class="lead">Leadin text</p>
        <h1>{{ category | first }}</h1>
    </div>
    <div class="colscroll unlock">
{% for posts in category %}
{% for post in posts %}
    <div class="colblock" itemscope itemtype="http://schema.org/BlogPosting">    
        <div class="excerpt">
            <time class="date" datetime="{{ page.date | '%Y-%m-%dT%H:%i:%S-08:00' }}" itemprop="datePublished">
                {{ page.date | date: '%B %d, %Y' }}
            </time>
        <h1>
            <a itemprop="url" href="{{ post.url }}" target="_blank" title="{{ post.title }}">
                <span itemprop="name" itemprop=name>{{ post.title }}</span>
            </a>
        </h1>                        
        <p itemprop="description">
            {{ post.excerpt }}..
        </p>
        <p class="link_tags">{{ page.tags }}</p>
        </div>
    </div>
{% endfor %}
{% endfor %}
    </div>
</div>
{% endfor %}
</main>
