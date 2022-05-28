# Reduced Test case for 11ty Render

I didn't even get to my real test case (though I put a case in for it)

Currently this repo has the Render plugin, but it is not rendering markdown. I pulled a static example from the docs (modified the h1 for that one) 

```
    {% renderTemplate "md" %}
    # I expect this to output an h1 and 2 list items
    
    * I am a list
    * I am a list
    {% endrenderTemplate %}
```

And i have a case of using the plugin with a shortcode that is supposed to insert Markdown to be rendered. Currently just a static return from the shortcode

```js 
  eleventyConfig.addShortcode("outputMD", function() {
   
    return `# Hello World`;
  })
```

```html
    {% renderTemplate "md" %}
    > I expect this to output the markdown from the shortcode
        {% outputMD %}
    {% endrenderTemplate %}
```

## Output

Here's the output

![Test case showing the markdown being output as a string](https://github.com/brob/eleventy-reducedtest-render/blob/main/test-case.png?raw=true)