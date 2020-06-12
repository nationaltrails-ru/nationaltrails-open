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


## [Volga river blue trail: The Great Adventure](/trails/volga-river-blue-trail)

Над волжскими водами еще много тысячелетий назад горели костры первобытного человека. Грубые, выдолбленные или выжженные из древесных стволов челны лежали на песке у древних городищ. Птолемей во втором веке нашей эры упоминай о Волге, называя ее древним именем Ра. Жившие на берегах Волги финские племена называли ее Светлая, Блистающая. Арабы в средние века величали - Итиль - Река Рек. С восьмого века она становится уже одним из главных торговых путей для огромной территории. В летописях рассказывается о том, как славяне-руссы спускались вниз по Волге, бесстрашно плыли через Каспийское море и проникали со своими товарами далеко на восток, в сказочный Багдад.

Словно гигантское дерево, раскинула Волга по Русской равнине свои ветви-притоки. Почти полтора миллиона квадратных километров захватила она в черту своего бассейна. Зародившись небольшим ручьем в центре Валдайской возвышенности, Волга на пути к морю принимает дань от многочисленных притоков и превращается в могучую реку, самую большую во всей Европе.

{% include "includes/trail-map.html.twig" with {'trail': 'volga-river-blue-trail'} %}


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