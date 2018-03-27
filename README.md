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
<div class="entry"> 
  <h1>{{title}}</h1>
  <div class="body"> 
    {{body}} 
  </div> 
</div> 
```

A handlebars expression is a {{, some contents, followed by a }}

You can deliver a template to the browser by including it in a <script> tag.

```
<script id="entry-template" type="text/x-handlebars-template"> 
  <div class="entry"> 
    <h1>{{title}}</h1> 
    <div class="body"> 
      {{body}} 
    </div> 
  </div> 
</script> 
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
<script type="text/javascript" src="precomp.js"></script>
```

```
var renderer = Handlebars.templates["precomp"];
```

Here precomp is the file name which we will get after compilation.
