---
title: Home
taxonomy:
    tag:
        - menu_footer
metadata:
    description: 'National Trails of the Russia'
    keywords: 'National trails, expeditions, adventures, soul, nature, wilderness, exploring, education'
content:
    items:
        '@page': /blog
    order:
        by: folder
        dir: desc
    limit: 5
    pagination: false
---

## [National Trails: Historic, Scenic, Recreation.](/trails)

Trails — is an Education, Nature and a Soul.


## [The First Settlers Historic Trail](/trails/the-first-settlers-trail)

The trail starts in the European part of Russia and heading East, the path of the explorers and first settlers who have studied and mastered our country. The trail goes up and down the rivers, crosses the watershed, out to the Pacific ocean, is its edge, and then climbs again to the continent, to the river Indigirka to roll out to the Arctic ocean and walk to Cape Dezhnev. Only the passage of the Trail you need 4 years.

The trail passes along the rivers Volga, Kama, Tagil, Tobol, Irtysh, Ob, Tom, Abakan, Yenisei, Angara, Lena, Olekma, Zeya, Amur, Indigirka.

{% include "includes/trail-map.html.twig" with {'trail': 'the-first-settlers-trail'} %}

## [Our Blog](/blog) <sup><small>{{ header.content.limit }} last messages of {{ page.find('/blog').children|length }}</small></sup>

{% set collection = page.collection %}

<ul id="blogcontent">
{% for child in collection %}
	<li>	
		<p class="intro"><small>{{ child.slug|regex_replace('/\-([0-9]{2})$/', ':$1')|localizeddate('long', 'short', 'en', 'UTC') }} UTC</small></p>

		<h2><a href="{{ child.url }}">{{ child.title }}</a></h2>

		{{ child.content }}
	</li>
{% endfor %}
</ul>

### [read all posts: {{ page.find('/blog').children|length }}](/blog)