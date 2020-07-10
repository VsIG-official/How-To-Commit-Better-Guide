# Guide "How to commit better"

<p align="center">
 <img src="https://imgs.xkcd.com/comics/git_commit_2x.png" width="400" height="200" />
</p>

## Table of Contents

- [Description](#description)
- [Rules](#rules)
- [Badges](#badges)
- [Example](#example)
- [Contributing](#contributing)
- [License](#license)

## Description

This is My guide "How to commit better". There You'll find some useful stuff to write **Your** commits better.

## Rules

> or guide itself

1. Commit **early**, commit **often**

It all starts with frequency. If you are starting out fresh with Git, then you should be committing early and often to your changes. Do it until it becomes second nature. When you add a method, commit. When you change something, commit. Did you rename some files? Commit. You know that floppy disk we call a save button? When you get to the point of committing your code as often as you are saving your Word documents, only then can you start winding back to a more comfortable cadence.

2. Make your commit messages **meaningful** using a semantic style

Imagine a box. You can put stuff into the box. You can take stuff out of the box. This box is the staging area of Git. You can craft commits here. Committing commits is like sealing that box and sticking a label on it. The contents of that box are your changes. So, why not have the label mean something? You wouldn’t label a moving box with kitchen items “stuff.”

Commit message composition is just as important as naming your variables and methods. If you’re following the first tip above, it’s very tempting to label a commit as simply “changes” or “savepoint.” Don’t fall into that hole.

- Specify the type of commit:

    - feat: The new feature you're adding to a particular application
    
    `feat: add beta sequence`
    
    - fix: A bug fix
    
    `fix: remove broken confirmation message`
    
    - style: Feature and updates related to styling
    
    `style: convert tabs to spaces`
    
    - refactor: Refactoring a specific section of the codebase
    
    `refactor: share logic between 4d3d3d3 and flarhgunnstow`
    
    - test: Everything related to testing
    
    `test: ensure Tayne retains clothing`
    
    - docs: Everything related to documentation
    
    `docs: explain hat wobble`
    
    - chore: Updating grunt tasks etc; no production code change
    
    `chore: add Oyster build script`

You can also use [emojis](https://getemoji.com/) to represent commit types.

- Specify **where** the changes were did (if they were in the same file (or one type of files)):

    `docs: change wrong typings [*.uml]`

- Specify the size of commit (optional):

    - s: small
    
    `s(feat): some text`
    
    - m: middle
    
    `m(feat): some text`
    
    - b: big
    
    `b(feat): some text`

3. Make your changes in each commit **atomic**

Some of you already know where I’m going with this, but for those of you who are thinking atomic means hydrogen or carbon, let me explain. We want our commits to be, in a way, transactional. When you are committing changes to your repository, they should be as minimal as possible, but with a caveat. The changes should also be related. So, if you are changing one part of your code that affects another, make sure to include all of that in one commit. I’d caution not to include everything, though. Keep your commits as small as possible, but keep your changes in each commit related. For example, you keep your constants separate from the rest of your code and include them only when necessary. If you add or update some constants in addition to including them on that new service you wrote, you should probably include those changes together. The idea behind this is so that if you need to roll back to a previous commit, you are rolling back incrementally and not in huge swaths of changes and hours of work. See rule №1.

4. **Push** your code to a remote (if you have one)

Early in our project, we had some team members who would work all day before committing their code. One commit for hours of work. This is a terrible idea. Look at it like this. Your changes don’t happen until you commit them. If you are working with others, your code does not exist until you push your changes to a remote repository. Don’t put yourself in a position to lose hours of work. Commit your code and push it to a remote if you have one. It’s that important.

5. **Never rewrite** shared history

Did you ever wish you could go back in time and Marty McFly some of the bad code you committed? Well, with Git, you can. Should you? Not if you’re working with others and your commits have already been pushed. Otherwise, just be careful. If you’ve seen Back to the Future, you already know why it’s a bad idea to change the past.

In Git, you can go back in time, rebase different branches on to other branches. You can also delete commits, rename them, squash them into single commits, and much more. If you are the only developer and it is your local machine, you tend to have more freedom than if you are working on a team. If you are working in a team that shares the same history, rewriting that history will just upset them. Git gives you the freedom to create branches and merge them back together later on, so in many cases, rewriting history isn’t necessary. Since Git already gives you the ability to checkout any previous commit, it makes sense to not alter any of your past commits so you can use any of them as a point of reference in the future.

6. Some _small_, but **useful** rules:

- The first line of the commit message should be a short description (**50 characters** is the soft limit), and should skip the full stop

<p align="center">
    <img src="https://i.imgur.com/zyBU2l6.png">
</p>

and will truncate any subject line longer than **72 characters** with an ellipsis:

<p align="center">
    <img src="https://i.imgur.com/27n9O8y.png">
</p>

- The body should provide a meaningful commit message, which:
    - uses the imperative, present tense: “change” not “changed” or “changes”:
        - **bad**: "Renamed the iVars and removed the common prefix"
        - **good**: "Rename the iVars to remove the common prefix"
    - includes motivation for the change, and contrasts its implementation with previous behaviour.

- **Referencing** issues. Closed issues should be listed on a separate line in the footer prefixed with "Closes" keyword like this:
    - Closes [#234](link)

    or in case of multiple issues:

    - Closes [#123](link), [#245](link), [#992](link)

- Separate the subject from the body with a **blank line**
- Your commit message should not contain any **whitespace** errors
- Remove **unnecessary** punctuation marks
- **Do not end** the subject line with a period
    - **bad**: Open the pod bay doors **.**
    - **good**: Open the pod bay doors

- If applied, this commit will your subject line here. For example:

`If applied, this commit will refactor subsystem X for readability.`

`If applied, this commit will update getting started documentation`

`If applied, this commit will remove deprecated methods`

`If applied, this commit will release version 1.0.0`

`If applied, this commit will merge pull request #123 from user/branch`

Notice how this doesn’t work for the other non-imperative forms:

`If applied, this commit will fixed bug with Y`

`If applied, this commit will changing behavior of X`

`If applied, this commit will more fixes for broken stuff`

`If applied, this commit will sweet new API methods`

- Capitalize the subject line and each paragraph
    - **bad**: accelerate to 88 miles per hour
    - **good**: Accelerate to 88 miles per hour
- Use the body to explain what changes you have made and why you made them.

This commit from Bitcoin Core is a great example of explaining what changed and why:

> commit eb0b56b19017ab5c16c745e6da39c53126924ed6
> 
> Author: Pieter Wuille <pieter.wuille@gmail.com>
> 
> Date:   Fri Aug 1 22:57:55 2014 +0200
> 
> Simplify serialize.h's exception handling
> 
> Remove the 'state' and 'exceptmask' from serialize.h's stream implementations, as well as related methods.
> 
> As exceptmask always included 'failbit', and setstate was always called with bits = failbit, all it did was immediately raise an exception. Get rid of those variables, and replace the setstate with direct exception throwing (which also removes some dead code).
> 
> As a result, good() is never reached after a failure (there are only 2 calls, one of which is in tests), and can just be replaced by !eof(). fail(), clear(n) and exceptions() are just never called. Delete them.

In most cases, you can leave out details about how a change has been made. Code is generally self-explanatory in this regard (and if the code is so complex that it needs    to be explained in prose, that’s what source comments are for). Just focus on making clear the reasons why you made the change in the first place—the way things worked before the change (and what was wrong with that), the way they work now, and why you decided to solve it the way you did.

- Do not assume the reviewer understands what the original problem was, ensure you add it.
- Do not think your code is self-explanatory
- Follow the commit convention defined by your team
- Bullet points are okay, too
- Typically a hyphen or asterisk is used for the bullet, preceded by a single space, with blank lines in between, but conventions vary here

## Badges

> [![Theme](https://img.shields.io/badge/Theme-Git%20Commits-blue)](https://git-scm.com/docs/git-commit)
> [![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

## Example

```Git Commit
docs: change wrong typings [*.uml]

OR

s(docs): change wrong typings [*.uml]
```

---

## Contributing

> To get started...

### Step 1

- 🍴 Fork this repo!

### Step 2

- **HACK AWAY!** 🔨🔨🔨

---

## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- **[MIT license](http://opensource.org/licenses/mit-license.php)**
- Copyright 2020 © [VsIG](https://github.com/VsIG-official).
