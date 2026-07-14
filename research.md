---
layout: default
title: Research
permalink: /research/
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
    <h1>Research</h1>
<section class="post-content">
    <h2>Publications</h2>

    <ol class="publications">
    {% for paper in site.data.papers %}
        <li class="publication">

            {{ paper.authors | join: " and " }},
            "{{ paper.title }}",

            {% if paper.journal %}
                <em>{{ paper.journal }}</em>
            {% endif %}

            {% if paper.volume %}
                {{ paper.volume }}
            {% endif %}

            {% if paper.number %}
                ({{ paper.number }})
            {% endif %}

            {% if paper.pages %}
                , {{ paper.pages }}
            {% endif %}

            {% if paper.year %}
                ({{ paper.year }}).
            {% endif %}

            {% if paper.arxiv %}
                <a href="https://arxiv.org/abs/{{ paper.arxiv }}" target="_blank">arXiv:{{ paper.arxiv }}</a>.
            {% endif %}

            {% if paper.doi %}
                DOI: <a href="https://doi.org/{{ paper.doi }}" target="_blank">{{ paper.doi }}</a>.
            {% endif %}

        </li>
    {% endfor %}
    </ol>

</section>
