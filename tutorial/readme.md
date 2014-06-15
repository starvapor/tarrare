#`<Notes from the weekend>`
This doesn't really have any extra info that the following websites haven't already said:

* https://help.ubuntu.com/community/AndroidSDK Android Developer Tools and SDK setup
* http://www.kilobolt.com/game-development-tutorial.html Full Android tutorial
* http://www.kilobolt.com/introduction.html Flappy Birds tutorial

##Install for the Kids
1. `sudo apt-get install openjdk-7-jre openjdk-7-jdk icedtea-7-plugin` install OpenJDK implementation of Java[^1].
2. `mkdir ~/development && cd $_` makes a development folder, and changes into it.
3. download the [ADT-Bundle](https://developer.android.com/sdk/index.html) into this development folder.
4. Type `unzip`+(space)+`adt`+(tab) to auto-complete. It should look like `unzip adt-bundle-linux-x86_64-20140321.zip -d ~/development/adt-bundle-linux`. I renamed mine to just `adt-bundle-linux`.

[^1]: JDK 7 is backwards compatible with 6

##SDK Platform Tools
1. `cd sdk/tools`
2. `./android`
3. select at minimum
  * Android SDK Tools
  * Android SDK Platform-tools
  * an Android SDK Build-tools (19.0.3 in my case) is probably already installed.
  * For demoing things, just need Android 4.4.2 or your choice
    * SDK Platform
    * Optionally samples to show people, or for your own use
    * You only need a System Image for your choice that you're going to test. that said, if you want to test on your own phone, you don't need this.
    * Android Support Library, gives you things like Fragments

![percents](android_percents.png 'Android platform percentages')

At the time of writing, if we just include 4.1.x Jelly Bean and higher, we can cover 72% of the userbase [^2]. We can assign the kids to ask their parents what version they use and just download any older platform versions on a case-by-case basis. On the other hand, in the 2d game development class, everyone was excited to share their games via usb to the other kids. Maybe alternatively use the lowest level of platform the kids mention instead of the case-by-case basis, so they can share. :)

[^2]: https://developer.android.com/about/dashboards/index.html?utm_source=ausdroid.net

##Modify PATH Env Var
Just go to https://help.ubuntu.com/community/AndroidSDK already.

It is so you can type `./android` or `./adb` (etc) in any working directory.

##OPEN SESAME
* `cd adt-bundle-linux/eclipse`
* `./eclipse`

Still just following [tutorial](http://www.kilobolt.com/day-3-creating-our-first-android-application.html)..

![new](new_application_0.png 'Creates a New Android Application')

Set what Android versions you want to support. Don't make it a library.

![configure](new_application_1.png 'Configure Project')

The default workspace is fine.

![configure path](new_application_1.5.png 'Configure Project Path')

I'm doing this tutorial, so I'm choosing a subfolder of the project for the game.

![icons](conf_icon.png 'Configure icon set')
Choose an icon!

![create activity](activity_0.png 'Choose Activity')

Just choose blank activity. Activities are akin to pages, or what is going on and visible. If the kids already have menu items chosen or something, tell them to have at it, but for consistency it might be easier to just tell them to click Next.

![blank activity](activity_1.png 'Blank Activity')

and leave default names so everyone is using the same jargon. Click Finish.

##Etc
The rest is up to your own preference. Make a virtual device, and allocate more RAM than it has as default. Use `Use Host GPU` or `Snapshot` to speed things up when setting it up. Since I was just following the tutorial, I won't repeat anything further. Setup for my example app [Tarrare](https://github.com/starvapor/tarrare) is in the readme of the main repo. All the source and instructions are going to be put on [github.com/starvapor/tarrare](https://github.com/starvapor/tarrare) if you want to see. We'll also upload just the `.apk` so you can test on your phone if you want. :)

#`</notes>`

#Off Topic
If anyone is interested in trying out [Android Studio](https://developer.android.com/sdk/installing/studio.html) at the end of the workshop, it looks promising. It might be easier for the kids. Also, for 2d game people out there, there's [LÖVE Lua](https://love2d.org/), I dunno if that'd fit into your curriculum. My favorite game example is [Mari0](http://stabyourself.net/mari0/) which is a cross between Portal and Mario that has a level maker. It is open [source](http://stabyourself.net/dl.php?file=mari0-1006/mari0-source.zip), check it out.

Everything in this repository is open source ([see license](https://github.com/starvapor/tarrare#license)), feel free to remix and share. This is just me organizing my own thoughts, and doesn't indicate how things should be done, or association with any group. That said, I'd love to have a group of people who help kids code to work on lessons and strategies with! Please comment below on *anything*. This is all a work in progress and I would love to hear input. Hopefully this helps some kids and teachers out.
