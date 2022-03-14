---
permalink: /blog
title: Blog
---
Insert blogs here.

{% include nav.html %}
    <div id='blog' class='wrap'>
        <div id='intro'>
            <div class='quote'>
                <p>I learned very early the difference between knowing the name of something and knowing something.</p>
                <a href='https://en.wikiquote.org/wiki/Richard_Feynman' target='_blank'>Richard Feynman</a>
            </div>
        </div>
        <div id='posts' class='section'>
            {% for post in site.posts %}
                <div class='post-row'>
                    <p class='post-title'>
                        <a href="{{ post.url }}">
                            {{ post.title }}
                        </a>
                    </p>
                    <p class='post-date'>
                        {{ post.date | date_to_long_string }}
                    </p>
                </div>
                <p class='post-subtitle'>
                    {{ post.subtitle }}
                </p>
                <span class='hidden'>{{ forloop.index }}</span>
            {% endfor %}
        </div>
    </div>