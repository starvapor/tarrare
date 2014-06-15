So, I'm making a game for my app. I kinda got really excited and didn't think about the other classes; that there was already a 2d and 3d game class.. Should my class be a game class again, but for mobile? Nope. Or at least not a resounding 'yes'. However, I definitely still want to log the steps in making my first mobile app.

I chose to use [libGDX](https://github.com/libgdx/libgdx). I searched around, looking at Unity, Corona, etc etc (etc) (so many!!), and the reason I chose libGDX was really only because it looked the best for me using Java, and fit what I wanted; open source, and what was best for the kids; I think they'll get a kick out of it, if they find that they can put their games on anything, if they're interested that is.  That said, I'd really rather have written something in [Löve Lua](https://love2d.org), [Processing](http://processing.org) or [Python](https://www.python.org).

Setting stuff up for me, download the `gdx-setup.jar` from the [Project Setup Gradle](https://github.com/libgdx/libgdx/wiki/Project-Setup-Gradle) wiki page. Then `java -jar gdx-setup.jar`.

![libgdx](libgdx_setup.png 'libGDX setup')

I scratched my steps in the initial setup of ADT, and used the above settings. I decided to use the [box2d](https://github.com/libgdx/libgdx/wiki/Box2d) extension as well.

![eclipse project files](libgdx_advanced.png 'Generates Eclipse project files')

Since, I *am* still using ADT, I also checked off Eclipse in the advanced settings to generate Eclipse project files.

After pressing Generate, it took a few minutes, and then I got a happy BUILD SUCCESSFUL. :)

I then opened Eclipse and File > Import > General > Existing Project into Workspace. Then select your directory, in my case `/home/tom/projects/tarrare`. Then, press Finish.
