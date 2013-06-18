# Zurb Foundation 4, Responsive "Fork me on Github" Ribbon

by James Stone. Forked from the excellent css-fork-on-github-ribbon by Christian Heilmann.

* Lightweight (37 lines of Scss)
* Foundation 4, Resposive for Mobile
* Sass/Scss
* Go crazy, BSD License

1. Add the following HTML

``` html
<div class="row">
    <div class="small-12 columns" id="forkongithub"><a class="button expand" href="https://github.com/manofstone/foundation4-fork-on-github-ribbon">Fork me on GitHub</a></div>
</div>
```

2. Add the following to your sass/app.scss
``` scss
// A modification and refactoring of the excellent 
// responsive css-fork-on-github-ribbon by Christian Heilmann
// specificly for use with Zurb Foundation 4 and Sass/Scss

// https://github.com/manofstone

// Software License Agreement (BSD License)
// Copyright (c) 2013, Christian Heilmann.
// All rights reserved.

// https://github.com/codepo8/css-fork-on-github-ribbon

$forkingithub-width: 300px;
$forkingithub-offset: 60px;

@media #{$small} {

  #forkongithub {
    position:absolute;
    display:block;
    top:0;
    right:0;
    width: emCalc($forkingithub-width);
    overflow:hidden;
    height:emCalc($forkingithub-width);
    z-index:1000;
  }

  #forkongithub a {
    width:emCalc($forkingithub-width);
    position:absolute;
    top:emCalc($forkingithub-offset);
    right:emCalc(-$forkingithub-offset);
    transform:rotate(45deg);
    -webkit-transform:rotate(45deg);
    box-shadow:4px 4px 10px rgba(0,0,0,0.8);
  }

  #forkongithub a::before, #forkongithub a::after { 
    content:"";
    width:100%;
    display:block;
    position:absolute;
    top:1px;
    left:0;
    height:1px;
    background:#fff;
  }

  #forkongithub a::after {
    bottom:1px;
    top:auto;
  }
}
```

3. Compile with Compass, enjoy.

