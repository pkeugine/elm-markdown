# CommonMark - ATX headings

## [Example 43](https://spec.commonmark.org/0.29/#example-43)

This markdown:

````````````markdown
### foo ###     

````````````

Should give output:

````````````html
<h3>foo</h3>
````````````

But instead was:

````````````html
<h3>foo ###</h3>
````````````
## [Example 45](https://spec.commonmark.org/0.29/#example-45)

This markdown:

````````````markdown
# foo#

````````````

Should give output:

````````````html
<h1>foo#</h1>
````````````

But instead was:

````````````html
<h1>foo</h1>
````````````
## [Example 46](https://spec.commonmark.org/0.29/#example-46)

This markdown:

````````````markdown
### foo \###
## foo #\##
# foo \#

````````````

Should give output:

````````````html
<h3>foo ###</h3><h2>foo ###</h2><h1>foo #</h1>
````````````

But instead was:

````````````html
<h3>foo \</h3><h2>foo #\</h2><h1>foo \</h1>
````````````
## [Example 49](https://spec.commonmark.org/0.29/#example-49)

This markdown:

````````````markdown
## 
#
### ###

````````````

Should give output:

````````````html
<h2></h2><h1></h1><h3></h3>
````````````

But instead was:

````````````html
<h2></h2><h3></h3>
````````````
