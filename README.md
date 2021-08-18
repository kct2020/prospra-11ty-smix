# Keith's Heading

Project notes here with original README below. Then I'll rewrite this if it works. Initially, I want to: 
- deploy to Cloudflare Pages. 
Then later:
- add PWA capabilities, including push notifications (OneSignal).
Amend this todo list as project progresses. Adding detailed notes below with latest changes first

## yymm02a Branch3

## yymmddb Branch2

## 210818b 1st Config
Usually, I create a 1st Config branch to get a working site with config changes as per original README instructions and note files changed with any additional notes. Most of this detail is deleted from final README but it serves to keep track of installation progress. I can't find any configuraton notes in the Smix code. But here's what I've found to change so far:
- /src/data/site.json - author info
- /src/layouts/default.liquid - not been personalized so not sure this is right place

So I'll deploy to Cloudflare now, and investigate live site for required changes.

## 210818a Preparation
Notes for my workflow instructions:
- Created new repo (not fork because that seems to imply a commitment to update original which is not my intention for my own starter. Not sure what best practise is)
- Imported https://github.com/hirusi/smix-eleventy-starter
- Renamed LICENSE to LICENSE-smix and used `Add file` to add a BSD-3 LICENSE (see commit notes for reasoning). Note: Github helpfully offers templates when the new filename is LICENSE.

## Original Smix README below...

***

# 🌻 Smix
__A gulp-based starter for Static Site Generators, preconfigured for Eleventy and Forestry CMS.__

## Framework

* __Eleventy__ 0.12.1 out of the box.
  * Date filters for a friendly version such as `10 March 2020`, and ISO8601 (also RFC822 compatible).
  * `getUrl` shortcode similar to Jekyll's `post_url` and `link` liquid tags.
  * Custom rendering engine for HTML files - `Liquid v9`.
    * Adds support for missing filters such as `where` and improves performance.
* __Preconfigured__ for [Forestry CMS](https://forestry.io/) _and_ [Netlify](https://netlify.com/). Find more [instructions in the docs](docs/publishing.md).
* __Indie__ publishing and reading experience.
  * microformats2 support for `h-card`, `h-entry`, and `h-feed` out of the box.
* Modern __JavaScript__.
  * Transpilation via Babel.
    * Support for __ES2015__ JavaScript syntax.
    * Support for __ES2017__ `async`/`await` syntax.
  * Module bundling via Browserify.
* __PostCSS__ as the choice of CSS transpiler.
  * Includes: imports, nesting, purge, minification, autoprefixer.
  * TailwindCSS (v1), configured to strip out unused classes from production builds.
  * Easily build a dark mode using the included `dm` screen type: `dm:bg-gray-900`.
* __SEO__ and other behind-the-scenes goodies.
  * Meta tags for social networks (Open Graph/Twitter).
  * Sitemap with `changeFrequency`; `robots.txt` (please also see [issue #7](https://github.com/hirusi/smix-eleventy-starter/issues/7)).
  * An Atom feed with support for both `published` and `updated` dates on articles.
  * Support for `content-description` meta tag.
* A sane __fonts__ setup.
  * The `font-sans` class is configured to use system-default fonts.
  * Include fonts locally for enhanced privacy of your visitors.
  * `typeset` for professional looking content.
* Minified assets on production.
* __Prettier and editorconfig__ for consistent formatting.
* __Modular gulp task files__ for easy configuration and modification.

## To-Do

* Reload automatically after our assets change (filed [issue here](https://github.com/11ty/eleventy/issues/1125), waiting for response/PR approval). Please reload manually for now.
* System default serif font class.
* Scheduled blog posts.
* Lazy-load images.
* Responsive images.

## How to Use

### Local Development

See [development docs](docs/development.md).

### Staging

`ELEVENTY_ENV` must be set to `staging`. 

* `npm run staging`

### Production

`ELEVENTY_ENV` must be set to `production`.

* `npm run prod`
