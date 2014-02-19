# Sass vs less-css: imports with overrides

## Challenge

Let's admit you have defined some variables in a partial style file and want to override some of their definition in a second partial style file via a sequential import in your `styles.pre-processor`:

    @import "vars";
    @import "vars-overrides";

But some of overridden definitions depends on some other variables:

    /* vars */
    $grey: #ccc;
    $white: #fff;

    /* vars overrides */
    $white: $grey;
    $grey: #fff;

## Expectations

If we define a css rule like:

    a {
        color: $white;
        background-color: $grey;
    }

Once pre-processed, we expect:

    a {
        color: #ccc;
        background-color: #fff;
    }

## Results

Less:

    a {
      color: #cccccc;
      background-color: #cccccc;
    }

Sass:

    a {
      color: #cccccc;
      background-color: white; }

**Sass wins!**
