---
layout: default
---
<!-- Main -->
<div id="main" class="wrapper style1">
    <div class="container">
        <header class="major">
            <h2>Welcome to Open Lab?</h2>
            <p>Open Lab is a weekly meeting for developers who are interested in learning technology, sharing experiences or simple code for a couple of hours after work.</p>
        </header>
    </div>
</div>
<!-- Content -->
{% for post in site.posts %}
{% if post.highlighted == true %}
<!-- Five -->
<section id="five" class="wrapper style2 fade">
    <div class="container">
        <h3><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h3>
        {{ post.excerpt }}
    </div>
    <section class="special">
            <ul class="actions">
                <li><a href="{{ site.baseurl }}{{ post.url }}" class="button">Read more</a></li>
            </ul>
    </section>
</section>
{% endif %}
{% endfor %}
{% for post in site.posts %}
{% if post.highlighted != true %}
<section id="content">
    <div class="wrapper style1">
        <div class="container">
            <h3><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h3>
            {{ post.excerpt }}
        </div>   
    </div>
    <section class="special">
        <ul class="actions">
            <li><a href="{{ site.baseurl }}{{ post.url }}" class="button">Read more</a></li>
        </ul>
    </section>
</section>
{% endif %}
{% endfor %}
