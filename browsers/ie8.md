## IE8 ##

#### Refuses to fire change events on hidden inputs
If your input has `visibility: hidden;`, any bound `change` event-listeners won't fire. 

The solution? Hide your input with `-ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=0)";` instead.
