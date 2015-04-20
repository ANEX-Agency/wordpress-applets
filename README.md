# WordPress Applets
WordPress Applets is an attempt to combine shortcodes, widgets and template tags within WordPress

### What is an applet?
An Applet is basically a piece of code which can be inserted anywhere within WordPress. It works basically like a shortcode, a widget or a template tag

### Why the combination of them?
As a wordpress developer there is always the decision what functionality will be put as shortcode, what will be put as widget and what will be put only as template tag. In the most scenarios the code output itself doesn't change much, but with the current system it is somehow harder to maintain the code base.

Let's take as example a function which should display a language switcher. That language switcher will basically consist of a list of options (languages) which can be choosen from. It may display the language name and or the flag.

Seasoned developers know that they can wrap that functionality within a single function, and use this function within a shortcode and within a widget. If for some reason something changes, the developer only have to fix this issue within the function - leaving the code from the shortcode and from the widget untouched, still they have (probably) 3 files where to maintain code for the same functionality (eg. adding a new option or another parameter).

More complex stuff like a slider also mostly involves the usage of Javascript. There are ways available to only load JS (and/or CSS) only if a certain function, shortcode or widget gets used, but still - not everyone is aware of such techniques.

Last but not least there is always the work for the options itself of a particular function. Many developers put plenty of parameters into their shortcodes, making it hard for everyone to remember the correct syntax, and widget settings just look bloated when having more than 10 options available.

### How to solve that?
That's where applets come in handy. An applet combines all of that, leaving only the frontend output in the hands of the developer. The whole logic is done behind the curtain.

So basically it only needs to have a definition file which consists of a multi-dimensional array where to setup the parameters of an applet. The applet itself will be created dynamically from the WordPress Applets Plugin.

### Ready?
Not yet. Still working on a pre-alpha. Suggestions are welcome.
