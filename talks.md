---
layout: default
title: Talks
permalink: /talks/
navigation: true
---

<header class="black-strip">
    <nav class="main-nav clearfix">
        <a class="blog-logo" href="../">
            <img src="../assets/images/logo.png" alt="Webpage Logo" />
        </a>

        <div class="nav-buttons">
            <a class="no-menu-button" href="../assets/pdf/CV_Marco (2).pdf" target="_blanck">CV</a>
            <a class="no-menu-button" href="{{ '/talks/' | relative_url }}">Talks</a>
            <a class="no-menu-button" href="{{ '/research/' | relative_url }}">Research</a>
        </div>
    </nav>
</header>

<section class="post-content">

<h1>Talks and Seminars</h1>

{% assign talks = site.data.talks | sort: "year" | reverse %}

{% for talk in talks %}

<div class="post-content">

    <h3>{{ talk.title }}</h3>

    <p class="no-te-pases">
        <a href="{{ talk.workshop-link }}">
            {{ talk.workshop }}
        </a>
    </p>

    <p class="no-te-pases">
        <strong>{{ talk.date }} {{ talk.year }}.</strong>
        {{ talk.place }}
    </p>

    <p class="no-te-pases">

    {% if talk.pdf %}
        <a href="{{ talk.pdf }}" target="_blanck">📄 PDF</a>
    {% endif %}

    {% if talk.slides %}
        {% if talk.pdf %} | {% endif %}
        <a href="{{ talk.slides }}" target="_blanck">🖥 Slides</a>
    {% endif %}

    {% if talk.video %}
        {% if talk.pdf or talk.slides %} | {% endif %}
        <a href="{{ talk.video }}" target="_blanck">▶ Video</a>
    {% endif %}

    </p>

</div>

<hr class="no-te-pases tampoco-te-pases">

{% endfor %}





<h1>Posters</h1>

{% assign talks = site.data.posters | sort: "year" | reverse %}

{% for talk in talks %}

<div class="post-content">

    <h3>{{ talk.title }}</h3>

    <p class="no-te-pases">
        <a href="{{ talk.workshop-link }}">
            {{ talk.workshop }}
        </a>
    </p>

    <p class="no-te-pases">
        <strong>{{ talk.date }} {{ talk.year }}.</strong>
        {{ talk.place }}
    </p>

    <p class="no-te-pases">

    {% if talk.pdf %}
        <a href="{{ talk.pdf }}" target="_blanck">📄 PDF</a>
    {% endif %}

    {% if talk.slides %}
        {% if talk.pdf %} | {% endif %}
        <a href="{{ talk.slides }}" target="_blanck">🖥 Slides</a>
    {% endif %}

    {% if talk.video %}
        {% if talk.pdf or talk.slides %} | {% endif %}
        <a href="{{ talk.video }}" target="_blanck">▶ Video</a>
    {% endif %}

    </p>

</div>

<hr class="no-te-pases tampoco-te-pases">

{% endfor %}



</section>






