css-grid-generator
==================

Simple PHP script to generate CSS for a grid

## Installation

This will clone the repository into your bin directory and add a symbolic link
to the `cssgrid` script.

    $ cd ~/bin/
    $ git clone git://github.com/sumpygump/css-grid-generator.git
    $ ln -s css-grid-generator/cssgrid cssgrid

## Requirements

- PHP 5.3+

## Usage

    cssgrid --cols=12 --col-width=67 --gutter=16 --units=percent > grid.css

This will generate the CSS rules for a grid and put them in a file `grid.css`.

### Parameters

    --cols : number of columns
    --col-width : width in pixels of columns
    --gutter : width in pixels of gutter space between columns
    --units : output units (pixels or percent)

## Example Output

```css
/* ---------------------------------------------------------------------
 Grid

 Generated with cssgrid v0.8.1 at 2013-02-12 21:30:54 CST
 https://github.com/sumpygump/css-grid-generator
 cssgrid --units=percent --cols=12 --col-width=67 --gutter=16 --max-width=980

 ============================================
 Formulas used for calculation of grid values
 ============================================
 gutter      = (gutter / max-width) * 100
 col-width   = (((col-width * col-index) + (gutter * (col-index - 1)) / max-width) * 100
 col-push    = (((col-width * col-index) + (gutter * col-index)) / max-width) * 100
 col-pull    = (((col-width * col-index) + (gutter * col-index)) / max-width) * 100 * -1
 col-prefix  = (((col-width * col-index) + (gutter * col-index)) / max-width) * 100
 col-suffix  = (((col-width * col-index) + (gutter * col-index)) / max-width) * 100 * -1
------------------------------------------------------------------------ */
.grid:after {
    content: " ";
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
    margin-left: 1.6326530612245%;
}

.grid-col_1of12 { width: 6.8367346938776%; }
.grid-col_2of12 { width: 15.30612244898%; }
.grid-col_3of12 { width: 23.775510204082%; }
.grid-col_4of12 { width: 32.244897959184%; }
.grid-col_5of12 { width: 40.714285714286%; }
.grid-col_6of12 { width: 49.183673469388%; }
.grid-col_7of12 { width: 57.65306122449%; }
.grid-col_8of12 { width: 66.122448979592%; }
.grid-col_9of12 { width: 74.591836734694%; }
.grid-col_10of12 { width: 83.061224489796%; }
.grid-col_11of12 { width: 91.530612244898%; }
.grid-col_12of12 { width: 100%; }

.mix-grid-col_push1of12 { left: 8.469387755102%; }
.mix-grid-col_push2of12 { left: 16.938775510204%; }
.mix-grid-col_push3of12 { left: 25.408163265306%; }
.mix-grid-col_push4of12 { left: 33.877551020408%; }
.mix-grid-col_push5of12 { left: 42.34693877551%; }
.mix-grid-col_push6of12 { left: 50.816326530612%; }
.mix-grid-col_push7of12 { left: 59.285714285714%; }
.mix-grid-col_push8of12 { left: 67.755102040816%; }
.mix-grid-col_push9of12 { left: 76.224489795918%; }
.mix-grid-col_push10of12 { left: 84.69387755102%; }
.mix-grid-col_push11of12 { left: 93.163265306122%; }
.mix-grid-col_push12of12 { left: 100%; }

.mix-grid-col_pull1of12 { left: -8.469387755102%; }
.mix-grid-col_pull2of12 { left: -16.938775510204%; }
.mix-grid-col_pull3of12 { left: -25.408163265306%; }
.mix-grid-col_pull4of12 { left: -33.877551020408%; }
.mix-grid-col_pull5of12 { left: -42.34693877551%; }
.mix-grid-col_pull6of12 { left: -50.816326530612%; }
.mix-grid-col_pull7of12 { left: -59.285714285714%; }
.mix-grid-col_pull8of12 { left: -67.755102040816%; }
.mix-grid-col_pull9of12 { left: -76.224489795918%; }
.mix-grid-col_pull10of12 { left: -84.69387755102%; }
.mix-grid-col_pull11of12 { left: -93.163265306122%; }
.mix-grid-col_pull12of12 { left: -100%; }

.mix-grid-col_prefix1of12 { margin-left: 8.469387755102%; }
.mix-grid-col_prefix2of12 { margin-left: 16.938775510204%; }
.mix-grid-col_prefix3of12 { margin-left: 25.408163265306%; }
.mix-grid-col_prefix4of12 { margin-left: 33.877551020408%; }
.mix-grid-col_prefix5of12 { margin-left: 42.34693877551%; }
.mix-grid-col_prefix6of12 { margin-left: 50.816326530612%; }
.mix-grid-col_prefix7of12 { margin-left: 59.285714285714%; }
.mix-grid-col_prefix8of12 { margin-left: 67.755102040816%; }
.mix-grid-col_prefix9of12 { margin-left: 76.224489795918%; }
.mix-grid-col_prefix10of12 { margin-left: 84.69387755102%; }
.mix-grid-col_prefix11of12 { margin-left: 93.163265306122%; }
.mix-grid-col_prefix12of12 { margin-left: 100%; }

.mix-grid-col_suffix1of12 { margin-right: 8.469387755102%; }
.mix-grid-col_suffix2of12 { margin-right: 16.938775510204%; }
.mix-grid-col_suffix3of12 { margin-right: 25.408163265306%; }
.mix-grid-col_suffix4of12 { margin-right: 33.877551020408%; }
.mix-grid-col_suffix5of12 { margin-right: 42.34693877551%; }
.mix-grid-col_suffix6of12 { margin-right: 50.816326530612%; }
.mix-grid-col_suffix7of12 { margin-right: 59.285714285714%; }
.mix-grid-col_suffix8of12 { margin-right: 67.755102040816%; }
.mix-grid-col_suffix9of12 { margin-right: 76.224489795918%; }
.mix-grid-col_suffix10of12 { margin-right: 84.69387755102%; }
.mix-grid-col_suffix11of12 { margin-right: 93.163265306122%; }
.mix-grid-col_suffix12of12 { margin-right: 100%; }
```

