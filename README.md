CompressJS
==========

This a Jekyll module based off of donaldducky's [CssMinify](https://github.com/donaldducky/jekyll-cssminify) for use with the static site generator [Jekyll](http://jekyllrb.com). The module minifies and concatenates _js/main.js and any listed dependencies (see below) as _site/js/main.min.js. This plugin came about because we already liked using [jekyll-sass](https://github.com/noct/jekyll-sass) for CSS, and we could only find minification/concatenation plugins that handled both JS and CSS assets.

## Installation

1. Install [Jekyll](http://jekyllrb.com) and [Juicer](https://github.com/cjohansen/juicer).
1. Place the compressjs.rb plugin into your `<root>/_plugins` directory so that Jekyll can load it
1. Create a new path for unminified javascript `<root>/_js`.
1. Create a main js file in `_js` folder named `main.js`. To include other files in the minification/concatenation process, follow Juicer's [@depend syntax](https://github.com/cjohansen/juicer). 
1. Use the following to load the optimized script file: `<script type="text/javascript" src="{% minified_js_file %}"></script>`
1. Compile your site with `jekyll`