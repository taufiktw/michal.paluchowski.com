---
author: michal
title: "Home directory scourge"
date: 2019-09-06T12:51:24Z
categories:
  - Technology
tags:
  - operating systems
image:
---

The one-stop shop for all your user data. Home directories. Easy to backup, easy to migrate. Available since the dawn of multi-user operating systems. Am I the only one in the world who despises them?

<!--more-->

*nix systems [since forever had some variation][wikipedia-home-directory] of the `/home/<username>` directories, where everything user-specific was collected: configurations, settings, history, documents, downloads, multimedia and so forth. Windows joined the club with NT (and for the average user with Windows XP) where the earlier `C:\My Documents` was moved to the new `C:\Documents and Settings\<username>\My Documents` and later simply `C:\Users\<username>\...`.

The intention is benign: **make it easy for users to find all their data**. Start from your home directory, follow the pre-defined structure inside and *voilà*, there's that document you were looking for. Also, keeping everything in one place [becomes a sort-of memento pattern][memento-pattern], where you can back up all the files with a single command and path. No worries about missing something. It's all in one place.

That's all good and fine, but reality is a little trickier. The thing is, software you install is built by other people, who have their own views on how to structure information, which they put into practice by storing configurations *in your home directory* the way *they* like it, not necessarily the way *you* want it. So, my Linux home directory looks like:

```
.3T/            .aws/               .bash_aliases
.bash_history   .bash_logout        .bash_profile
.bashrc         .bouml              .boumlrc
BRF/            .cache/             code/
.config/        .cups/              .dbshell
.dbus/          Desktop/            Documents/
Downloads/      .embedmongo/        .gconf/
gdrive/         genealogy/          .gitconfig
.gnome/         .gnupg/             go/
.gphoto/        .gradle/            .gramps/
.gvfs/          .ICEauthority       .IntelliJIdea2019.2/
.java/          .lesshst            .local/
.m2/            .mongorc.js         .mozilla/
Music/          .node-gyp/          .npm/
.nvm/           .oracle_jre_usage/  .packer.d/
Pictures/       .pki/               .profile
.psql_history   Public/             resources/
.rnd            .sambox.cache       .selected_editor
snap/           .ssh/               Templates/
Videos/         .vscode/            .wget-hsts
.zoom/
```

__Where, in this whole mess, is *my* data?__ The code I wrote, the documents I produced?[^1]

Yes, I could just list these sans the `-a` flag, which would've dropped all the items starting with a dot `.`, conventionally known as "hidden". Same for Windows, where files and directories with a "hidden" attribute are by default not displayed by Explorer. But I'm not a regular user. I'm what you'd call a "power user", and I frequently delve into these hidden directories and files, so keeping them invisible would be impractical. Besides, many of the non-hidden items are also not part of what I consider my data, which I curate and structure to my liking.

Everybody has their own way of organizing information, so that it's easy to retrieve. We cannot possibly memorize every piece of text or image we've ever encountered. The brain doesn't work that way. Instead, **we memorize the locations of these items, and we take shortcuts, by grouping multiple items into one location**. Ie. all downloaded files go into "Downloads", so you don't need to remember where exactly the `hot-new-music.mp3` file went, you only need to remember that:

1. it was downloaded from the internet, and
2. all downloads are stored in the `Downloads` directory.

And item (1) is shared between all files of the same origin.

Your brain's [hippocampus is responsible for dealing with spatial memories][hippocampus]. That's what a directory tree is---a space in which we place items that we want to retrieve in the future. And since everybody's brain is different---neurons connect differently, based on your genetic markup and experience you acquired over your lifetime---then everybody's preferred spatial structure for storing information is different.

Then, what about the easy backups? Having to copy just a single directory and being able to restore it easily. That certainly works, as long as you don't mind having really bloated backups. Local program store all kinds of stuff in their directories, *including executables*, because home directories are user-writable without requiring administrative rights[^2]. My own home directory is currently at 24GB, out of which *maybe* 100MB is worth keeping in a backup. Everything else is configurations, executables, local caches and so on. I have to maintain a whitelist of paths to copy anyway---which naturally erodes with time and will always be missing something.

## My approach

My own way of organizing personal data is to keep it outside the home directory and under my strict control. Let software keep its order---whatever the programmers prefer---and I'll keep mine.

Because I've been primarily a Windows user since forever, my typical solution is to **create a separate disk partition called DATA**, usually with the drive letter D, and put a base structure there:

```
Code        # source code
Documents   # text files, spreadsheets, etc.
GDrive      # synced Google Drive content
Genealogy   # my family tree
Inbox       # downloads, anything pending sorting
```

I normally don't keep any music or photos on my computers, storing them on a NAS instead. Temporarily such files may reside inside `Inbox`, until I decide what to do with it---delete or label and move to the NAS. (Plus, in the age of Spotify and Netflix, one rarely needs to store multimedia locally.)

Keeping a separate partition, plus the NAS, made it **very easy to reinstall Windows**, because I only needed to wipe the system partition (typically drive C) and install everything back there, while the other partition(s) remained untouched. Nowadays that's less of a benefit, because Windows never really needs to be reinstalled, but still, the drive/partition abstraction creates a strict boundary between my curated data and everything else.

I admit, I don't have a solution for Linux, yet. There are no drives to speak of and everything is inside this single tree of directories. For the time being, I keep my stuff in the home directory and suffer slightly. But it's less of a suffering than it was on Windows, because with Linux one tends to work mostly from the terminal and I memorized most of the paths I go to, without having to list files outside of them. It's efficient enough and only my sense of order is hurt sometimes, when I press tab twice in the wrong place, then get hit with the nasty list of everything that's inside `~`.


[^1]: Windows is even worse these days, because Windows-centric applications store their data inside `C:\Users\<username>\AppData\...`, but Linux-centric apps sprinkle their files in dot-directories right inside `C:\Users\<username>\...`.
[^2]: This, of course is meant to make software and its updates easier to install, also for regular users, who may not have root/administrator rights on their machines.

[wikipedia-home-directory]: https://en.wikipedia.org/wiki/Home_directory
[memento-pattern]: https://sourcemaking.com/design_patterns/memento
[hippocampus]: https://www.verywellmind.com/what-is-the-hippocampus-2795231
