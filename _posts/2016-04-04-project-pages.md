---
layout: post
title: How to get hyde/lanyon working with project pages
---

Hyde and lanon are two pretty jekyll themes, however to get them working with project pages as opposed to personal pages, some editing
needs to be done. 

## Set baseurl 

First, go to `_config.yml` and edit the content for `url` and `baseurl` like so

```
url:              https://username.github.io
baseurl:          /page/
```

the trailing slash after `page/` is v.important so don't forget it.

## Edit HTML layouts

Next we need to edit a 3 HTML files.

We're going to add the line "{{ site.baseurl }}" which seems to be missing and nececessary 

* *index.html*

First go to index.html and add {{ site.baseurl }} to line 10 (post title href)

```
<h1 class="post-title">
      <a href="{{ site.baseurl }}{{ post.url }}">
```

* *post.html*

Locate post.html in the `layouts` folder.

Add {{ site.baseurl}} to line 17

```
 <h3>
          <a href="{{ site.baseurl }}{{ post.url }}">
```

* *sidebar.html*

Finally, go to sidebar.html in the includes folder and update line 24, adding {{ site.baseurl}} to {{ node.url }}

```
            <a class="sidebar-nav-item{% if page.url == node.url %} active{% endif %}" href="{{ site.baseurl }}{{ node.url }}">{{ node.title }}</a>

```
