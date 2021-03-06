# Original - amps_and_angles_encoding

## Example undefined

This markdown:

````````````markdown
AT&T has an ampersand in their name.

AT&amp;T is another way to write it.

This & that.

4 < 5.

6 > 5.

Here's a [link] [1] with an ampersand in the URL.

Here's a link with an amersand in the link text: [AT&T] [2].

Here's an inline [link](/script?foo=1&bar=2).

Here's an inline [link](</script?foo=1&bar=2>).


[1]: http://example.com/?foo=1&bar=2
[2]: http://att.com/  "AT&T"

````````````

Should give output:

````````````html
<p>AT&amp;T has an ampersand in their name.</p><p>AT&amp;T is another way to write it.</p><p>This &amp; that.</p><p>4 &lt; 5.</p><p>6 &gt; 5.</p><p>Here&#39;s a<a href="http://example.com/?foo=1&amp;bar=2">link</a>with an ampersand in the URL.</p><p>Here&#39;s a link with an amersand in the link text:<a href="http://att.com/" title="AT&amp;T">AT&amp;T</a>.</p><p>Here&#39;s an inline<a href="/script?foo=1&amp;bar=2">link</a>.</p><p>Here&#39;s an inline<a href="/script?foo=1&amp;bar=2">link</a>.</p>
````````````

But instead was:

````````````html
<p>AT&amp;T has an ampersand in their name.</p><p>AT&amp;T is another way to write it.</p><p>This &amp; that.</p><p>4 &lt; 5.</p><p>6 &gt; 5.</p><p>Here&#39;s a [link]<a href="http://example.com/?foo=1&amp;bar=2">1</a>with an ampersand in the URL.</p><p>Here&#39;s a link with an amersand in the link text: [AT&amp;T]<a href="http://att.com/" title="AT&amp;T">2</a>.</p><p>Here&#39;s an inline<a href="/script?foo=1&amp;bar=2">link</a>.</p><p>Here&#39;s an inline<a href="/script?foo=1&amp;bar=2">link</a>.</p>
````````````
