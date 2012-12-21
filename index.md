---
layout: page
title: 
tagline: Supporting tagline
---
{% include JB/setup %}

小站使用[Jekyll Bootstrap](http://jekyllbootstrap.com)博客平台,并托管在[GitHub](www.github.com)上.这里的文章除了注明转载外,皆为原创,       
同时我也会发表在我的[博客园](www.cnblogs.com/xdao)上,所有文章采取"署名-非商业性使用-相同方式共享 3.0"协议.


<div class="content-cnt">
<div class="ui-grid-25 ui-grid-right content-top">	
	<div class="ui-grid-23 violet-post clearfix">
        <div class="violet-post-det clearfix">
    <div class="ui-grid-16 violet-journal">
        <h4 class="v-section-tit">Last Journal</h4>
        {% for rpost in site.posts limit:5 %}
        <article class="v-excerpt clearfix">
            <div class="ui-grid-7 ui-grid-bottom">
                <h3 class="v-excerpt-title"><a href="{{ rpost.url }}" title="{{ rpost.title }}" rel="bookmark">{{ rpost.title }}</a></h3>
                <p class="v-date"><span>&#8227;</span><time pubdate="{{ rpost.date | date_to_utc | date: '%Y-%m-%d' }}">{{ rpost.date | date_to_utc | date: "%Y-%m-%d" }}</time></p>
            </div>
            <div class="ui-grid-9 ui-grid-right v-excerpt-det">
                <p>{{ rpost.description }}</p>
                <p class="v-more"><a href="{{ rpost.url }}" title="Read More" rel="nofollow"><span>&#10149;</span>Read More</a></p>
            </div>
        </article><!-- //v-post-excerpt -->
        {% endfor %}
        {% for npost in site.posts limit:3 offset:5  %}             
        <article class="v-post-list fn-clear">
            <p class="v-date"><span>&#8227;</span><time pubdate="{{ npost.date | date_to_utc | date: '%Y-%m-%d' }}">{{ npost.date | date_to_utc | date: "%Y-%m-%d" }}</time></p>
            <h3 class="v-post-title"><a href="{{ npost.url }}" title="{{ npost.title }}" rel="bookmark">{{ npost.title }}</a></h3>
        </article><!-- //v-post-list -->
        {% endfor %}
    </div><!-- //Journal -->
    
    {% include JB/aside.html %}
    </div>
    </div>
</div>
</div>


