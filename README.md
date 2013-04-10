CSS Design Patterns
===================

This is a living document, detailing our front-End Dev design patterns, abstractions and re-usable objects in vanilla CSS. 
Use patterns to cut-down on how much CSS you need to write and to quicky prototype the stuff those designers give you. 

### Also see ###
* Inuit CSS - [https://github.com/csswizardry/inuit.css]
* SMACSS - [http://smacss.com/]
* This talk by Harry Roberts (43min) - [http://www.youtube.com/watch?v=R-BX4N8egEc]
* Markdown syntax: [http://daringfireball.net/projects/markdown/syntax#html]

### Patterns ###

```CSS
/*  
    .nav
    -----------------------------------------------
    Basic horizontal nav list object.
    Breaks nav items to vertical blocks at 25em for mobile
    Assumes the element is a list

    <ul class='nav'>
        <li>Something</li>
        <li>Something</li>
    </ul>
 
    SaSS: @extend .nav;
*/

.nav { /* ul, ol */
    margin: 0;
    padding-left: 0;
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




/*
    .media
    -----------------------------------------------
    The classic Media object from Nicole Sullivan:
    http://www.stubbornella.org/content/2010/06/25/the-media-object-saves-hundreds-of-lines-of-code/
    
    <div class='media'>
        <div class='media__image'>
            <img src='image.png' alt='An Image'>
        </div>
        <p class='media__body'>
            The media text.
        </p>
    </div>
    
*/

.media, .media__body { /* div, li */
    overflow: hidden;
    *overflow:visible;
    zoom:1;
}
    .media__image{
        float:left;
        margin-right: 0.5em;
    }
    
    .media__image img{
        display:block;
    }

    .media__body{
         /* The container for your text */
    }


/*
    .split
    -----------------------------------------------
    Splits text into left and right columns, as in a price list,
    ingredients list etc.
    
    <dl class='split'>
        <dt class='split__left'>Widgets</dt>
        <dd>$5.00</dd>
        <dt class='split__left'>Sprokets</dt>
        <dd>$7.00</dd>
    </dl>
*/

.split { /* div, dl, li, p */
    text-align: right;
    overflow: hidden;
}


    .split__left{ /* dt, span */
        text-align: left;
        float: left;
    }

```
