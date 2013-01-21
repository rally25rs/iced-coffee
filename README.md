# iced-coffee.js

Iced Coffee is a "bookmarklet" that is designed to add some basic CoffeeScript support to Telerik's [Icenium Myst](https://app.icenium.com/Mist).

If you want the Icenium team to add *real* CoffeeScript support in a future release please also upvote it in [Icenium Feedback](https://feedback.telerik.com/Project/87/Feedback/Details/774-coffeescript-support).

## The Bookmarklet

Create a bookmark in your browser with this as the location
(sorry, GitHub's markdown prevents me from just making a draggable link on this page):
```
javascript:(function(){var d=document;var s=d.createElement('script');s.src='https://github.com/rally25rs/iced-coffee/raw/master/iced-coffee.js';d.getElementsByTagName('head')[0].appendChild(s);})();
```

## Usage

1. Create a new bookmark in your browser with the code listed above (sorry, GitHub's markdown prevents me from just making a draggable link on this page).
2. Open Icenium Myst to a project.
3. Click the bookmarklet. In the upper right corner of Icenium next to your user name it should now say "+IcedCoffee" to indicate that it is enabled.
4. Create 2 new files in your project, both using the "JavaScript" file template, but name one `.coffee` and the other `.js`. So for example, `hello-world.coffee` and `hello-world.js`.
5. Open your `.coffee` file, write some CoffeeScript, and save the file. The `.js` file with the same name will be auto updated.

## What Works

* When you save a file with a `.coffee` extension, a `.js` file with the same name will be updated with the compiled code.
* If the corresponding `.js` file does not exist an alert box will be shown.
* If you run the bookmarklet twice, it will not re-initialize itself.
* The `.js` file being generated does not need to be open in Icenium. IcedCoffee tells the server to update the contents.
* If the `.js` file being generated is open in Icenium, its contents will be reloaded after the save. This way you can see the changes right away.

## What Doesn't Work

* Does not detect if Icenium is actually open when the bookmarklet is run. This will be simple to add later.
* Does not create a `.js` file for you. You have to create the empty file manually.
* `.coffee` files **are still deployed with your App**, just like they were `.js` content files. I haven't figured out if there is a way to prevent this yet.
* No syntax highlighting. I don't even know where to start with this.
* There is no way to add a "CoffeeScript" file template to the "New File" dialog box. These templates are maintained on the server that can not be modified by the bookmarklet.

[1]: javascript:(function(){window.tmpElem=document.createElement('script');tmpElem.src='https://github.com/rally25rs/iced-coffee/raw/master/iced-coffee.js';document.getElementsByTagName('head')[0].appendChild(tmpElem);})();
