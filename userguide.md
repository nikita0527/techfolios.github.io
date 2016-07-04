---
layout: userguide
title: User Guide
---

<p style="padding-top: 20px">This User Guide provides tips on how to increase your effectiveness at building and maintaining your portfolio after mastering the directions in the QuickStart.</p>

# 1. Develop locally

The [QuickStart page](/quickstart.html) shows you how to create and edit your portfolio "in the cloud" using only a browser. While this is a simple way to get started, there are some advantages to developing your portfolio locally:

  * You can use your favorite text editor or IDE for writing (Emacs, Eclipse, IntelliJ Idea, etc.). Note: do not use Microsoft Word! 
  * After installing Jekyll, you can build and review the site instantly on your computer after making changes. 
  
There are two components to developing your techfolio locally: (1) managing a local copy of your portfolio repo, and (2) running Jekyll locally to build your site.  

### Manage your portfolio files locally

To manage your portfolio repo on your computer, you will need to acquire basic familiarity with [git](https://git-scm.com/) and its implementation in GitHub.  

While teaching you about git and GitHub is beyond the scope of this User Guide, here are some pointers to get you started:

  * [GitHub Hello World Guide](https://guides.github.com/activities/hello-world/). An introduction to managing GitHub repositories.
  * [GitHub Tutorial for Beginners](https://www.youtube.com/watch?v=0fKg7e37bQE). A 20 minute introduction to git and GitHub. 
  * [GitHub Desktop](https://desktop.github.com/). A desktop application to simplify basic git tasks for cloning repos and committing changes.
 
Although git can get really complicated really quickly, you only need to know enough to do the following:

  * Clone your GitHub techfolio repo onto your local computer.
  * Edit your techfolio files locally.
  * Commit your local changes to GitHub.
  
Once you understand the basics of git and its implementation in GitHub, you no longer need to use a browser to edit your portfolio files. Instead, you can create or edit portfolio files on your computer using your favorite editor, then commit those files to GitHub.  GitHub will then invoke Jekyll to rebuild your site and you can see the results in your browser. 
 
### Build your portfolio site locally

Once you are able to manage a local copy of your portfolio files on your computer, you can now install Jekyll so that you can build and review your site without committing to GitHub. 
 
First, follow the [Jekyll installation instructions](https://jekyllrb.com/docs/installation/).

Second, open a shell window, cd into your portfolio directory, and run the following command:

```sh
jekyll serve --baseurl ''
```

Third, open a browser and go to [http://localhost:4000](http://localhost:4000).  You should see the home page of your site. 

# 2. Getting updates

When you fork the TechFolio [template repository](https://github.com/techfolios/template) while following the QuickStart, you create your own "snapshot" of that template code.  However, the template code will occasionally be updated with new themes or other improvements. Major improvements to the template will be publicized in the [News Page](/news.html), so you can check there occasionally to see if there are updates to the template. 

To incorporate an updated template into your own portfolio, you have to create a copy of your GitHub repo on your local computer, merge the updated template repo into your local copy of your portfolio, then push your updated local copy back to GitHub. 
    
More specifically:

First, follow the instructions in [Manage your portfolio files locally](/userguide.html#Manageyourportfoliofileslocally) to obtain a local copy of your portfolio files on your computer.

Second, open a command shell, and cd into your portfolio directory. 

Third, execute the following commmands:

```sh
% git fetch techfolios
% git merge techfolios master
% git push origin master
```

For more details on this process, consult [Syncing a fork on GitHub](https://help.github.com/articles/syncing-a-fork/). Note that the template repository will already be set as an upstream repository with the name "techfolios". You can see this by executing the following command:

```sh
% git remote -v
```

In rare cases, the merge command will indicate conflicts. In this case, you will need to resolve the conflicts, commit your changed files, and then push the results.  See the [Help](/help.html) page if you need assistance. 

# 3. Anatomy of bio.json