# Earth Lab git tutorial - July 27, 2016 Noon to 1 PM

# Pre-workshop prep

At least one day before the workshop, please do the following:

## 1. [Install git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) on your laptop or workstation

## 2. [Set up git](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)

Make sure that you have defined your user name, e-mail address, and default text editor (e.g., [nano](https://www.nano-editor.org/)). The easiest way to do this is via the terminal, following the instructions [here](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup). If you are using Windows, you will want to use the bash shell ([instructions for installing bash on windows here](https://www.rc.colorado.edu/training/workshop/2016basicsbootcamp)).

## 3. Sign up for a free account on [GitHub](https://github.com/)

If you are a student you are eligible for the [Student Developer Pack](https://education.github.com/pack) which includes some nice functionality.


## 4. Fork this repository

Go to [https://github.com/mbjoseph/git-participants](https://github.com/mbjoseph/git-participants) and [fork the repository](https://help.github.com/articles/fork-a-repo/) by clicking on the Fork button in the upper right corner.
A repository is a collection of files associated with one project. Forking a repository creates a personal copy of the files associated with your GitHub username.

## 5. Clone the repository

Congratulations! You now have your own copy of the repository on GitHub at https://github.com/yourusername/git-participants. The next step is to pull the repository down to your local machine (i.e., your laptop). To do this, you will use the `git clone` command from bash (your terminal), substituting your GitHub username:

```
git clone https://github.com/yourusername/git-participants
```

## 6. Make changes

You should now have a local copy of your repository in a folder called git-participants.
Now, you are going to add two files to the repository:

**File 1: your picture**

Choose a picture to represent yourself.
This can be a real picture, or if you like, download a free image with a CC-0 license from a site like [pixabay](https://pixabay.com/).
Don't use large files - ideally they are < 1 MB.
Place this image file (e.g., `glamour_shot3.jpg`) in the `img/` folder.

**File 2: your bio**

Create a file with the filename formatted as YYYY-MM-DD-yourname.md (e.g., [2016-07-20-mbjoseph.md](https://raw.githubusercontent.com/mbjoseph/git-participants/gh-pages/_posts/2016-07-20-mbjoseph.md)) in the `_posts/` directory.
The contents of the file should be as follows:

```
---
title:  "Your name"
subtitle: "Your job"
date:   YYYY-MM-DD
image: "img/glamour_shot3.jpg"
---

Something about yourself here.
```

substituting your name, job, the date, the path to your image, and writing a little something about yourself.
Be sure that your file includes the lines that consist of only dashes (e.g., `---` on lines 1 and 6).
These dashes delineate the "front-matter" of your file, which gets used later.

## 7. Add and commit your changes with git

Go back to the terminal and type `git status`.
This command should print a message that provides information about which files were modified, deleted, etc.
Because we added files, there should be two files under the *Untracked files* section: one called something like `img/glamour_shot3.jpg` and another like `_posts/2016-07-23-hjsimpson.md`.
If we want git to track changes in these files we have to `add` them as follows:

```
git add img/glamour_shot3.jpg
git add _posts/2016-07-23-hjsimpson.md
```

After executing the above commands, type `git status` again.
This time, you should see the image and markdown file under the *Changes to be committed* section rather than the *Untracked files* section.
Once you're sure that the files are correct (make sure the image is in the `img/` folder and the .md file is in the `_posts/` folder), then you are ready to commit the changes.

Committing changes can be thought of as creating a snapshot of the state of a file.
Committing changes will create a permanent record of the file that can be referenced later on at any time.
This is useful when things break, because you can always revert back to previous commits.

Whenever you commit changes, you have to provide a commit message - a short description of the changes that you are committing.
The commit message is provided in quotes after a `-m` flag to the `git commit` command.
Execute the following, substituting your own commit message:

```
git commit -m 'add bio and picture for Homer Simpson'
```

## 8. Push your changes to GitHub

After committing your changes, you are ready to push to GitHub.
Pushing your changes will take whatever commits you have locally and represent these remotely (on GitHub).
Pushing is as simple as:

```
git push
```

## 9. Creating a pull request

If you pushed your changes, then they will be reflected when you visit your forked repository on GitHub at https://github.com/yourusername/git-participants.
To integrate your changes with the original repository, you'll need to open a pull request.
Pull requests are used when you want to merge two repositories (or branches within repositories) together into one.

To open a pull request, click the "New pull request" button in your repository.
This will take you to a "Comparing changes" page.
Make sure that the base fork is set to mbjoseph/git-participants, and that the head fork is set to yourusername/git-participants.
The base fork receives changes from the head fork.
You should see a green button that says "Create pull request".
Click that button and enter a title and description for your pull request.
The pull request will show any differences between the base fork and the head fork, allowing easy comparisons.

Once you open the pull request, I (Max) will evaluate your changes, let you know if anything needs to be fixed, and then merge your changes once everything looks good!


### Attributions
Forked from [Jekyll_modern-blog](https://github.com/inded/Jekyll_modern-blog), which is based off of this [article from Codrops](http://tympanus.net/codrops/?p=24222).

### License

Released under the [GNU GPL license v3](https://www.gnu.org/licenses/gpl-3.0.html).
