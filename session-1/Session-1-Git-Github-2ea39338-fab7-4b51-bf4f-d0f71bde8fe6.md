# Session 1: Git / Github

*Teaching curriculum for SWE & WIT website building program.*

---

## Outline of Topics

- What is Git / Github? How are they different?
- Why version control is important for long-term development
- How to download Git (if necessary)
- How to set up a personal Github account
- Joining a Github organization
- What is a repository?
    - What does `git clone` do? → How to clone `swe-wit.github.io`
- How to code in a file?
- What commands can you use?
    - `git push`
    - `git pull`
- What are merge conflicts and how do we avoid them?

---

## What is Git / Github?

**Git** is a system to manage code development. It keeps track of the different versions and programmers of a programming project.

**Github** is a online hosting system for Git projects. 

Both are examples of version control software**.** 

→ **Version control** is an important part of code development. There's many reasons that long-term projects require version control:

- if you make a mistake and want to go back to an earlier version of your code,
- if you're working with multiple people and you want to know who's been doing what,
- if you want to base multiple projects off of one starter project,

etc. 

## How do I get started with Git & Github?

You need to make a Github account!

Start by visiting [github.com](https://github.com), then click *Sign Up* in the upper left corner*.*  

Fill out your info and click *Select a Plan* at the bottom. 

Choose the free one (lol). 

Complete the setup. 

A verification email will be sent to the email address you specified. Go ahead and verify your account.

You'll be taken to the *Create a new repository* page but **we are not going to create a new repository.** If you ever want to make your own projects, that's where you'll start. 

Click the icon in the top left corner, and then select *Signed in as [your username]* on the drop-down menu. You're now looking at your Github account!

![](mygithub-7d20d14e-ef4f-414f-a502-b2cb001b954a.png)

For example, this is my Github account! It displays my repositories, contribution history, and organizations. 

## What are the basic elements on this page?

- **Repositories:** a Github repository is like a folder that holds all the files you need for a specific project (we call them "repos" for short)

    → *What's the difference between that and a Github project?*

    A **project** on Github can only belong to an organization or repository; since you can't have one belong to your account, they're not meant for individual work.

- **Contribution history:** the little squares you see correspond to a day, and the more green it is, the more work you did using Github that day.
- **Organizations:** a Github organization is where you can store multiple repositories that will be used by its members.

Right now, I'm adding everyone here to the `[swe-wit](http://swe-wit.github.io)` organization. Go ahead and visit [https://github.com/swe-wit](https://github.com/swe-wit).

You should (eventually) see a banner at the top of the page saying I've invited you to join `swe-wit`. Click *View* and then *Join swe-wit.* You should now see this page:

![](swe-wit-e87fb42f-47ea-4575-bf4d-0dad3e125c91.png)

swe-wit organization page. There are two repositories.

The first repository contains lesson plans & notes for our sessions. The second contains the code that will launch our website! 

Click on *[swe-wit.github.io](https://github.com/swe-wit/swe-wit.github.io)* repository.

You're now viewing the following page:

![](repo-4cb86ed1-e0e2-4094-ab30-cc4b96704459.png)

swe-wit.github.io!

The most important files are `index.html` and `style.css`. We'll get to those in Sessions 2 and 3. 

## Get ready to code!

The last thing we're going to do is to clone this repository from the remote repository to your local computer. 

- **Clone:** this basically means the same thing as copy!
- **Remote:** existing on Github.
- **Local:** existing on your computer.

There's a big, green button on the left-hand side that says *Clone or download.* Click that and copy the weird stuff in the box. 

Then, open a *command-line interface.* On my Mac, it's called *Terminal,* and it looks like this:

![](terminal-9fdaaf25-ac5e-4ced-9383-e1641de6ce41.png)

You just open it like you would any other app.

If you're using a different computer / operating system and need help, please let me know.

Type the following:

`git clone [paste what you copied!]`

and then hit enter. Now when you type `ls` (which is short for list), you'll see a list of your files, including `swe-wit.github.io`.

You now have the repository downloaded onto your local computer. There are other things you'll need to know to start coding, but you can review them below on your own time. 

Thank you all!

---

## How do I code in a file?

There are many *text editors* that will let you do this. We're going to use one that you can open from your command line, called *vim.* 

To try it, type `vim index.html`. You should see this:

![](vim-18e17cbe-bdc6-4f11-8fdc-a939f420c45f.png)

index.html opened using vim. 

You can use your arrows to go back and forth. To edit the file, press `i` to enter *insert mode.* 

When you're done, press `esc` + `:wq` to save and quit, or `esc` + `:q` to quit without saving.

## How do I update the changes I've made to the repository I see on Github?

When inside the `[swe-wit.github.io](http://swe-wit.github.io)` directory on your computer, type the following:

`git add .`

`git commit -m "[your message here]"`

`git push origin master`

*the `.` in the first command means "all files"

*the `"[your message here]"` in the second file is a little message you enter to talk about what's been updated since you updated last.

## How do I bring new changes that exist on Github onto my own computer?

When inside the `[swe-wit.github.io](http://swe-wit.github.io)` directory on your computer, type the following:

`git pull`

And your directory should update to match the repository on Github.

## What are merge conflicts?

We have to be careful when working with many other people on the same project! Sometimes multiple people try to update the remote repository with their individual changes at the same time. 

This can lead to **merge conflicts,** which are when people try to push their competing versions to Github. It's ok if this happens — Git is designed to handle these situations (let us know and we'll help you). 

But to avoid merge conflicts, make sure you communicate about who is working and when, and:

1. *always push your changes when you are done working.*
2. *always pull when you begin working.*