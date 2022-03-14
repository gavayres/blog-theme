---
permalink: /notes/
title: Notes
---
<html>
<head>
    <title>Gavin Ayres</title>
    <meta charset='UTF-8'>
    <meta content='width=device-width, initial-scale=1' name='viewport'/>

    <meta name='description' content='Masters student at Southampton.'>
    <!-- A decent browser will parse this fine:
         https://webmasters.stackexchange.com/questions/92744. -->
    <meta name='keywords' content='
        machine learning,
        statistical machine learning,
        bayesian inference,
        statistics,
        computational statistics,
        linear algebra,
        numerical linear algebra,
        statistical software,
        deep learning,
        computer science
    '>
    <meta name='author' content='Gavin Ayres'>

    <link rel='shortcut icon' href='/favicon.png?v=e' />
    <link href='/css/blog.css' rel='stylesheet'/>

    {% include mathjax.html %}
</head>
<body>
    <div id='notes' class='wrap'>
        <div id='intro'>
            <div class='quote'>
                <p>"Your talk," I said, "is surely the handiwork of wisdom because not one word of it do I understand."</p>
                <a href='https://www.goodreads.com/author/quotes/15248.Flann_O_Brien' target='_blank'>Flann O'Brien</a>
            </div>
        </div>
        <div id='study_notes' class='section'>
            {% for note in site.notes %}
                <div class='note-row'>
                    <p class='note-title'>
                        <a href="{{ note.url }}">
                            {{ site.baseurl }}{{ note.title }}
                        </a>
                    </p>
                    <p class='note-date'>
                        {{ note.date | date_to_long_string }}
                    </p>
                </div>
                <p class='note-subtitle'>
                    {{ note.subtitle }}
                </p>
                <span class='hidden'>{{ forloop.index }}</span>
            {% endfor %}
        </div>
    </div>
</body>
</html>
