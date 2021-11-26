# Bookmarklets

You all heard of Bookmarks but have you heard of Bookmarklets. No? Well me too. After all these years of using various browsers and extension, finally in 2021 I get to know about bookmarklets.


Bookmarklets are kind of like an ancient version of browser extensions. Bookmarklets are browser extensions that is saved as a bookmark. When this bookmark is clicked instead of opening a website url as usual, this time it will execute javascript code. *But how does it execute javascript code?*


### Omnibox - Address Bar on Steroids
You see, browsers have this address bar on top in which the website's url address is displayed. But this address bar can do much more than that. It can support many types of ("UriSchemes")[https://www.iana.org/assignments/uri-schemes/uri-schemes.xhtml] or simply text commands.


For eg: `file:///`, `https://`, `ftp://`, `bitcoin:`, `mailto:` etc etc etc.


You can even directly use it as a search box. Because of this omnipotenence, Chrome browser calls this an *Omnibox*. Finding name of omnibox in different browser's has been left as an exercise for the reader. Anyways, it so happens that we can execute javascript code inside this omnibar using the UriScheme `javascript:`


Now all we have to do is write an anonymous funtion in javascript using the following syntax :


`javascript:(function(){ writeYOURcodeHERE })();`


Make sure the code is in a single line because if you think about it, the address bar is a text box with one line. An example code to get a basic Dark Mode in any website would be like this - 


`javascript:(function(){document.body.style.background='black'; document.body.style.color='magenta'; alert("Dark Mode Enabled")})();`
