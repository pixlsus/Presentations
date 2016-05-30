# Presentations

Talks, slides, assets for presenting information about free software photography

## Overview

This repo contains a set of slides that you can use and customize to help you give presentations about free software for photographers.

These slides are made such that you can build your presentation using [pandoc](http://pandoc.org/README.html#synopsis).

You can assemble your slides by copying and pasting content into a master file or using a utility like `cat` to get everything in one file.

For example, to make one big file out of all of the slides currently in this repo:

    cat title.md \
    what_is_free_software.md \
    free_software_advantages.md \
    available_tools.md \
    what_is_pixls.md \
    contribute.md \
    software_support.md \
    these_slides_are_free_software.md > all_the_slides.md

Then use pandoc to convert to a slide format:

    pandoc --template=Template/default.revealjs -V theme=simple -t revealjs -o index.html all_the_slides.md

This use the HTML-based [reveal.js](https://github.com/hakimel/reveal.js). Clone down the repo for reveal.js:

     git clone https://github.com/hakimel/reveal.js

Now start a webserver (requires python 2.7):

    python2 -m SimpleHTTPServer

And point your browser to `http://localhost:8000`.

If you want that all in one command:

    git clone https://github.com/hakimel/reveal.js && \
    cat title.md \
    what_is_free_software.md \
    free_software_advantages.md \
    available_tools.md \
    what_is_pixls.md \
    contribute.md \
    software_support.md \
    these_slides_are_free_software.md \
    | pandoc --template=Template/default.revealjs -V theme=simple -t revealjs -o index.html -s && \
    python2 -m SimpleHTTPServer && \
    firefox http://localhost:8000

## Templates

The templates directory contains a reveal.js from the current (at the time of writing) git version of pandoc, as the version of the template shipping in Fedora 23's version of pandoc has a slight bug in it. We welcome new pandoc templates!

It'd be awesome to have a slide transition that is an aperture closing then opening.
