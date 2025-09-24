---
title: Publications
layout: default
permalink: /publications
---

# Publications

## Recently Submitted

{% for pub in site.data.publications_recent %}
[{{ pub.title }}]({{ pub.link }})  
{{ pub.authors }}  
*{{ pub.journal }}*, {{ pub.year }}

{% endfor %}

## Peer-Reviewed Articles

{% for pub in site.data.publications_peerreviewed %}
[{{ pub.title }}]({{ pub.link }})  
{{ pub.authors }}  
*{{ pub.journal }}*, {{ pub.year }}

{% endfor %}

## Conference Proceedings

{% for pub in site.data.publications_conference %}
[{{ pub.title }}]({{ pub.link }})  
{{ pub.authors }}  
*{{ pub.conference }}*, {{ pub.location }}, {{ pub.year }}

{% endfor %}

## Oral Presentations

{% for pub in site.data.publications_oral %}
**{{ pub.title }}**  
{{ pub.authors }}  
*{{ pub.conference }}*, {{ pub.location }}, {{ pub.year }}

{% endfor %}

## Poster Presentations

{% for pub in site.data.publications_poster %}
**{{ pub.title }}**  
{{ pub.authors }}  
*{{ pub.conference }}*, {{ pub.location }}, {{ pub.year }}

{% endfor %}





