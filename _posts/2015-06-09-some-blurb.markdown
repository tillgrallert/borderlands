---
layout: post
title: "A first blurb to try and play with Jekyll"
date: 2015-06-09 16:45:46 
---
I am currently playing around with jekyll, git and [github pages](https://www.github.com).

# jekyll: dynamic static websites

- we need an up-to-date ruby installation, which might require all sorts of other stuff. Remember that ruby gems are always installed inside the user folder!

- jekyll uses a special flavour of markdown
- [Jekyll](http://jekyllrb.com/). For Windows see: http://jekyllrb.com/docs/windows/ 
- it needs ruby and rubygems, which one might need to install
- jekyll can do both concatanated websites and single pages; can be combined etc. 

- there is static folder "_includes"
	+ footer.html
	+ head.html : containing all the metadata, i.e. <head></head> inside all our websitesc
	+ header.htlm
- "_layouts"
	+ default.html
	+ page.html
	+ post.html

- _config.yml: configures the entire website. It is a dictionary
	+ specify markdown flavour;
		* markdown: kramdown
		* permalink: pretty

## commands

- `$jekyll new`: new project
- `$jekyll build`: creates a folder "_site" using only html and css, which is what then should be pushed to your website
    + `$jekyll build -w` or `$jekyll build --watch`: perpetually checks for changes to the source files and rebuilds the jekyll site in the background
- `$jekyll serve`: starts constant rebuilding and a local server upon which the jekyll website is running


## liquid templating:

- another syntax written inside double curly braces inside our html chunks
- it seems to be a procedural markup: "do something until you find a new command"

## liquid syntax

- there is a great link to the liquid syntax on [github](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers)

{% computing instruction %}
{{ get data }}
| separates the data from a specific command:
    + {{ post.date | date: "%b %-d, %Y" }}

this can be commented out / escape by any standard markdown way of doing this

- how to iterate in liquid
    + {% for %}
    + {% endfor %}
    + example 

    `{% assign i=1 %}
    {% for project in site.data.projects limit:1 offset:i %}
    <p>Link <a href="{{ project.link }}">{{ project.link }}</a></p>
    {% endfor %}`

# Yaml

group similar entries re-using keys with arreys prefixed with a hyphen and a dash:

- day: 1
  name: 
- day: 2
  name:

## yaml data-store: posts

date and title of the post in the file name!

yyyy-MM-dd-title.markdown
