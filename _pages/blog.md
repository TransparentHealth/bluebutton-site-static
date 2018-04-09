---
layout: post_with_category
title:  "Blue Button Blog"
date:   2018-03-26 23:46:00 -0500
description: The Blue Button Blog for Developers using Blue Button 2.0 API.
landing-page: live
gradient: "blueberry-lime-background"
subnav-link-gradient: "blueberry-lime-link"
categories: general
badge: blog
permalink: "/blog/"
---

{% for post in site.posts %}

<h1><a href="{{ post.url }}" class="ds-u-display--block" >{{ post.title }}</a></h1>
  
{{ post.excerpt }}
  
{% endfor %}