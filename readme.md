# Aviator

API documentation template for Jekyll. Browse through a [live demo](https://tangerine-lemon.cloudvent.net/).
Start documenting your API with this configurable theme.

![Aviator template screenshot](images/_screenshot.png)

Aviator was made by [CloudCannon](http://cloudcannon.com/), the Cloud CMS for Jekyll.
Find more templates and themes at [Jekyll Tips](http://jekyll.tips/templates/).

Learn Jekyll with step-by-step tutorials and videos at [Jekyll Tips](http://jekyll.tips/).

## Features

* Three column layout
* Fully responsive
* Full text search
* Pre-styled components
* Auto-generated navigation based on category
* Optimised for editing in [CloudCannon](http://cloudcannon.com/)
* SEO tags
* Google Analytics

## Setup

1. Add your site and author details in `_config.yml`.
2. Get a workflow going to see your site's output (with [CloudCannon](https://app.cloudcannon.com/) or Jekyll locally).

## Develop

Aviator was built with [Jekyll](http://jekyllrb.com/) version 3.1.6, but should support newer versions as well.

Install the dependencies with [Bundler](http://bundler.io/):

~~~bash
$ bundle install
~~~

Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
$ bundle exec jekyll serve --baseurl ''
~~~

## Editing

Aviator is already optimised for adding, updating and removing documentation pages in CloudCannon.

### Usage

* Each section is a different collection, this helps organise your content.
* Set the order of the collections with the position field in collection configuration in `_config.yml`.
* Set the order of the documents inside a collection by setting the position in front matter.

## Proposing Changes

Proposing changes to the API can be done using github.

1. Create a new branch.
1. Edit the markdown files for the specific endpoints you propose to change
1. Create a pull request into master.
1. Add the `proposed change` label
1. Assign reviewers.
1. After approval, change the label to `unreleased` until the relevant code is released.
1. During this time assign the PR to the documentation team to update PAW and flesh out the additional details. (example requests/responses etc.)
1. After the doc team has completed their work, this branch should be merged coordinated with release of the change.

The file for a particular endpoint is found in the category folder pertaining to the call.
You can see those categories on the left nav in the API documentation (login, organzations, billing, etc.)

Let’s say I wanted to add an api call at ‘/api/export/slap-dusty/’:

I would create a new file called `slap_dusty.md` inside the `_export` folder.

The contents would be:
```
---
title: /api/export/slap-dusty/
name: Slap Dusty
method: get
description: Give dusty a good slap.
---
### Request Parameters:
slap_type
: (string) Slap Type is the type of slap you are giving. e.g. back-handed, open-handed, butt

intensity
: (int) The intensity of the slap. 1-11

### Response Parameters:

uuid
: (string) Universal Unique Identifier for the slap

exclamation
: (string) The sound that came out of Dusty as you slapped him

| Code | Name                   | Meaning                                        |
|------|-------------------------------------------------------------------------|
| 200  | OK                     | Dusty was slapped                              |
| 400  | Bad Request            | You failed at slapping Dusty.                  |
| 401  | Unauthorized           | You haven't told me who you are to slap Dusty. |
| 403  | Permission Denied      | You are not allowed to slap Dusty.             |
| 404  | Not Found              | Dusty is missing                               |
```
Note that type=method. We should change that.
