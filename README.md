CSS Design Patterns
===================

This is a living document, detailing our front-End Dev design patterns, abstractions and re-usable objects in vanilla CSS. 

Use patterns to cut-down on how much CSS you need to write and to quicky prototype the stuff those designers give you. 

### Also see ###
Inuit CSS - [https://github.com/csswizardry/inuit.css]
SMACSS - [http://smacss.com/]
This talk by Harry Roberts (43min) - [http://www.youtube.com/watch?v=R-BX4N8egEc]
Markdown syntax: [http://daringfireball.net/projects/markdown/syntax#html]

### Patterns ###

```CSS
/*  
    .nav
    -----------------------------------------------
    Basic horizontal nav list object.
    Breaks nav items to vertical blocks at 25em for mobile

    <ul class='nav'>
        <li>Something</li>
        <li>Something</li>
    </ul>
 
    SaSS: @extend .nav;
*/

.nav { /* ul */
    margin: 0;
    padding-left: 0;
    overflow: hidden;
}

.nav li {
        display: inline-block;
        list-style: none;
}

@media screen and (max-width: 25em) {
    .nav li {
        display: block;
    }
}
```
