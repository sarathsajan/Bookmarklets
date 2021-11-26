# Bookmarklets

## What are they ?
You all heard of Bookmarks but have you heard of Bookmarklets. No? Well me too. After all these years of using various browsers and extension, finally in 2021 I get to know about bookmarklets. I was trying my hands on making a Chrome extension and that's how I landed on Bookmarklets.


Bookmarklets are kind of like an ancient version of browser extensions. Bookmarklets are browser extensions that is saved as a bookmark. When this bookmark is clicked instead of opening a website url as usual, this time it will execute javascript code. *But how does it execute javascript code?*


## Omnibox - Address Bar on Steroids
You see, browsers have this address bar on top in which the website's url address is displayed. But this address bar can do much more than that. It can support many types of ["UriSchemes"](https://www.iana.org/assignments/uri-schemes/uri-schemes.xhtml).

For eg:
```
file:///

https://

ftp://

bitcoin:

mailto:
```

You can even directly use it as a search box. Because of this omnipotenence, Chrome browser calls this an *Omnibox*. Finding name of omnibox in different browser's has been left as an exercise for the reader. Anyways, it so happens that we can execute javascript code inside this omnibar using the UriScheme `javascript:`

## Building a Bookmarklet
Now all we have to do is write an anonymous funtion in javascript using the following syntax :


`javascript:(function(){ writeYOURcodeHERE })();`


Make sure the code is in a single line because if you think about it, the address bar is a text box with one line. An example code to get a basic DarkMode in any website would be like this - 


`javascript:(function(){document.body.style.background='black'; document.body.style.color='magenta'; alert("Dark Mode Enabled")})();`


Now to make this script work as a 'bookmarklet',


1. First enable the bookmarks tab in your browser so that the bookmarks tab is always present in all tabs.


2. `Right-click` on bookmarks tab and select `Add page...`


3. In the `Name` field give a name for your bookmarklet. In the URL field(in some browsers it might be written Path) enter or paste your one-line javascript code. *Make sure that the syntax is correct*. As an example try this code `javascript:(function(){document.body.style.background='black'; document.body.style.color='magenta'; alert("Dark Mode Enabled")})();`. This code will be like a basic Dark Mode.


4. Click the `Save` button.


5. Now go to *google.com* and once the webpage is fully loaded click on the bookmarklet that we just created. Voila...there you have it, world's shittiest dark mode.


*Another weird bookmarklet*


`javascript:(function(){document.body.style.color='white';alert("Invisible Mode Enabled")})();`
