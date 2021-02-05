# Base

Knowledge base template for Jekyll.

Base was orignally made by [CloudCannon](http://cloudcannon.com/), the Cloud CMS for Jekyll. Some features has been added to make it suitable to be used as a senseBox Knowledge Base.

## Features

* Tutorials organised by category
* Two types of tutorials - text and video
* Ability to have a "tutorial series"
* FAQ section
* Sticky sidebar for main headings in tutorials

## Setup

1. Add your site and author details in `_config.yml`.
2. Add your Google Analytics, Disqus and MailChimp keys to `_config.yml`.
3. Get a workflow going to see your site's output (with [CloudCannon](https://app.cloudcannon.com/) or Jekyll locally).

## Develop

Base was built with [Jekyll](http://jekyllrb.com/) version 3.4.3, but should support newer versions as well.

Install the dependencies with [Bundler](http://bundler.io/):

~~~bash
$ bundle install
~~~

Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
$ bundle exec jekyll serve
~~~

## i18n

The master contains the german version of the docs and serves [https://docs.sensebox.de]. English is stored in the `EN` branch and serves [https://en.docs.sensebox.de].

## How to add a Document



The sticky sidebar in tutorials in populated by pulling out `<h2> or ##` elements from the content.

### Posts

* Add, update or remove a post in the *Posts* collection.
* The tutorials page is organised by categories.
* use the font-matter to organize your document

```
---
date: 2020-03-11 //Date when created
title: senseBox:home mit LoRa // Title
title_order: 5 //If you want to specify the order of appearance on the main page
categories: sensebox-home-erweiterungen //Name of the category
description: Daten der senseBox:home über LoRa verschicken //Short Description for the overview page
type: Document //Document or Video
set: sensebox-home-general //name of the set. Needs to be the same as the document name
set_order: 3 //
image00: /images/2020-03-11-home-erweiterung-lora/home-lora-00.png //specify images
---
```

Adding a new categories is simple. Just add `categories: category-name` to the font-matter. Please only use small letters and no spaces. If you add a complete new category add a description in the folder `_descriptions`. Follow the given examples. 
* `head` will be used a headline on the overview page
* `description` will appear on the category pages

![include](/images/readme/category.png)


### Post Series
To create a new series:

* Add a new document to the `sets` collection.
* Set the `title` and `description`.

To add a tutorial/post to a series:
* Add a `set` field to the tutorial front matter which points to the file name of the desired set without the `.md` extention. e.g. If I have a set at `_sets/getting-started.md` I would use this in my tutorial front matter: `set: getting-started`.
* Add a `set_order` field to the tutorial front matter and specify a number. This is the tutorials order in the set.

The set will be displayed as the following

![include](/images/readme/set.png)