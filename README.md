# ll-kss

Lincoln Loop's default [kss-node](https://github.com/kss-node/kss-node) style guide template.

## Setup

Make sure you [read the docs](http://kss-node.github.io/kss-node/) for kss-node!

First, clone ll-kss. Your cloned version does not need to live within your project.

Next, we recommend setting up an example kss-node configuration file, typically named `kss-config.json`. An example configuration file looks like this:

    {
      "//": "The title of your style guide. Used in page titles and in the guide header."
      "title": "Title of my Style Guide",
      "//": "Where to look for CSS/Scss/Less/whatever that you're parsing"
      "source": "client/scss",
      "//": "The directory where the guide will be built."
      "destination": "build/styleguide",
      "//": "The path to the template you're building from. In this case, ll-kss."
      "template": "ll-kss",
      "//": "The CSS file that represents your project's styles."
      "css": [
        "/static/css/screen.css"
      ],
      "//": "Show lots of logging!"
      "verbose": true
    }

kss-node looks for a Markdown file named `styleguide.md` that represents the homepage of the guide. This file needs to be in the `source` directory mentioned above. Alternatively, you can add `homepage` to the `kss-config.json` file and pass in the path. The point is, don't forget this file!

## Building the Guide

Lastly, you can compile the style guide as follows:

    kss-node --config kss-config.json

## Compiling ll-kss Scss

You'll need to run `npm install` to build the dependencies needed to compile Scss. After doing this, simply run:

    npm run compile-scss

This will generate the `kss.css` file needed to render styles for the guide.
