
## First Things First

> Bare in mind this is opinionated.

### The Right Things First

The first thing you absolutely should do when endeavoring to learn Kotlin is to - not learn Kotlin! 

Instead I would say, you should instead endeavor to gain a new skill, to accomplish more tasks more efficiently with a different toolset and different paradigm than is offered in other languages.

Second I would say, almost as a caveat to absolute beginners who may be reading this, while on one hand any language is a 'good' first language, it is my opinion Kotlin is not a 'good' first language. 

For that you may want to go to C, Python, or Java. There are many reasons for this. Many of which have to do with the foundational knowledge C programming gives you to how computers actually work, and the plethora of learning material targeted towards beginners in python.  I may expound on additional reasons why Kotlin is not a good first language later, and hopefully through the course of reading this if you're already an experienced programmer with CS knowledge it will become clear why Kotlin as a first language might be the wrong choice. 

### The Development Environment

There's a certain Zen to programming, and if we're to find our Zen and our flow state, we need a temple or a dojo to practice our craft, if not a prayer cushion and a space where we can practice (as in the case of seated meditation). 

For a base operating system, while learning Kotlin it's helpful to have a \*nix based system that has a JVM. In practice this means: 

Your development operating system should be (in priority order)

1. MacOS
2. Your favorite Linux Distribution
3. Windows with WSL2

**Why**

Yes you might ask why, and I'll tell you. We haven't learned this yet but Kotlin can compile to many different platforms from the same codebase. One killer feature of Kotlin is the ability to produce cross platform mobile applications. Unfortunately, unless you know a guy, you can only build and deploy iOS application code from a registered version of XCode, from a compute running MacOS. 

Additionally, these three operating systems support running the JVM without any hassle, and they are supported platforms for Jetbrains Intellij. 

I do however recommend, if you choose option 1 or 3 as your base development environment, go ahead and provision your favorite linux distribution as virtual machine / developer workstation that you can ssh into and run your programs on. Especially if you intend to produce web programs, your code will most likely be running on Linux anyway. 

### The IDE

Love it or hate it, Jetbrains made Kotlin, while it's wholly possible to program Kotlin code in VS Code, NeoVIM, (your favorite text editor), I've tried and it's just not as smooth. Luckily the Community Edition of JetBrains Intellij is free and Open Source Software, so if you can't afford what I'm about to recommend, use that and you'll be fine. 

> This is opionionated

The best IDE for Kotlin right now is IntelliJ Idea Ultimate. Get it.

If you're a student, or have access to a .edu email address or have smartly set your graduation date to never while registering for the Github student developer pack, congratulations! You can get the stable version for free by going to JetBrains website, registering an account, and getting a license for the all products pack. Then all you need to do is get the JetBrains toolbox, and install Intellij Idea Ultimate. 

If you're not a student, do the above but just buy a personal license. If you're using it for commercial use for your company and you have purchasing authority, ideally you should purchase the commercial edition (there is no difference in feature set), but you could very well also just buy the community edition of the all products pack and file a reimbursement. This is not legal advice, but Intellij's lawyer's aren't going to come after you personally if you happen to mis license your product. Unless you're a company, then don't be a scumbag, buy the right license. 

**Getting it for free legally**

If you're price conscious or If you're interested in not running the stable version, and like being a guinea pig for new features, the Intellij Ultimate Early Access Program (EAP) version is free for use by anyone. Caveat being you'll be on the bleeding edge release. This means that you'll be required to update your IDE quarterly, or as they do releases, and Plugins may break because they break compatibility with the API. In practice this is seldom a hinderance. Personally, I pay for the all products pack to have access to the stable versions of all of the IDES, but I run IntelliJ Idea Ultimate EAP. Mostly so I can experience bugs, have new features early and file bug reports. They really do listen to their bug reports, so that's nice. 

So yeah by now you hopefully have read some long rambling and have IntelliJ Installed. Now it's time to install the JVM.

But wait! Don't go straight to Oracle's website or brew/dnf/apt-get install Java. We're going to be smart and *use protection*. In so far as, like when we use pyenv, rvm, nodenv, etc version managers for our development toolchains, we're going to use a version manager for our JVM installations. 

So go a ahead and install SDKMAN! (the name is literally all caps with an exclamation point). Once you have sdkman installed and in your path, pick a recent JVM version, like anything above 17 and install it.

I recommend OpenJDK 20, or GraalVM EE 23 at the time of writing. But since the JVM follows a spec, pretty much any JVM you install for development will function the same for you out of the box. (With the exception of GraalVM, which will do more for you, more on that later). 

So assuming you've added sdkman to your zshrc/bashrc, have downloaded a JDK and have Intellij Idea installed, you're off the the races. 

You should now continue to the primer of [[Preparing To Write Code]]