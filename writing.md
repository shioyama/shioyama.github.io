---
layout: page
title: Writing
permalink: /writing/
---

Before becoming a programmer, I wore many hats including science writer, journalist
and blogger, covering topics ranging from basic science to <a
href="https://globalvoices.org/2011/10/18/japan-were-losing-to-apple-and-heres-why/"
target="_blank">the Japanese Internet</a>. Writing
has always been—and continues to be—a passion of mine.

Nowadays, I mostly blog at [dejimata.com](https://dejimata.com). Below are some
highlights from recent years.

{% for item in site.data.writing %}
<h3>
<a href="{{ item.url }}" target="_blank">{{ item.title }}</a> <span class="side-note date">({{ item.date }})</span>
</h3>

{{ item.details }}
{% endfor %}
