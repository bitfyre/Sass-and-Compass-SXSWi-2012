!SLIDE 

The Basics
==========

!SLIDE

Variables
---------

    $font-color:        #3B3330;

    $sans-family:       Helvetica, FreeSans, 
      "Nimbus Sans L", Arial, sans-serif;

    $fancy-sans-family: "dejarip-1",
      "dejarip-2", $sans-family;
    
    h1 {
      font-family: $fancy-sans-family;
      color: $font-color;
    }

!SLIDE

Setting a Default Variable Value
--------------------------------

    $font-size: 12 !default;

!SLIDE

Nesting selectors
-----------------

    .nav {
      font-family: $sans-family;
      ul, ol {
        list-style: none;
        list-style-image: none;
      }
    }

!SLIDE

Parent References
-----------------

    .nav {
      …
      a {
        &:hover, &:focus {
          color: $link-hover-color;
        }
      }
    }

!SLIDE

Nesting statements
------------------

    background: {
      color: $nav-bg-hover;
      image: url("nav-bg.png");
      repeat: no-repeat;
    }

!SLIDE

Comments
--------

    /*  Standard CSS style Comment
        It will show up in the CSS */

    // Sass comment.
    // This will not show up in the CSS.

