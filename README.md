# handlebars

To install handlebars through node way:-

```
npm install --save handlebars
```

to generate handlebars precompiled templates :-
handlebars <input file name> -f <output file name>
    
Handlebars.js is a popular templating engine that is powerful, simple to use and has a large community. It is based on the Mustache template language, but improves it in several important ways. With Handlebars, you can separate the generation of HTML from the rest of your JavaScript and write cleaner code


### 1. Templates
Handlebars templates look like regular HTML, with embedded handlebars expressions.

```
&#x3C;div class=&#x22;entry&#x22;&#x3E; <br/>
  &#x3C;h1&#x3E;{{title}}&#x3C;/h1&#x3E;<br/>
  &#x3C;div class=&#x22;body&#x22;&#x3E; <br/>
    {{body}} <br/>
  &#x3C;/div&#x3E; <br/>
&#x3C;/div&#x3E; <br/>
```

A handlebars expression is a {{, some contents, followed by a }}

You can deliver a template to the browser by including it in a <script> tag.

```
&#x3C;script id=&#x22;entry-template&#x22; type=&#x22;text/x-handlebars-template&#x22;&#x3E; <br/>
  &#x3C;div class=&#x22;entry&#x22;&#x3E; <br/>
    &#x3C;h1&#x3E;{{title}}&#x3C;/h1&#x3E; <br/>
    &#x3C;div class=&#x22;body&#x22;&#x3E; <br/>
      {{body}} <br/>
    &#x3C;/div&#x3E; <br/>
  &#x3C;/div&#x3E; <br/>
&#x3C;/script&#x3E; <br/>
```

Compile a template in JavaScript by using Handlebars.compile
```
    var source   = document.getElementById("entry-template").innerHTML;
    var template = Handlebars.compile(source);
```
### 2. Precompilation
Using the Handlebars precompiler, you can precompile your Handlebars templates to save time on the client and reduce the required runtime size of the handlebars library.
By doing so you don't need to do Handelbars.compile(template), and it will save time on client side.

```
&#x3C;script type=&#x22;text/javascript&#x22; src=&#x22;precomp.js&#x22;&#x3E;&#x3C;/script&#x3E; <br/>
```

```
var renderer = Handlebars.templates["precomp"];
```

Here precomp is the file name which we will get after compilation.
