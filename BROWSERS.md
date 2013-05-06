Weird things that browsers do
===================

Title says it all.

## Internet Explorer ##
Has lots of awesome bugs. 

### IE7 ###

#### Sibling selector #
Sibling selector fails to match if an HTML comment sits between the adjoining elements.

```CSS

ul + p {
	margin-top: 3em;
}

```

This will fail in IE7:

```HTML
<ul>
	<li>Bacon</li>
	<li>Ham</li>
	<li>Prosciutto</li>
	<li>Pork*</li>
</ul>
<!-- oink -->
<p>*Leading cause of heart disease</p>
```

But this is fine:

```HTML
<ul>
	<li>Bacon</li>
	<li>Ham</li>
	<li>Prosciutto</li>
	<li>Pork*</li>
</ul>

<p>*Leading cause of heart disease</p>
```