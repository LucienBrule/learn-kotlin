
So you've done [[Getting Started]] and have a development environment setup. That's great! Now we're going to prepare to write code. First, for illustrative purposes we're going to do it "The Hard Way", then we'll do it "The Easy Way"

The right way of course is the middle path, something between the hard and easy way. Walk the middle path once you've known the hard and easy way. 

## The Ways

**What is the Hard Way?**

- From the command line, with little to no code generation
- We make our directory structure by hand
- We make our build scripts by hand
- Less magic happens

See [[The Hard Way]]

**What is the Easy Way?**

- From the IDE with code generation
- The IDE sets up our directory structure for us
- The IDE gives us a boilerplate starting point to 'just write code'
- Almost all the magic happens

See [[The Hard Way]]

**What is the Middle Path?**

- Ask and you shall receive
- Seek and ye shall find
- Knock and it will be revealed unto to you
- Magic happens but you have full control over the magic

See [[The Middle Path]]
## Setting Up A Developer Directory

You might have personal preferences on how you organize your code. 
For my own sanity, I'm going to assume you do something sane. 

Also for posterity I'm going to describe the system I use to organize my source on my development machine. You'll want to either copy my setup if you don't have one that works for you. 

You need to do this no matter which path you take.

If you're on windows, I'm going to assume you're smart enough to do this in WSL or you have enough preferences to have your own setup. 

### Instructions

Here we're going to setup an initial Developer folder in our Home directory. 

```bash
cd # Go Home (~/.)
mkdir Developer # Make a developer directory
cd Developer # enter developer
mkdir {etc,opt,src} # make etc , opt, source directories
cd src # enter source directory
mkdir {active,scratch,archive} # make active, scratch archive directories
```

Once we've done this we have some primitives to work with, I'll explain them.
But first here's what a more flushed out directory structure might look like, it's left as an exercise to the reader to make the other directories (as they see fit)

```bash
~/Developer❯ tre -l 3
.
├── etc
│   ├── dotfiles
│   ├── secrets
│   └── notes
├── opt
│   └── oss
└── src
    ├── archive
    ├── scratch
    └── active
```

> tre is like tree but better, [get tre](https://github.com/dduan/tre)

So you'll notice it loosely follows the [Filesystem Hierarchy Standard](https://www.pathname.com/fhs/) . That document describes the naming convention of the directories and their purposes. 

**ie:** quickly do `ls /`, you'll notice you'll see something like: 

```bash
# or 
❯ tre -l 1 /
/
├── sbin
├── lib64
├── root
├── boot
├── sys
├── opt
├── run
├── tmp
├── var
├── lost+found
├── nfs
├── etc
├── lib
├── proc
├── home
├── mnt
├── srv
├── afs
├── media
├── dev
├── bin
└── usr
```

I'm not about to write a long winded explanation of my own system but it's pretty simple.
#### Source Directory

**~/Developer/src**

- where all your source code lives that you're writing or making patches to, whatever.

**~/Developer/src/scratch**

- where new projects that you're just testing out live
- if you're a developer, you'll test out a lot of projects
- you may clone a lot of open source projects to poke around at them, maybe make patches and drop them and never properly fork and commit back upstream
- maybe you have a new side project idea, let it incubate under scratch

**~/Developer/src/active**
- where actual projects you work on regularly, under active development are stored.
- If you're working as part of a team for say a company, make a directory for your company and clone your company's codebase there
- Long lived side projects

**~/Developer/src/archive**
- Dead code
- Old code
- Code you want to save but don't develop anymore
- ~~salvaged private source from old jobs~~
- Think of this as your special stash of secret knowledge, or old course work that you can reference. 
- Incredibly satisfying when you have to do a new requirement and you're like, oh wait I've done this before. and then plop, work is done (with edits)
#### Opt directory

On production systems opt is where programs that don't install to /bin , /usr/bin etc live. I like installing to /opt/app-root on production systems.

**~/Developer/opt**

- For programs, be they source or larger distributions that we use as tools but don't necessarily work on / commit to

**~/Developer/opt/oss**
- to give at least one example directory, and to differentiate between open source and proprietary software you might use, we use an oss directory.
- For example, I use [Open Web UI](https://github.com/open-webui/open-webui), it's not exactly fully packaged yet and I want to build it from source. So on my systems it lives at `~/Developer/opt/oss/open-webui/open-webui`.
- Note we maintain the open source maintainers distribution group in the oss folder, incase we run into forks, and so we otherwise preserve provenance at a glance. 

#### Etc directory

**~/Developer/etc**

Etc... config files, secrets, notes,text files you name it. Things you can't execute and are probably configuration for other things

**~/Developer/etc/secrets**
- cloud credentials, other peoples ssh keys ;) , love letters, offsets, sensitive notes what have you

**~/Developer/etc/notes**

- This is where I store like literally all my notes in markdown, like this document I'm writing right now. I'm using [obsidian](https://obsidian.md/), but think flat folder structure of topics for notes on various subjects.

**~/Developer/etc/dotfiles**
- dotfiles are the files that start with a dot (.) like .zshrc that you want to save. You should periodically export your dotfiles you're proud of / depend on / want to save from your home folder to `~/Developer/etc/dotfiles`, assuming you're not a nut who puts secrets in their dotfiles you may also want to make a repo and host your dotfiles so if you get a new system you can get up and running quickly with your existing tweaks macros and general setup. 

> ProTip: Install [autojump](https://github.com/wting/autojump) then instead of `cd ~/Developer/...` you can do that once and then just `j name-of-project`

If you're reading this in sequential order, and have a directory structure setup it's time to head over to [[The Hard Way]]