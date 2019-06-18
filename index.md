---
layout: home
---

<div class="index-content blog">
    <div class="section">
        <ul class="artical-cate">
            <li class="on"><a href="/"><span>随笔</span></a></li>
            <li style="text-align:center"><a href="/technical"><span>技术</span></a></li>
            <li style="text-align:right"><a href="/project"><span>项目</span></a></li>
        </ul>

        <div class="cate-bar"><span id="cateBar"></span></div>

        <ul class="artical-list">
        {% for post in site.categories.essay %}
            <li>
                <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
                <div class="title-desc">{{ post.description }}</div>
            </li>
        {% endfor %}
        </ul>
    </div>
    <div class="aside">
    </div>
</div>
<iframe width="980" height="410" src="https://mars.nasa.gov/layout/embed/send-your-name/mars2020/certificate/?cn=838474548443" frameborder="0"></iframe>