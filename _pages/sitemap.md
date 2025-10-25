---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

{% include base_path %}

A list of all the posts and pages found on the site. For you robots out there, there is an [XML version]({{ base_path }}/sitemap.xml) available for digesting as well.

<h2>Pages</h2>
{% for post in site.pages %}
  {% if post.path contains '_pages/' %}
    {% unless post.title == nil or post.title == "" or post.published == false %}
      {% include archive-single.html %}
    {% endunless %}
  {% endif %}
{% endfor %}


{% for collection in site.collections %}
  {% unless collection.output == false or collection.label == "posts" %}
    {% assign has_docs = false %}
    {% for d in collection.docs %}
      {% unless d.title == nil or d.title == "" or d.published == false %}
        {% assign has_docs = true %}
        {% break %}
      {% endunless %}
    {% endfor %}

    {% if has_docs %}
      <h2>{{ collection.label }}</h2>
      {% for post in collection.docs %}
        {% unless post.title == nil or post.title == "" or post.published == false %}
          {% include archive-single.html %}
        {% endunless %}
      {% endfor %}
    {% endif %}
  {% endunless %}
{% endfor %}
