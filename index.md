---
layout: home
---

**Programmer, writer and speaker experienced in building and maintaining
complex web applications for the Japanese market.** I'm the author of
[Mobility](https://github.com/shioyama/mobility), a Ruby gem for managing model
translations, and an active contributor to many other open-source projects
including Ruby on Rails.

I currently spend my days developing the foundations for commerce
as a member of the Code Foundations team at [Shopify](https://www.shopify.com).
[Learn more about me.](/about)

## Recent

<ul class="recent">
  {% for item in site.data.recent %}
    <li>
      <span class="date">{{ item.date }}</span><br />
      <a href="{{ item.url }}" target="_blank"><strong>{{ item.title }}</strong></a>
      <span class="details">{{ item.details }}</span>
    </li>
  {% endfor %}
</ul>
