




<h1 align="center">Zee</h1>
<div align="center">Free, simple, efficient landing page builder.</div>

## [Read intro, features & benefits here &rarr;](http://bdavidxyz.github.io/zee)

## Quickstart

### Prerequisite


 - [Ruby](https://www.ruby-lang.org/en/downloads/) - use the installer
 - [Jekyll](https://jekyllrb.com/) - ```$ gem install jekyll```
 - [NodeJS](https://nodejs.org/en/download/) - use the installer.
 - [GulpJS](http://gulpjs.com/GulpJS) - ```$ npm install -g gulp ```

Tested with : node 5.11.1, npm 3.8.6, gulp 3.9.1, jekyll 3.1.6, ruby 2.3.0

### Develop


```shell

$ git clone https://github.com/bdavidxyz/zee
$ cd zee
$ npm install
$ gulp
 # The browser launches itself,
 # and will rebuild and live-reload each time you
 # change a file
```

Change text inside _includes/ownhtml/own-hero0.html.

The change should reflect in the browser immediately.

### Deploy

The tool comes with a prebuilt command to deploy to github pages : it's free.

```shell

$ gulp deploy
 # You can view and share your website at https://github.com/<your_github_name>/<your_github_repo>
```


## Sections

### What it is

A section is a part of a landing page : pricing table, testimonial, our team, etc.

Each section has many designs, so that can choose the one you prefer. For example :

 - Designs of pricing tables : pricingtable0, pricingtable1, pricingtable2, etc
 - Designs of testimonials   : testimonial0, testimonial1, testimonial2, etc

For a given design, there are 3 file, for example : 
 - _includes/ownhtml/pricingtable0.html (HTML is mantory)
 - _sass/owncss/pricingtable0.scss (CSS file may or may not be required)
 - _includes/ownjs/pricingtable0.js.html (JS file, may or may not be required)

**⚠️ You must include all needed files (min 1 - max 3) for a given section (see below)⚠️**


### How to include a section

Example with pricingtable0.

Inclusion of html : in file **index.html**

```html
  <!--include HTML section here, 
  don't forget to include SCSS and JS 
  for a given section, if apply-->
  {% include ownhtml/pricingtable0.html %}
```

Inclusion of css (if apply) : in file **css/main.scss**

```css
//Import SCSS of sections here
@import "owncss/pricingtable0";
```

Inclusion of js  (if apply) : in file **_layout/default.html**

```js
    <!--startjs-->
      {% include ownjs/pricingtable0.js.html %}
    <!--endjs-->
```
(put the line right above the endjs comment to allow 3rd party lib to load first)