## How to Use in HTML

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <!-- META DATA -->
        <meta charset="utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <meta name="MSSmartTagsPreventParsing" content="true" />
        <meta http-equiv="imagetoolbar" content="no" />
        <!--[if IE]><meta http-equiv="cleartype" content="on" /><![endif]-->

        <!-- SEO -->
        <title>Demo Grid</title>
        <meta name="description" content="" />
        <meta name="author" content="" />

        <!-- STYLESHEETS -->
        <link rel="stylesheet" media="screen, projection" href="grid.css" />
        <style>
            body { background-color: #eeeeec; }
            .wrapper { width: 980px; margin: 0 auto; }
            .box {
                height: 100px;
                padding-top: 20px;
                margin-bottom:16px;
                background-color: #e9b96e;
                color: #ce5c00;
                border: 2px solid #204a87;
                text-align: center;
            }
        </style>
    </head>
<body>
    <div class="wrapper">
        <div class="grid">
            <div class="grid-col grid-col_8of12">
                <div class="box">COL 1 (8of12)</div>
            </div>
            <div class="grid-col grid-col_2of12">
                <div class="box">COL 2 (2of12)</div>
            </div>
            <div class="grid-col grid-col_2of12">
                <div class="box">COL 3 (2of12)</div>
            </div>
        </div>
        <div class="grid">
            <div class="grid-col grid-col_8of12">
                <div class="box">COL 1 (8of12)</div>
            </div>
            <div class="grid-col grid-col_2of12 mix-grid-col_push2of12">
                <div class="box">COL 2<br />push --&gt;</div>
            </div>
            <div class="grid-col grid-col_2of12 mix-grid-col_pull2of12">
                <div class="box">COL 3<br />&lt;-- pull</div>
            </div>
        </div>
        <div class="grid">
            <div class="grid-col grid-col_2of12 mix-grid-col_prefix6of12">
                <div class="box">COL 1 (2of12)<br />|-- prefix6of12</div>
            </div>
            <div class="grid-col grid-col_2of12">
                <div class="box">COL 2 (2of12)</div>
            </div>
            <div class="grid-col grid-col_2of12">
                <div class="box">COL 3 (2of12)</div>
            </div>
        </div>
        <div class="grid">
            <div class="grid-col grid-col_2of12">
                <div class="box">COL 1 (2of12)</div>
            </div>
            <div class="grid-col grid-col_2of12">
                <div class="box">COL 2 (2of12)</div>
            </div>
            <div class="grid-col grid-col_2of12 mix-grid-col_suffix6of12">
                <div class="box">COL 3<br />suffix6of12 --|</div>
            </div>
        </div>
    </div>
</body>
</html>
```
