# karl.tech Ghost Theme
You can see this theme in action on [karl.tech](https://karl.tech/)

## What you can use this repo for
Possibly nothing. The issue is, I had to make some pretty serious changes to the theme this theme is based off of. 
I wanted to get it all done quickly, and so I ended up hardcoding a lot of stuff.

#### Technical Debt Meter: 60%

That being said, you can use this repo if you:

1. Want to throw up an exact replica of karl.tech, and you're OK with spending a few hours fixing broken stuff (like fonts... get your own Adobe Typekit!)
2. You are editing the existing karl.tech site
3. You are evaulating Karl's coding abilities by checking out this repo. If this is the case though, you're not going to be very impressed. karl.tech was hacked together quite haphazardly.

## How to build/edit
This is a record of how I would build this site. I couldn't get a good workflow going, so this is what I ended up with:

1. Host the site for dev using the [Ghost Docker image](https://hub.docker.com/_/ghost/)
2. Install build tools using Karl's [rundock node -w](https://github.com/karlfloersch/.bin/blob/master/rundock). That way you don't pollute your global namespace.
3. Check to see if Ghost is working correctly by going to [http://localhost:8080](http://localhost:8080)
4. To make changes to the templates, just edit the *root level* *.hbs files. That needs no compilation.
5. To make changes to the css, edit the /src/*.scss files. Those need compilation, so run `grunt` after to compile it.
6. **The compiled css will output to `/build/assets/css/*`** so you need to now *manually copy* the minified css to `assets/css/*`. **NOTE:** I realize I could have edited the grunt file to include this copy, but ain't nobody got time for that.
7. Check out your sweet changes and start blogging!

## Credits
Forked from [Ghostium](https://github.com/oswaldoacauan/ghostium/).

## License

[MIT License](http://oswaldoacauan.mit-license.org/) © Karl Floersch
