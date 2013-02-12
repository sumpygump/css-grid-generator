css-grid-generator
==================

Simple PHP script to generate CSS for a grid based in inputs similar to gridinator.com

## Installation

This will clone the repository into your bin directory and add a symbolic link
to the `cssgrid` script.

    $ cd ~/bin/
    $ git clone git://github.com/sumpygump/css-grid-generator.git
    $ ln -s css-grid-generator/cssgrid

## Usage

    cssgrid --cols=12 --col_width=64 --gutter=16 --margin=10 --output=percent > grid.css

This will generate the CSS rules for a grid and put them in a file `grid.css`.

### Parameters

    --cols : number of columns
    --col_width : width in pixels of columns
    --gutter : width in pixels of gutter space between columns
    --margin : margin of grid container
    --output : output type (pixels or percent)

## Example Output

    /* ---------------------------------------------------------------------
     Grid
     Generated with cssgrid v0.5 at 2013-02-12 00:53:58
     cssgrid --cols=12 --col_width=64 --gutter=16 --margin=10 --output=percent
    ------------------------------------------------------------------------ */
    .grid:after {
        content: ".";
        display: block;
        height: 0;
        clear: both;
        visibility: hidden;
    }

    .grid-col {
        position: relative;
        float: left;
    }

    .grid-col + .grid-col {
        margin-left: 16px;
    }

    .grid-col_1of12 { width: 6.7796610169492%; }
    .grid-col_2of12 { width: 14.618644067797%; }
    .grid-col_3of12 { width: 22.457627118644%; }
    .grid-col_4of12 { width: 30.296610169492%; }
    .grid-col_5of12 { width: 38.135593220339%; }
    .grid-col_6of12 { width: 45.974576271186%; }
    .grid-col_7of12 { width: 53.813559322034%; }
    .grid-col_8of12 { width: 61.652542372881%; }
    .grid-col_9of12 { width: 69.491525423729%; }
    .grid-col_10of12 { width: 77.330508474576%; }
    .grid-col_11of12 { width: 85.169491525424%; }
    .grid-col_12of12 { width: 93.008474576271%; }

