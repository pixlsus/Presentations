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

## Logos

Relevant [PIXLS.US logo/image assets][Logos].
These are `.svg` files - the default slate blue is the current background to the logo on the site, and is: `#778899`.  The background can also be set to white `#FFFFFF` as appropriate for the medium.

The foreground color for the logo/text is _not_ black.  It's a dark gray: `#323232` RGB(50,50,50).

[Logos]: ./Logos

<a href="https://github.com/pixlsus/Presentations/blob/master/Logos/pixls.us-logo-url.svg">
<img src="https://pixls.us/images/pixls.us-logo-250px.png" alt="PIXLS.US url Logo" width="100" height="100" >
</a>

## Typography

The font used for the logo is [Arvo][] (by [Anton Koovit][koovit]).

[Arvo]: https://www.google.com/fonts/specimen/Arvo
[koovit]: https://profiles.google.com/110835161102775862873/about


### The League of Movable Type

[The League of Movable Type][lmt] ([github](https://github.com/theleagueof)) has various font faces of note that have been used in the past, including:

* [League Gothic][] ([github](https://github.com/theleagueof/league-gothic))
* [Ostrich Sans][] ([github](https://github.com/theleagueof/ostrich-sans))
* [Raleway][] ([github](https://github.com/theleagueof/raleway))

The larger, bolder type is [League Gothic][] and the lighter sans-serif font is often [Ostrich Sans][]. Both of these are used in the LGM2015 State of the Libre Graphics presentation slides.

[League Gothic]: https://www.theleagueofmoveabletype.com/league-gothic
[Ostrich Sans]: https://www.theleagueofmoveabletype.com/ostrich-sans
[lmt]: https://www.theleagueofmoveabletype.com/
[Raleway]: http://theleagueofmoveabletype.com/raleway

## Templates

The templates directory contains a reveal.js from the current (at the time of writing) git version of pandoc, as the version of the template shipping in Fedora 23's version of pandoc has a slight bug in it. We welcome new pandoc templates!

It'd be awesome to have a slide transition that is an aperture closing then opening.

## Upcoming

List of upcoming presentations/talks
* [LGM2016 - _PIXLS.US – Building a Freedom Based Photography Community_](/LGM2016_PIXLS.US/)
    * April 15-18, 2016
    * University of Westminster, Harrow, London
    * [website](http://www.libregraphicsmeeting.org/2016/)
    * [proposal](/LGM2016_PIXLS.US/proposal.md)
    * status: accepted


## Delivered

* [Libre Graphics Meeting 2015 - _State of the Libre Graphics_][lgm2015]
    Delivered by pippin on behalf of Pat David/pixls community.
    * [website]: http://www.libregraphicsmeeting.org/2015/

[lgm2015]: /LGM2015_State_Of
