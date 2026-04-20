---
layout: photolist
title: Publications/Posters
description: Publications with links to papers, blogs and code.
menu: yes
order: 1
---
\* denotes equal contribution
{% assign hashes = (site.data.papers) %}
{% capture years %}
{% for hash in hashes %}
{{ hash[0] }}
{% endfor %}
{% endcapture %}

{% assign sortedyears = years | split:' ' | sort | reverse %}
<ul>
{% for year in sortedyears %}{% for paper in hashes[year] %}{% include paper_lena.html paper=paper %}{% endfor %}{% endfor %}
</ul>
