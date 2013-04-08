CSS Design Patterns
===================

Handy, time-saving Front-End Dev design patterns, abstractions and objects.

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
