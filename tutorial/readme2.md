#LibGDX with Android
This is a reset in my tutorial.

##Intro
So, I'm making a game for my app. I kinda got really excited and didn't think about the other classes; that there was already a 2d and 3d game class.. Should my class be a game class again, but for mobile? Nope. Or at least not a resounding 'yes'. However, I definitely still want to log the steps in making my first mobile app.

I chose to use [libGDX](https://github.com/libgdx/libgdx). I searched around, looking at Unity, Corona, etc etc (etc) (so many!!), and the reason I chose libGDX was really only because it looked the best for me using Java, and fit what I wanted; open source, and what was best for the kids; I think they'll get a kick out of it, if they find that they can put their games on anything, if they're interested that is.  That said, I'd really rather have written something in [Löve Lua](https://love2d.org), [Processing](http://processing.org) or [Python](https://www.python.org).

##Setup
Setting stuff up for me, download the `gdx-setup.jar` from the [Project Setup Gradle](https://github.com/libgdx/libgdx/wiki/Project-Setup-Gradle) wiki page. Then `java -jar gdx-setup.jar`.

![libgdx](libgdx_setup.png 'libGDX setup')

I scratched my steps in the initial setup of ADT, and used the above settings. I decided to use the [box2d](https://github.com/libgdx/libgdx/wiki/Box2d) extension as well.

![eclipse project files](libgdx_advanced.png 'Generates Eclipse project files')

Since, I *am* still using ADT, I also checked off Eclipse in the advanced settings to generate Eclipse project files.

After pressing Generate, it took a few minutes, and then I got a happy BUILD SUCCESSFUL. :)

~~Then open Eclipse and `File > Import > General > Existing Project into Workspace`. Then select your directory, in my case `/home/tom/projects/tarrare`. Then, press Finish.~~

That was pretty cool, but you're not done yet.

###Setting up Eclipse
See [setting up Eclipse](https://github.com/libgdx/libgdx/wiki/Setting-up-your-Development-Environment-%28Eclipse%2C-Intellij-IDEA%2C-NetBeans%29#setting-up-eclipse).

If you were following the previous tutorial, you already have JDK-7, Eclipse, the Android SDK (via ADT bundle), *and* if you have the ADT Bundle, then you already have the [ADT Plugin for Eclipse](https://developer.android.com/tools/sdk/eclipse-adt.html). If you weren't following the tutorial, or don't have the ADT Bundle, then get that plugin! Everyone[^1] though needs the [Eclipse Integration Gradle plugin](https://github.com/spring-projects/eclipse-integration-gradle/). You'll install this via an [update site](https://github.com/spring-projects/eclipse-integration-gradle/#installing-gradle-tooling-from-update-site). AWESOME!

[^1]: Be sure to see that [Setting up Eclipse](https://github.com/libgdx/libgdx/wiki/Setting-up-your-Development-Environment-%28Eclipse%2C-Intellij-IDEA%2C-NetBeans%29#setting-up-eclipse) link if you're targeting iOS. There's some extra setup.

###Importing Your Project
See [Gradle and Eclipse - Importing Your Project](https://github.com/libgdx/libgdx/wiki/Gradle-and-Eclipse).

![gradle import](gradle_import.png 'Import Gradle project')

`File > Import > Gradle > Gradle Project`, then `Build Model`, then `Finish`.

##Running and Debugging
Get excited.

See [Running Your Project](https://github.com/libgdx/libgdx/wiki/Gradle-and-Eclipse#running-your-project) and [Debugging](https://github.com/libgdx/libgdx/wiki/Gradle-and-Eclipse#debugging-your-project).

![libgdx is alive](libgdx_is_alive.png 'Running as Android application')

My blank app running as an Android application. See links above for simple instructions.

###HTML5
Even if the kids don't want games as apps, running the application in browser is *much* less straining on the computer. I could see this as a benefit to using libGDX across the board.

![html superdev setup](libgdx_html_superdev_0.png 'Setup to run as HTML5')

See [Running Your Project](https://github.com/libgdx/libgdx/wiki/Gradle-and-Eclipse#running-your-project) for setup. It'll take a moment, maybe more, I'm just crossing my fingers that it doesn't do that every time, but after it is generated, there's no lag. So, do as the output instructs to get your bookmarklets and be happy. That is, direct yourself to `http://localhost:9876`. Then direct yourself to `http://localhost:8080/html`.

![html superdev running](libgdx_html_superdev_1.png 'Running as HTML5')

Hooray!
