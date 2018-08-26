---
title: Наш Блог
menu: Блог
taxonomy:
    tag:
        - menu_middle
        - menu_footer
content:
    items:
        - '@self.children'
    order:
        by: publish_date
        dir: desc
    limit: 10
    pagination: true
feed:
    limit: 10
---