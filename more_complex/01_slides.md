!SLIDE 

A Bit More Complex
==================

Working with Multiple Files
---------------------------

    site.scss, site.sass
    site.css.scss, site.css.sass

!SLIDE 

Store in a `./lib` Sub-directory of the Sass files

Partials start with an underscore e.g. `_nav.scss`  
and are imported in the following way

    @import "lib/nav";
    @import "nav";

!SLIDE 

Mixins
------

    @mixin wrap($wrap-width) {
      margin: 0 auto;
      overflow: hidden;
      text-align: left;
      max-width: $wrap-width;
    }
    
    #wrapper {
      @include wrap(960px);
    }

!SLIDE 

Selector Inheritance
--------------------

    .clearfix { 
      …
      &:after {
        …
      }
    }
    
    .main {
      @extend .clearfix
    }

!SLIDE code

    .clearfix, .main {
      …
    }
    .clearfix:after, .main:after {
      …
    }
    .main {
      …
    }

!SLIDE 

Branching/Conditionals/Etc.
---------------------------

[From the Compass Project](http://compass-style.org/reference/compass/css3/text-shadow/ "Compass Text Shadow | Compass Documentation")

!SLIDE code smaller

    @mixin single-text-shadow(  ↵
      $color: $default-text-shadow-color,  ↵
      $hoff: $default-text-shadow-h-offset,  ↵
      $voff: $default-text-shadow-v-offset,  ↵
      $blur: $default-text-shadow-blur  ↵
    ) {

      // XXX I'm surprised we don't need 
      // experimental support for this property.
      @if $color == none {
        text-shadow: none; }
      @else {
        text-shadow: $color $hoff $voff $blur; } }

!SLIDE 

### Some other Control Directives available

    @for
    @each
    @while

!SLIDE 

Functions
---------

!SLIDE 

    $base-font-size: 12 !default;
    
    @function pxs2ems(  ↵
      $px: 0,   ↵
      $context: $base-font-size
    ) {
    
      $ems: ($px / $context) * 1em;
      @return $ems;
    }
    
    h1 {
      font-size: pxs2ems(24, 12);
    }

!SLIDE 

* Supports Various Math operations
* Converts Between Units automatically whenever it's possible

