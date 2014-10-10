# Responsive Favicon Experiment

This is an experimental "responsive favicon" implementaiton using Web Components

What I wanted to do:

- Create responsive favicon component that can be declaratively defined.
- Changes favicon size depending on device pixel ratio

## How to use

1. Prepare an `img` folder with multiple sized favicon images. Images should be preceded with `_16x16`, `_24x24`, `_32x32` respectively targeting on each device pixel ratio.
    - dpr = 1.0: `_16x16`  
      ex) `favicon_16x16.png`
    - dpr = 1.5: `_24x24`.png  
      ex) `favicon_24x24.png`
    - dpr = 2.0: `_32x32`.png  
      ex) `favicon_32x32.png`

2. Define base url for a favicon so it will be replaced with relevant image url

    <link is="responsive-favicon" href="img/favicon_16x16.png">

    - Use `link` tag
    - Add `is` attribute with value of `responsive-favicon`
    - `href` attribute represents image file name
    - `_16x16` portion will be replaced with something else depending on device pixel ratio

## How to try this demo
- Download this repository (I won't register this to bower registry)
- Run `bower install`
- Launch a local server, then access `index.html`
