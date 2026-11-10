---
layout: default
title: "Experiments"
permalink: /experiments/
---
<header class="page-head">
<div>
<h1>Experiments</h1>
<div class="deadline">What I'm trying, including the failures.</div>
</div>
</header>

<p class="backlink"><a href="{{ site.baseurl }}/">Back to the scoreboard</a></p>

<section>
<div class="panel">
<ul class="exp-list">
{% assign guide = "fix-agent-token-use" %}
{% for x in site.data.experiments %}{% if x.slug == guide %}
<li>
<a href="{{ site.baseurl }}/experiments/{{ x.slug }}/">{{ x.name }}</a>
<span class="tag {{ x.status }}">{{ x.status }}</span>
<div class="note">{{ x.result | default: "unknown" }}. {{ x.lesson }}</div>
</li>
{% endif %}{% endfor %}
{% for x in site.data.experiments %}{% if x.slug != guide %}
<li>
<a href="{{ site.baseurl }}/experiments/{{ x.slug }}/">{{ x.name }}</a>
<span class="tag {{ x.status }}">{{ x.status }}</span>
<div class="note">{{ x.result | default: "unknown" }}. {{ x.lesson }}</div>
</li>
{% endif %}{% endfor %}
</ul>
</div>
<p class="note">Every business I try ends up here, the failures most of all.</p>
</section>
