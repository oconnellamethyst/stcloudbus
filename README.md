# St. Cloud GTFS Project
A volunteer project led by @oconnellamethyst to create a GTFS feed for the city of St. Cloud, MN. All are welcome to join. Learn more about what [GTFS feeds are](https://developers.google.com/transit/)

A GTFS feed is a way for a transit system's data to communicate with apps, like Google Maps. We are creating a Static GTFS system for the busses in the city of St. Cloud that are not covered by the GTFS system for the Metro Transit System, specifically the busses covered by the Metro Bus system. This will allow the people in St. Cloud to use apps that use GTFS feeds, such as Google Maps, to be able to navigate their city. This will be especially helpful for incoming St. Cloud State University students, such as @oconnellamethyst who will be transferring there in the Fall from the cities (unless the U of M stops ghosting them).

### What is NorthScript?
NorthScript is a group of developers and aspiring developers that meets in Minneapolis. It is a group that uses freecodecamp.org and other resources to build on our development abilities. You can find us on our [Facebook Page](https://www.facebook.com/groups/free.code.camp.minneapolis/about/) and our [Gitter](https://gitter.im/Northscript/Lobby)

### How do I work with this repository?
As an aspiring developer, you may not be familiar with GitHub and Git, or doing things with stuff. That's okay, here's a crash course in it! If you ever need any help with any of this, drop me a line in the Gitter chat or in the Facebook Group

First, you'll need a computer. You may be thinking, "Yes, @oconnellamethyst, of course I need a computer to code, but I'm on a computer right now!" But when I say that, I mean, you need a computer that you are actually comfortable developing code in. When I first started at Northscript, I started with a Windows 7 laptop that was a pain to get anything of value to run on and had the battery life of a early 2000s cheap cell phone, it wrecked my ability to understand anything of substance in computer programming. Then that computer died and I bought a new-used [XUbuntu](https://xubuntu.org/tour/) Laptop from [Free Geek Twin Cities](http://freegeektwincities.org/) for $170, promptly installed [Ubuntu (the Long-Term Stable Release)](https://www.ubuntu.com/download/desktop) over XUbuntu just because I was getting super weird glitches when trying to install Google Chrome, and promptly realized that I had just accidentally improved my coding abilities by 200% just by getting a laptop that I didn't have to fight to code anything on. In coding, such as in life, you need tools that will work with you, not against you. I highly recommend the laptops sold by [Free Geek Twin Cities](http://freegeektwincities.org/), as not only are they recycling laptops and keeping them from going to waste, but also, they're just really good, but honestly, just get something that you aren't fighting. Coding is a battle all it's own without having to fight your computer.

Second, you need to get Git on your computer. [Installation instructions here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). Notice how easy it is to install Git if you followed my advice and got a laptop from Free Geek Twin Cities, and installed Ubuntu over XUbuntu, you just open up the Terminal and type a few lines!

Now you've got to do Github things. If you haven't created a Github account, go do that now, and make sure to verify your email. See that button in the top right corner that says Fork? Press it. Now you are making your own copy of this Repository so that you don't accidentally eat it or something IDK. Now you want a copy of your copy of this repository on your computer so that you can edit code things. Open up your terminal in Ubuntu, or the BASH Terminal emulator that comes with Git on Windows, or whatever magic you Mac folks do, and basically get a Git copy of your fork, which is a copy of this repository. On my Ubuntu, this looks something like this.

'''
computerusername@Computername:~$ mkdir folderthatIwantcodestuffsin
computerusername@Computername:~$ cd folderthatIwantcodestuffsin/
computerusername@Computername:~/folderthatIwantcodestuffsin$ git clone https://github.com/githubuser/stcloudbus.git
Cloning into 'stcloudbus'...
remote: Counting objects: 34, done.
remote: Compressing objects: 100% (33/33), done.
remote: Total 34 (delta 1), reused 30 (delta 0), pack-reused 0
Unpacking objects: 100% (34/34), done.
'''

I made a folder that I wanted my codestuffs in using '''mkdir''' which is short for make directory, it makes you a nice folder. I then went inside of that folder using '''cd''' which is short for change directory, it lets you go inside of that folder you just created. What if I forget what the folder is called? You might ask? That's where you use the '''ls''' command. It's short for list, and it lists all the files and directories that are in whereever you are, it's super useful, and looks something like this. Also, note, if you try to use a keyboard shortcut to copy and paste in the terminal, it wont work. You have to either do Shift+Ctrl+C or just right-click.

'''
computerusername@Computername:~/folderthatIwantcodestuffsin$ ls
stcloudbus
'''

See, when I git cloned my fork onto my computer in folderthatIwantcodestuffsin, it created a folder called stcloudbus, a special folder that works with git. I want in that folder, but I'm a lazy typer, so because there is only one folder, I can type '''cd s''' and then press the tab key, and since stcloudbus is the only folder that starts with an s, it will autocomplete. Nifty right?

'''
computerusername@Computername:~/folderthatIwantcodestuffsin$ cd stcloudbus/
computerusername@Computername:~/folderthatIwantcodestuffsin/stcloudbus$ 
'''

Now here's a quandry, what happens if say, @oconnellamethyst updates everything in this repository, and you want your folder on your computer to stay up to date with my shenanagins, so that you can add your code. That's pretty easy, you just need to tell git that this is the upstream. Before you do this, you usually want to make sure you don't already have an upstream, like so.

'''
computerusername@Computername:~/folderthatIwantcodestuffsin/stcloudbus$ git remote -v
origin	https://github.com/githubuser/stcloudbus.git (fetch)
origin	https://github.com/githubuser/stcloudbus.git (push)
'''

You're good. You've only got your stuff in there. Now, since you are on this page, and you are reading these instructions, you should go click that green button on this page to get the url. Then, in your terminal, type.

'''
computerusername@Computername:~/folderthatIwantcodestuffsin/stcloudbus$ git remote add upstream https://github.com/NorthScript/stcloudbus.git
'''

Now if you do '''git remote -v''' again, you'll find...

'''
computerusername@Computername:~/folderthatIwantcodestuffsin/stcloudbus$ git remote -v
origin	https://github.com/githubuser/stcloudbus.git (fetch)
origin	https://github.com/githubuser/stcloudbus.git (push)
upstream	https://github.com/NorthScript/stcloudbus.git (fetch)
upstream	https://github.com/NorthScript/stcloudbus.git (push)
'''

Note that, typing the same command twice, it's hard on your wrists. You don't want carpal tunnel. Luckily, the terminal doesn't either, so if you've already used a command in the terminal, and you want to use the same command again, you can use the up arrow key until you get to the command and then press enter. Nifty eh?








