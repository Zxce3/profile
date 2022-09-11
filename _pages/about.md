---
layout: default
title: About
permalink: /about/
order: 2
icon: person
---


{% capture gstats %}
<h2 class="content-title">Github Stats</h2>
<img class="img-fluid w-full" src="https://raw.githubusercontent.com/Zxce3/Zxce3/main/github-metrics.svg" alt="Metrics">
{% endcapture %}


{%- assign me = site.data.profile.my -%}
{%- if me -%}
<div class="content card border-0 m-0">
    {%- for data in me.data -%}
    <h2 class="content-title">{{ data.title }}</h2>
    <p>{{ data.content }}</p>
    {%- endfor -%}
    {%- include friend.liquid -%}
    {{ gstats }}
</div>
{%- endif -%}
