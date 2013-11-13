# Howdy, developers.

Picture this awesome and regularly occurring scenario: 

We make a little JS/CSS widget for a site, then install it
everywhere else coz we think it's neat (for instance onMediaQuery, or ShowHide.js).

A month later, we find a bug! Holy toledo Batman, **it's broken in IE8!**

We fix the bug, for the job we're working on right now, and then manually copy the code out to all our other projects.

Or some of our other projects. When we get round to it.

Or none of them, because more important things come up.

We really need a package manager for front-end assets. We started this with using svn:externals,
but anyone who's pulled and `svn up` with this pattern knows what a pain in the ass it is.

## Enter Bower

Available at http://bower.io/

Bower lets you install front-end dependencies via a git endpoint. So you can do this: 

`bower init` (in your project root) 

And then: 
 
```
bower install teflon.js
bower install quicktube.js
```

And you'll magically have the latest stable versions from github in your project. **BAM!**

## What about updating?

I'm glad you asked, o wise dao of development. It's really easy:

```
bower update on-media-query 
```

You can find out what versions are available by typing: 

```
bower info on-media-query
```

It'll also magically install dependencies of dependencies, so if
`teflon.js` needs a newer version of `on-media-query`, it will update those too.



The bower site has heaps more documentation. Just jump in, it's easy.
