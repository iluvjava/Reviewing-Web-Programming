# The DOM Model #

HTML is not just a page with a lot of tags, but all the tags represent a structure, and it's always a tree structure that is made of tree. So it's a data structure that is made of HTML tags. It sounds stupid because it is, but it's also kinda cool if you think about it carefully. 

Read (THIS)[https://www.w3schools.com/js/js_htmldom.asp] from W3School where it goes on and explain on this idea. 

**You have to read this** to understand how the CSS selector select things on the webpage. CSS select elements base on their hierarchy on the tree. (JavaScript too)


# CSS Selectors #

Now we will refers to **tags** in the HTML page as elements of the HTML page. Remember that tag is constructed with <> and if it's not a self closing tag, it will be accompanied by the closing tag: 
</>. 

CSS selectors selects a lot of tags and it has its syntax. Here is a list of guide from W3School: 

* [link](https://www.w3schools.com/cssref/css_selectors.asp) JUST READ IT!


## HTML Special Attributes ##
There are some attributes that are kinda special and related to the CSS selectors. They are created to make selecting elements on the page via CSS more friendly. 

### Class Attribute ###
* There is a special attribute for HTML tags that allows CSS selectors to recognize them. It's the class Attribute. 
```
<p class="red">This is a paragraph.</p>
```

In this case I have name the HTML attribute myself, it doesn't change anything on how the tag is displayed, but this meta information about this tag has been added, and it's visible to a CSS selector for a rule set. You can also choose to add multiple classes, and it will look like this: 
```
<p class="red big shadow">This is a paragraph.</p>
```
In this case, the same tag will have multiple classes belongs to it. 

### ID attribute ###

* Similar to class attribute, the ID attribute is also very friendly to the CSS selector. This is how it looks like: 
```
<p id="unique"> </p>
```
* This attribute is supposed to be uniqe on the page, meaning that the same id should not appear 2 times on the page. 

* When selecing the element by the ID value, the CSS will always choose the first element possessing that ID, if there are multiple of them, the one that comes after it will not be regnized (Unles the one that comes before it is removed.) 


### The Div Tag ###
* This tag is literally for grouping Tags in the DOM, which doesn't change the look of elements on the web page at all. 

## Common CSS Selectors ##
Here is a list of operators that I want to highlight: 

* .class 
    * Using the "." operator right in front of the class you want to select will select the class. 
    * Example: p.myintro: This will select all `<p>` tags that has class attribute value "myintro"

* #id: 
    * This will selecting the **first** element on the page with the id of "id"

* " ": 
    * THIS ONE IS IMPORTANT, as you are observing the CSS by yourself on random website, I hope you notice that spaces has some kind of meaning, however, it's very easy to overlook this one. 
    * Space, as " " in css selector meaning seleting from all its children (All the tages that are in side that tag).
    * For example `p a` will select all the `<a>` tag that is insdie of `<p>` tag. And by inside, I mean SEVERAL level of nesting is still counting as inside of the tag. 

* ","
    * The OR operator, `p, div` will select all `<p>` tags and all `<a>` tags. 

* ">"
    * The "Direct Decendent Of" operator, if `p > a` will choose all the  `<a>` tags that are strictly within 1 level contained inside of the `<p>` tag. 

### Weird CSS Selector ###

* '[]', ':'
    * In general, the '[]' contains a logical statement about the meta information on HTML tags. `[href$= ".pdf"]` means all tags with href attribute such that its attribute value ends with ".pdf". This is not particular useful when styling website, but it's very useful for web-scraping. 
    * ':' is the Pseudo Class Selector. 'a:active' selects an `<a>` tag that is currently in the state of active, and an anchor tag is "active" when the mouse hovers over it. 


# Properties of CSS Rules Set #