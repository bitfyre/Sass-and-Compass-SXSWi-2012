!SLIDE 

Two Syntaxes? 
=============

What's that all about?
----------------------

!SLIDE code

    $font-color:        #3B3330
    $sans-family:       Helvetica, FreeSans, »
      "Nimbus Sans L", Arial, sans-serif
    
    $fancy-sans-family: "dejarip-1", »
      "dejarip-2", $sans-family

!SLIDE code

    .nav
      font-family: $sans-family

      ul, ol
        list-style: none
        list-style-image: none

!SLIDE code

    …
      a
        background-color: $nav-bg-color

        &:hover, &:focus
          color: $link-hover-color

          background:
            color: $nav-bg-hover
            image: url("nav-bg.png")
            repeat: no-repeat


