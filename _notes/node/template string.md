---
tags: node
---
Template literals are string literals allowing embedded expressions. You can use multi-line strings and string interpolation features with them. They were called "template strings" in prior editions of the ES2015 specification.

Template literals are enclosed by the back-tick (\` \`)  (grave accent) character instead of double or single quotes. Template literals can contain placeholders. These are indicated by the dollar sign and curly braces (`${expression}`). The expressions in the placeholders and the text between them get passed to a function. The default function just concatenates the parts into a single string. If there is an expression preceding the template literal (`tag` here), this is called a "tagged template". In that case, the tag expression (usually a function) gets called with the template literal, which you can then manipulate before outputting. To escape a back-tick in a template literal, put a backslash \ before the back-tick.
> `string text ${expression} string text`