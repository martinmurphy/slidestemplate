# Presentation: Slides Template

This is a template for setting up a slides presentation. The slides are written in MarkDown and processed by reveal-md/reveal.js, and can then be displayed in a web browser with reveal.js handling the navigation and transitions. 

I wanted to keep the slide creation simple, focus on content rather than formatting.  I like that markdown can be editted and read using any text editor.  I didn't like that, in order to reveal.js, all of reveal.js would be included in the source of the presentation. Hence using reveal-md, just point it at a markdown file and it can generate a static website using reveal.js.
Then rather than having to commit the generated static site to the source of the presentation, it's wired up to use TravisCI to run the site generation step and then push the generated site back to the GitHub Pages branch at the project site

The [`.travis.yml`](.travis.yml) file should work, if you setup a travis build of the project and add an environment variable in the Travis settings, `GITHUB_TOKEN`, whose value should be a personal access token generate in the GitHub Developer Settings.

To make a presentation:
*  fork the repo
*  setup a build in travis for the fork (with the environment variable `GITHUB_TOKEN` set to your personal access token)
*  edit the slides.md file with your slides content
*  push to github
*  view presentation on GitHub in the project pages for your repo (or serve it locally)

[Presentation](https://martinmurphy.github.io/slidestemplate)

# Usage

Install reveal-md
```
npm install
```
then to serve and open the presentation in a browser
```
npm run presentation
```
or to generate a static website in the `docs` subdirectory
```
npm run generate
```

This presentation uses [reveal-md](https://github.com/webpro/reveal-md) which uses [reveal.js](http://lab.hakim.se/reveal-js)

Built and deployed to [GitHub Pages](https://pages.github.com) using [Travis CI](https://travis-ci.org)

[![Build Status](https://travis-ci.org/martinmurphy/slidestemplate.svg?branch=master)](https://travis-ci.org/martinmurphy/slidestemplate)


