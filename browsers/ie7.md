## IE7 ##
Has lots of awesome bugs. 

### Sibling selector #
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

### CSS inherit #
IE7 doesn't support `property:inherit`, meaning it only has a semi-cascading implementation of CSS. Go figure :) 

```CSS

.pig{
	border-color: pink;
}

.thing{
	border-color: inherit;
}

```
```HTML
<div class='pig'>
	<!-- .thing won't get a pink border in IE7 -->
	<div class='thing'></div>
</div>

```

