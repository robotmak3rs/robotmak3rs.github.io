---
layout: main
---
<main class="home" id="post" role="main" itemprop="mainContentOfPage" itemscope="itemscope" itemtype="http://schema.org/Blog">

<img style="width:100%" src="/assets/img/logo-rc.png">

## Heading 2
<em> Robot makers from around the world who embrace all LEGO robotic platforms (MINDSTORMS, WeDo and BOOST) to MAKE robots, SHARE our passion and INSPIRE generations to come to be interested in Science Technology Engineering Arts and Mathematics via the joys of "playing" with LEGO.

 </em>


    <div id="grid" class="row flex-grid">
    {% for post in site.posts %}
        <article class="box-item" itemscope="itemscope" itemtype="http://schema.org/BlogPosting" itemprop="blogPost">
            <span class="category">
<!--                <a href="{{ site.url }}{{ site.baseurl }}/category/{{ post.category }}">
                    <span>{{ post.category }}</span>
                </a> -->
            </span>
            <div class="box-body">
                {% if post.image %}
                    <div class="cover">
                        <!--{% include new-post-tag.html date=post.date %}-->
                        <a href="{{ post.url | prepend: site.baseurl }}" >
                            <img src="assets/img/placeholder.png" data-url="{{ post.image }}" class="preload">
                        </a>
                    </div>
                {% endif %}
                <div class="box-info">
                    <meta itemprop="datePublished" content="{{ post.date | date_to_xmlschema }}">
                    <time itemprop="datePublished" datetime="{{ post.date | date_to_xmlschema }}" class="date">
              <!--          {% include date.html date=post.date %} -->
                    </time>
                    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
                        <h2 class="post-title" itemprop="name">
                            {{ post.title }}
                        </h2>
                    </a>
                    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
                        <p class="description">{{ post.introduction }}</p>
                    </a>
                    <div class="tags">
                        {% for tag in post.tags %}
                            <a href="{{ site.baseurl}}/tags/#{{tag | slugify }}">{{ tag }}</a>
                        {% endfor %}
                    </div>
                </div>
            </div>
        </article>
    {% endfor %}
    </div>
</main>
