
## Recap

If you've gone through this sequentially, you've  done [[Preparing To Write Code]] and have walked through [[The Hard Way]].

You should have Intellij Idea Ultimate installed, SKDMAN! installed with a JVM available to use. 

Ideally, if you did the `The Hard Way` you have an initial project you've read through so you have some expectation of what `The Easy Way` will make easier for us, and what the end result will be.

If you're not going through this sequentially, that's fine too. `The Easy Way`, is Easy, and we'll be making a new, but extremely similar project to `The Hard Way`, just easier. 


## Step 1: Make a project

Start by Opening Intellij Idea

You'll be presented with a pane that looks something like like this (mine has the [Catppuccin Theme](https://github.com/catppuccin/jetbrains))

![[IdeaWelcomePage.png]]

Click "New Project"

Click Kotlin on the left hand side under New Project

![[IdeaKotlinCreate.png]]

Wait for the project to open and load, there will be a progress bar on the bottom  that might say indexing. If the code loads and says Kotlin not configured, click configure and select Java (JVM).

When it's all said and done, and indexed you'll see something like this (assuming you clicked add Sample code).

![[IdeaKotlinNewProject.png]]


## Step 2: Run That Bad Boy

This is `The Easy Way`, so we won't go into how we can make our lives harder. 

See that shiny green `Run` button next to the bug icon in the top right of the IDE? 

Hover over that, yeah that's right it says `Run Main.kt`.

Hell yeah! 

Click `Run` and see what happens!

![[IdeaKotlinAfterRun.png]]

From here it's pretty straightforward. Browse to build.gradle.kts in the Project Explorer (left hand side file tree), click that. View it

Here it is
```kotlin
plugins {  
    kotlin("jvm") version "2.0.0"  
}  
  
group = "org.example"  
version = "1.0-SNAPSHOT"  
  
repositories {  
    mavenCentral()  
}  
  
dependencies {  
    testImplementation(kotlin("test"))  
}  
  
tasks.test {  
    useJUnitPlatform()  
}
```

If you read [[The Hard Way]] You'll notice it's even more bare bones than what gradle init made for us. 

Navigate to settingles.build.gradle

Here it is

```kotlin
rootProject.name = "koltin-hello-world"
```

Pretty simple, sets the `rootProject.name` to kotlin-hello-world. 

Observe the top of the Project Explorer. The kotlin-hello-world directory has a special icon. It's got a folder with a blue marker on the bottom right. That means it's a module known to intellij. 

Right click the kotlin-hello-world direcotry name, mouse down to Open Module Settings.

> Pro Tip: Hit Command ; to get to Module Settings faster. 

> Pro Tip: Command Shift P / Command Shift A (or set a keybinding for find action) to bring up the command palette. Type in Module Settings. Hit enter. Brings you to the same page. 


You don't have to do anything wit this yet, just observe the window. It will become your friend. Explore the options.

