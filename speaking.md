---
layout: page
title: Speaking
permalink: /speaking/
---

<script>
    document.addEventListener("DOMContentLoaded",
        function() {
            var div, n,
                v = document.getElementsByClassName("youtube-player");
            for (n = 0; n < v.length; n++) {
                div = document.createElement("div");
                div.setAttribute("data-id", v[n].dataset.id);
                div.setAttribute("data-start", v[n].dataset.start);
                div.innerHTML = labnolThumb(v[n].dataset.id);
                div.onclick = labnolIframe;
                v[n].appendChild(div);
            }
        });

    function labnolThumb(id) {
        var thumb = '<img src="https://i.ytimg.com/vi/ID/hqdefault.jpg">',
            play = '<div class="play"></div>';
        return thumb.replace("ID", id) + play;
    }

    function labnolIframe() {
        var iframe = document.createElement("iframe");
        var embed = "https://www.youtube.com/embed/ID?autoplay=1&start=START";
        iframe.setAttribute("src", embed.replace("ID", this.dataset.id).replace("START", this.dataset.start));
        iframe.setAttribute("frameborder", "0");
        iframe.setAttribute("allowfullscreen", "1");
        iframe.setAttribute("start", this.dataset.start);
        this.parentNode.replaceChild(iframe, this);
    }
</script>

I am a frequent speaker at technology conferences in the United States, Europe
and Japan. My specialty is presenting difficult concepts in a way that is easy to
understand.

I'm available for speaking opportunities, [get in touch](mailto:{{ site.email }}) if you
think I might fit the bill.

### The Elusive Attribute <span class="side-note">@ RailsConf 2019</span> {#the-elusive-attribute}

Ruby on Rails is famous for its “magic”, but there is very little out there
explaining how that magic actually works under the hood. In this talk <a
href="https://railsconf.com/program/sessions#session-751" target="_blank">I
gave at RailsConf 2019</a>, I pick apart the magic underlying one of the most
basic elements of Rails: its **attributes**.

{% include presentation.html
  youtube-id="PNNrmNTQx2s"
  slides-url="https://speakerdeck.com/shioyama/the-elusive-attribute"
  slides-img="the-elusive-attribute.png" %}

### Building Generic Software <span class="side-note">@ RubyConf 2018</span> {#building-generic-software}

In this presentation <a
href="https://rubyconf.org/2018/program.html#session-715" target="_blank">given
at RubyConf 2018</a>, I introduce the concept of Inversion of Control (IoC)
through an example where we walk through the steps of building a framework.
The framework ends up being a simplified version of [Mobility](/projects#mobility).

{% include presentation.html
  youtube-id="RZkemV_-__A"
  slides-url="https://speakerdeck.com/shioyama/building-generic-software"
  slides-img="building-generic-software.png" %}

### Metaprogramming For Generalists <span class="side-note">@ EuRuKo 2018</span> {#metaprogramming-for-generalists}

Metaprogramming is the machinery that enables Ruby's diverse gem ecosystem, its
intuitive DSLs, and its flexible frameworks. But it is also demonized and
misunderstood. In this talk, which <a href="https://euruko2018.org/schedule/"
target="_blank">I gave at EuRuKo 2018</a> in Vienna, Austria, I explain why
metaprogramming is so important for building the generic components we depend
on every day.

{% include presentation.html
  youtube-id="1fIlcnrJHxs"
  youtube-start="290"
  slides-url="https://speakerdeck.com/shioyama/metaprogramming-for-generalists"
  slides-img="metaprogramming-for-generalists.png" %}

### The Ruby Module Builder Pattern <span class="side-note">@ RubyKaigi 2017</span> {#the-ruby-module-builder-pattern}

Did you know that Ruby has configurable modules? One of the most interesting
features of Ruby, the Module Builder Pattern is also probably its least
well-known. In this talk <a
href="https://rubykaigi.org/2017/presentations/shioyama.html"
target="_blank">given at RubyKaigi 2017</a>, I explain this powerful
feature through simple, concrete examples.

{% include presentation.html
  youtube-id="_E1yKPC-r1E"
  slides-url="https://speakerdeck.com/shioyama/the-ruby-module-builder-pattern"
  slides-img="the-ruby-module-builder-pattern.png" %}
