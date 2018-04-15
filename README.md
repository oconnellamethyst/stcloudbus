# St. Cloud GTFS Project
A volunteer project led by @oconnellamethyst to create a GTFS feed for the city of St. Cloud, MN. All are welcome to join. Learn more about what [GTFS feeds are](https://developers.google.com/transit/)

A GTFS feed is a way for a transit system's data to communicate with apps, like Google Maps. We are creating a Static GTFS system for the busses in the city of St. Cloud that are not covered by the GTFS system for the Metro Transit System, specifically the busses covered by the Metro Bus system. This will allow the people in St. Cloud to use apps that use GTFS feeds, such as Google Maps, to be able to navigate their city. This will be especially helpful for incoming St. Cloud State University students, such as @oconnellamethyst who has a 50% chance of transfering there in the fall, (the U of M stopped ghosting me the moment I wrote that line about not ghosting me. Coincidence?)

### News
Actually, MetroBus should already have a GTFS Feed due to it's use of the TransitArt system, but, it is not public to my knowledge. I am checking over their website to make sure, because I am a lazy person who would rather not have to duplicate labor, but if it isn't, I totally will. If it turns out that MetroBus totally does have a GTFS Feed that is publically avalable, this repository will become a project using this GTFS feed and other Minnesota GTFS feeds to do cool website things!

### What is NorthScript?
NorthScript is a group of developers and aspiring developers that meets in Minneapolis. It is a group that uses freecodecamp.org and other resources to build on our development abilities. You can find us on our [Facebook Page](https://www.facebook.com/groups/free.code.camp.minneapolis/about/) and our [Gitter](https://gitter.im/Northscript/Lobby)

### How do I work with this repository?
As an aspiring developer, you may not be familiar with GitHub and Git, or doing things with stuff. That's okay, here's a crash course in it! If you ever need any help with any of this, drop me a line in the Gitter chat or in the Facebook Group

First, you'll need a computer. You may be thinking, "Yes, @oconnellamethyst, of course I need a computer to code, but I'm on a computer right now!" But when I say that, I mean, you need a computer that you are actually comfortable developing code in. When I first started at Northscript, I started with a Windows 7 laptop that was a pain to get anything of value to run on and had the battery life of a early 2000s cheap cell phone, it wrecked my ability to understand anything of substance in computer programming. Then that computer died and I bought a new-used [XUbuntu](https://xubuntu.org/tour/) Laptop from [Free Geek Twin Cities](http://freegeektwincities.org/) for $170, promptly installed [Ubuntu (the Long-Term Stable Release)](https://www.ubuntu.com/download/desktop) over XUbuntu just because I was getting super weird glitches when trying to install Google Chrome, and promptly realized that I had just accidentally improved my coding abilities by 200% just by getting a laptop that I didn't have to fight to code anything on. In coding, such as in life, you need tools that will work with you, not against you. I highly recommend the laptops sold by [Free Geek Twin Cities](http://freegeektwincities.org/), as not only are they recycling laptops and keeping them from going to waste, but also, they're just really good, but honestly, just get something that you aren't fighting. Coding is a battle all it's own without having to fight your computer.

Second, you need to get Git on your computer. [Installation instructions here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). Notice how easy it is to install Git if you followed my advice and got a laptop from Free Geek Twin Cities, and installed Ubuntu over XUbuntu, you just open up the Terminal and type a few lines!

Now you've got to do Github things. If you haven't created a Github account, go do that now, and make sure to verify your email. See that button in the top right corner that says Fork? Press it. Now you are making your own copy of this Repository so that you don't accidentally eat it or something IDK. Now you want a copy of your copy of this repository on your computer so that you can edit code things. Open up your terminal in Ubuntu, or the BASH Terminal emulator that comes with Git on Windows, or whatever magic you Mac folks do, and basically get a Git copy of your fork, which is a copy of this repository. On my Ubuntu, this looks something like this.

```
computerusername@Computername:~$ mkdir folderthatIwantcodestuffsin
computerusername@Computername:~$ cd folderthatIwantcodestuffsin/
computerusername@Computername:~/folderthatIwantcodestuffsin$ git clone https://github.com/githubuser/stcloudbus.git
Cloning into 'stcloudbus'...
remote: Counting objects: 34, done.
remote: Compressing objects: 100% (33/33), done.
remote: Total 34 (delta 1), reused 30 (delta 0), pack-reused 0
Unpacking objects: 100% (34/34), done.
```

I made a folder that I wanted my codestuffs in using ```mkdir``` which is short for make directory, it makes you a nice folder. I then went inside of that folder using ```cd``` which is short for change directory, it lets you go inside of that folder you just created. What if I forget what the folder is called? You might ask? That's where you use the ```ls``` command. It's short for list, and it lists all the files and directories that are in whereever you are, it's super useful, and looks something like this. Also, note, if you try to use a keyboard shortcut to copy and paste in the terminal, it wont work. You have to either do Shift+Ctrl+C or just right-click.

```
computerusername@Computername:~/folderthatIwantcodestuffsin$ ls
stcloudbus
```

See, when I git cloned my fork onto my computer in folderthatIwantcodestuffsin, it created a folder called stcloudbus, a special folder that works with git. I want in that folder, but I'm a lazy typer, so because there is only one folder, I can type ```cd s``` and then press the tab key, and since stcloudbus is the only folder that starts with an s, it will autocomplete. Nifty right?

```
computerusername@Computername:~/folderthatIwantcodestuffsin$ cd stcloudbus/
computerusername@Computername:~/folderthatIwantcodestuffsin/stcloudbus$ 
```

Now here's a quandry, what happens if say, @oconnellamethyst updates everything in this repository, and you want your folder on your computer to stay up to date with my shenanagins, so that you can add your code. That's pretty easy, you just need to tell git that this is the upstream. Before you do this, you usually want to make sure you don't already have an upstream, like so.

```
computerusername@Computername:~/folderthatIwantcodestuffsin/stcloudbus$ git remote -v
origin	https://github.com/githubuser/stcloudbus.git (fetch)
origin	https://github.com/githubuser/stcloudbus.git (push)
```

You're good. You've only got your stuff in there. Now, since you are on this page, and you are reading these instructions, you should go click that green button on this page to get the url. Then, in your terminal, type.

```
computerusername@Computername:~/folderthatIwantcodestuffsin/stcloudbus$ git remote add upstream https://github.com/NorthScript/stcloudbus.git
```

Now if you do ```git remote -v``` again, you'll find...

```
computerusername@Computername:~/folderthatIwantcodestuffsin/stcloudbus$ git remote -v
origin	https://github.com/githubuser/stcloudbus.git (fetch)
origin	https://github.com/githubuser/stcloudbus.git (push)
upstream	https://github.com/NorthScript/stcloudbus.git (fetch)
upstream	https://github.com/NorthScript/stcloudbus.git (push)
```

Note that, typing the same command twice, it's hard on your wrists. You don't want carpal tunnel. Luckily, the terminal doesn't either, so if you've already used a command in the terminal, and you want to use the same command again, you can use the up arrow key until you get to the command and then press enter. Nifty eh?

Now you've just got to keep yours up to date with my shenanagins, 

```
computerusername@Computername:~/folderthatIwantcodestuffsin/stcloudbus$ git fetch upstream
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 3 (delta 1), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/NorthScript/stcloudbus
 * [new branch]      master     -> upstream/master
computerusername@Computername:~/folderthatIwantcodestuffsin/stcloudbus$ git checkout master
Already on 'master'
Your branch is up to date with 'origin/master'.
computerusername@Computername:~/folderthatIwantcodestuffsin/stcloudbus$ git merge upstream/master
Updating 5f46644..530c7ee
Fast-forward
 README.md | 77 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++--
 1 file changed, 75 insertions(+), 2 deletions(-)
```

See, now you're up to date with my shenanagins, but how do you keep me up to date on your shenanagins? First, you'll want to make changes to the code using the editor of your choice. For this particular project, I'm just using the default text editor gedit, but like, there are lots of cooler ones. You can go old school and use Vi, you can go new school and use Visual Studio Code. Anything really. Choosing an editor can be intimidating, but it's really the same as picking a computer. Choose something that helps, not hinders, your coding process. You will probably change editors over time as you get more experience, or in employment when your boss tells you to use a certain one. That's part of the learning process, the important part is that you code something in something!

So I make a change to trips.txt in the StCloudGTFS folder using whatever, and I want to send it to senpai @oconnellamethyst, and the world really. First, you should keep up with my shenanagins to make sure that I haven't already done the thing, see above. Then, I want to update my own fork!

```
computerusername@Computername:~/folderthatIwantcodestuffsin/stcloudbus$ git add StCloudGTFS/trips.txt
computerusername@Computername:~/folderthatIwantcodestuffsin/stcloudbus$ git commit -m "This is where I describe briefly the changes I made to trips.txt"
[master d08e589] This is where I describe briefly the changes I made to trips.txt
 1 file changed, 2 insertions(+), 2 deletions(-)
computerusername@Computername:~/folderthatIwantcodestuffsin/stcloudbus$ git push
Username for 'https://github.com': githubuser
Password for 'https://githubuser@github.com':
Counting objects: 7, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 3.49 KiB | 3.49 MiB/s, done.
Total 7 (delta 4), reused 0 (delta 0)
remote: Resolving deltas: 100% (4/4), completed with 3 local objects.
To https://github.com/githubuser/stcloudbus.git
   5f46644..d08e589  master -> master
```

Then I want to navigate to my fork on Github in my web browser, and submit a pull request, which is basically just, @oconnellamethyst senpai! Please add my code! So navigate to your fork, probably found at https://github.com/githubuser/stcloudbus with githubuser replaced with your username, or also found by going to your profile, and then to your repositories, and then finding this repository. Then push the New pull request button, and then press Create pull request, and then thoroughly describe the changes made to the code in the comments, and then press create pull request. If your code is good, senpai will notice you! And that is how you do things. What we are specifically doing 'round these parts is making a GTFS system for the city of St. Cloud, so if you want to help, you're going to want to [read about GTFS](https://developers.google.com/transit/). This code project is going to be really easy, yet really boring. Basically, read the schedules, write them in the GTFS format. That's all there is to it. Once we have all the schedules, we can actually use this to navigate St. Cloud's busses using Google Maps. Neato right? [Here are the schedules](https://www.ridemetrobus.com/)





