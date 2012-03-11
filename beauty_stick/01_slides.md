!SLIDE 

Hit CSS with the Pretty stick
=============================

!SLIDE 

Output styles
-------------

!SLIDE code smaller

    /* --------------------------------- */
    /* Navigation */
    /* --------------------------------- */

    // Typography
    $font-color: #3b3330;
    $sans-family: Helvetica, FreeSans, "Nimbus Sans L",   ↵
      Arial, sans-serif;

    $fancy-sans-family: "dejarip-1", "dejarip-2",   ↵
      $sans-family;

    // Nav colors
    $link-hover-color: blue;
    $nav-bg-color: $font-color;
    $nav-bg-hover: lighten($nav-bg-color, 20%);

!SLIDE code smaller

    .nav {
      font-family: $sans-family;
      ul, ol {
        list-style: none;
        list-style-image: none; }
      a {
        background-color: $nav-bg-color;
        &:hover, &:focus {
          color: $link-hover-color;
          background: {
            color: $nav-bg-hover;
            image: url("nav-bg.png");
            repeat: no-repeat; }; } } }

!SLIDE 

:nested
-------

!SLIDE code smaller

    /* --------------------------------- */
    /* Navigation */
    /* --------------------------------- */
    .nav {
      font-family: Helvetica, FreeSans, "Nimbus Sans L",    ↵
        Arial, sans-serif; }
      .nav ul, .nav ol {
        list-style: none;
        list-style-image: none; }
      .nav a {
        background-color: #3b3330; }
        .nav a:hover, .nav a:focus {
          color: blue;
          background-color: #73645e;
          background-image: url("nav-bg.png");
          background-repeat: no-repeat; }

!SLIDE 

:expanded
---------

!SLIDE code smaller

    /* --------------------------------- */
    /* Navigation */
    /* --------------------------------- */
    .nav {
      font-family: Helvetica, FreeSans, "Nimbus Sans L",   ↵
        Arial, sans-serif;
    }
    .nav ul, .nav ol {
      list-style: none;
      list-style-image: none;
    }
    .nav a {
      background-color: #3b3330;
    }
    .nav a:hover, .nav a:focus {
      color: blue;
      background-color: #73645e;
      background-image: url("nav-bg.png");
      background-repeat: no-repeat;
    }

!SLIDE 

:compact
--------

!SLIDE code smaller

    /* --------------------------------- */
    /* Navigation */
    /* --------------------------------- */
    .nav { font-family: Helvetica, FreeSans, "Nimbus Sans L",   ↵
       Arial, sans-serif; }
    .nav ul, .nav ol { list-style: none;   ↵
      list-style-image: none; }
    .nav a { background-color: #3b3330; }
    .nav a:hover, .nav a:focus { color: blue;   ↵
      background-color: #73645e; background-image: url("nav-bg.png");   ↵
      background-repeat: no-repeat; }

!SLIDE 

:compressed
-----------

!SLIDE code smaller

    .nav{font-family:Helvetica,FreeSans,"Nimbus Sans L",Arial,sans-serif}.nav ul,.nav ol{list-style:none;list-style-image:none}.nav a{background-color:#3b3330}.nav a:hover,.nav a:focus{color:blue;background-color:#73645e;background-image:url("nav-bg.png");background-repeat:no-repeat}


!SLIDE 

Other Useful Output Configs
---------------------------

    :line_comments => true,
    :debug_info => true

