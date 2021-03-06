# Crux Connect API Docs

Jekyll built and Github Pages hosted [API documentation](https://docs.cruxconnect.com)
and [Internal API documentation](https://docs.cruxconnect.com/internal/)

## Features

* Three column layout
* Fully responsive
* Auto-generated navigation based on category

## Develop
Crux Docs were built with [Jekyll](http://jekyllrb.com/) version 3.1.6, but should support newer versions as well.

Install the dependencies with [Bundler](http://bundler.io/):

~~~bash
$ bundle install
~~~

Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
$ bundle exec jekyll serve
~~~

## Editing

The source of each documented public endpoint is in the [Paw file](/files/Crux-API-Project.paw).

Internal endpoints are documented in the [Internal Paw file](/files/Internal_Crux_API-Project.paw).

The description contains the human readable notes and the code is generated from Paw.
Any changes are made there.
The [Crux Aviator Generator](https://github.com/CruxConnect/paw-aviator-extension)
extension is then used to generated the markdown file for each endpoint.

### Usage

* Endpoints are organizaed in collections based upon domain
* Set the order of the collections with the position field in collection configuration in `_config.yml`.
* Set the order of the documents inside a collection by setting the position in front matter.
* Messages may be added to the documentation with the following classes: `info`, `error`, `success`, `warning`

### Pages

There are several different documentation pages:

* `/` - The general public API documentation
* `/internal/` - The internal "undocumented" (unsupported) API documentation
* `/file-specs/` - Specifications for the "Crux Blessed" feed formats

### Visibility

Each collection or endpoint should have a `visiblity` setting.

The possible choices are:

* `all` - Item will appear on all pages
* `api` - Item will appear on both public facing `/` and internal `/internal/` pages
* `public` - Item will appear only on public facing `/` page
* `internal` - Item will appear only on `/internal/` page
* `file-specs` - Item will appear only on `/file-spec/` page

Any other value will cause the item to be hidden.

## Proposing API Changes

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

Let’s say I wanted to add an api call at ‘/export/slap-dusty/’:

I would create a new file called `slap_dusty.md` inside the `_export` folder.

The contents would be:
```
---
title: /export/slap-dusty/
name: Slap Dusty
method: get
visibility: public
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

### Expected Response Codes:
| Code | Name                   | Meaning                                        |
|------|-------------------------------------------------------------------------|
| 200  | OK                     | Dusty was slapped                              |
| 400  | Bad Request            | You failed at slapping Dusty.                  |
| 401  | Unauthorized           | You haven't told me who you are to slap Dusty. |
| 403  | Permission Denied      | You are not allowed to slap Dusty.             |
| 404  | Not Found              | Dusty is missing                               |
| 409  | Critical               | Dusty is not a supplier                        |
| 500  | Internal Server Error  | Dusty did something unexpected                 |

{% include links/response_codes.md %}
```

Note: Only document response codes in a table in the endpoint md file when they mean something special.
