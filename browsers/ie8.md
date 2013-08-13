## IE8 ##

#### Refuses to fire change events on hidden inputs
If your input has `visibility: hidden;`, any bound `change` event-listeners won't fire. 

The solution? Hide your input with `-ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=0)";` instead.

#### Don't use pseudo elements on the body tag
IE8 doesn't play nicely with pseudo elements `:before` and `:after` on the `<body>` element. In some version of IE8 it can cause it to switch to Compatibility Mode which uses the IE7 rendering engine \*sadface\*.
