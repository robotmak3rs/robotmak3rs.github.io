---
layout: main
---
<main class="home" id="post" role="main" itemprop="mainContentOfPage" itemscope="itemscope" itemtype="http://schema.org/Blog">

<img style="width:100%" src="/assets/img/rm3-logo-blk.jpg">

<html>


<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
* {
    box-sizing: border-box;
}

.column {
  float: left; 
   width: 14.2857142857%;
padding: 5px 0px 0px 5px; 
}

.row:after {
    content: "";
    display: table;
    clear: both;
}

@media screen and (max-width: 600px) {
    .column {
        width: 100%;
        padding: 5px 100px 5px 100px;
    }


</style>
</head>

<body>




<style>
a:link {
    color: #5b82af;
    background-color: transparent;
    text-decoration: none;
}

a:visited {
    color: #5b82af;
    background-color: transparent;
    text-decoration: none;
}

a:hover {
    color: #2395E4;
    background-color: transparent;
    text-decoration: none;
}

a:active {
    color: #5b82af;
    background-color: transparent;
    text-decoration: none;
}
</style>
<div style="margin-left:15%;margin-right:15%">
<h3 style="text-align: center;">This page is dedicated to robot makers from around the world who embrace all LEGO robotic platforms (MINDSTORMS Legacy & Robot Inventor, SPIKE Prime, WeDo, BOOST and PoweredUp) to MAKE robots, SHARE the passion and INSPIRE generations to come! Showcasing interest in Science, Technology, Engineering, Arts, and Mathematics via the joys of "playing" with LEGO. 

</h3>
</div>
<div class="row">

  <!--<div class="column">

</div>-->

  <div class="column" >
  <center><a href="https://www.facebook.com/groups/mindstormsrobotinventor/"><img style="width:50%" src="/assets/img/LMS-fb.png"></a></center>
  <a href="https://www.facebook.com/groups/mindstormsrobotinventor/"><h3 style="text-align: center;">MINDSTORMS 51515</h3></a>
  </div>
  <div class="column">
  <center><a href="https://www.facebook.com/groups/legomindstorms/"><img style="width:50%" src="/assets/img/EV3-fb.png"></a></center>
  <a href="https://www.facebook.com/groups/legomindstorms/"><h3 style="text-align: center;">MINDSTORMS Legacy</h3></a>
  </div>
  <div class="column">
  <center><a href="https://www.facebook.com/groups/SPIKEcommunity/"><img style="width:50%" src="/assets/img/Spike-fb.jpg"></a></center>
  <a href="https://www.facebook.com/groups/SPIKEcommunity/"><h3 style="text-align: center;">SPIKE Prime</h3></a>
  </div>
  <div class="column">
  <center><a href="https://www.facebook.com/groups/letsdowedo/about/"><img style="width:50%" src="/assets/img/WeDo-fb.png"></a></center>
  <a href="https://www.facebook.com/groups/letsdowedo/about/"><h3 style="text-align: center;">WeDo</h3></a>
  </div>
  <div class="column">
  <center><a href="https://www.facebook.com/groups/BOOSTcommunity/"><img style="width:50%" src="/assets/img/BOOST-fb.png"></a></center>
  <a href="https://www.facebook.com/groups/BOOSTcommunity/"><h3 style="text-align: center;">BOOST</h3></a>
  </div>
  <div class="column">
  <center><a href="https://www.facebook.com/groups/1901917436776385/"><img style="width:50%" src="/assets/img/PoweredUp-fb.jpg"></a></center>
  <a href="https://www.facebook.com/groups/1901917436776385/"><h3 style="text-align: center;">PoweredUp</h3></a>
  </div>
   <div class="column">
  <center><a href="http://www.thenxtstep.com/"><img style="width:50%" src="/assets/img/rm3-fb.png"></a></center>
  <a href="http://www.thenxtstep.com/"><h3 style="text-align: center;">Our blog</h3></a>
	</div>
</div>



<div style="padding: 20px 20px 20px 20px;"><h2 style="text-align: center;"> Meet the Members of the ROBOTMAK3RS Community</h2></div>



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
                <!--    <time itemprop="datePublished" datetime="{{ post.date | date_to_xmlschema }}" class="date">
                        {% include date.html date=post.date %}
                    </time>-->
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
