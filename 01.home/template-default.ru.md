---
title: Главная
taxonomy:
    tag:
        - menu_footer
metadata:
    description: 'Национальные Тропы России'
    keywords: 'Национальные Тропы, экспедиции, приключения, душа, природа, дикая природа, исследования, образование, обучение'
content:
    items:
        '@page': /blog
    order:
        by: folder
        dir: desc
    limit: 5
    pagination: false
---

## [Национальные Тропы: Исторические, Научные, Рекреационные.](/trails)

Тропы — это Познание, Природа и Душа.

## [Историческая: Тропа Первых Переселенцев](/trails/the-first-settlers-trail)

Тропа начинается в европейской части России и идёт на восток, по пути землепроходцев и первых переселенцев, изучавших и осваивавших нашу страну. Тропа идёт вниз и вверх по течению рек, пересекает водоразделы, выходит к Тихому океану, идёт его краем, затем снова забирается на континент, чтобы по реке Индигирка выкатиться к Северному Ледовитому океану и дойти до мыса Дежнёва.

Тропа проходит по рекам Волга, Кама, Тагил, Тобол, Иртыш, Обь, Томь, Абакан, Енисей, Ангара, Лена, Олёкма, Зея, Амур, Охотское море, Индигирка, Восточно-Сибирское море, мыс Дежнёва. Протяжённость Тропы 21000 км, на её прохождение требуется не менее 4 лет.

{% include "includes/trail-map.html.twig" with {'trail': 'the-first-settlers-trail'} %}

## [Наш Блог](/blog) <sup><small>{{ header.content.limit }} последних сообщений из {{ page.find('/blog').children|length }}</small></sup>

{% set collection = page.collection %}

<ul id="blogcontent">
{% for child in collection %}
	<li>	
		<p class="intro"><small>{{ child.slug|regex_replace('/\-([0-9]{2})$/', ':$1')|localizeddate('long', 'short', 'ru', 'UTC') }} UTC</small></p>

		<h2><a href="{{ child.url }}">{{ child.title }}</a></h2>

		{{ child.content }}
	</li>
{% endfor %}
</ul>

### [читать все записи: {{ page.find('/blog').children|length }}](/blog)