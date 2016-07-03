---
layout: userguide
title: User Guide
---

# 1. Develop locally

The [QuickStart page](/quickstart.html) shows you how to create and edit your portfolio "in the cloud" using only a browser. While this is a simple way to get started, there are some advantages to developing your portfolio locally:

  * You can use your favorite text editor or IDE for writing (Emacs, Eclipse, IntelliJ Idea, etc.). Note: not Microsoft Word! 
  * After installing Jekyll, you can build and review the site instantly on your computer after making changes. 
  
There are two components to developing your techfolio locally: (1) managing a local copy of your techfolio repo, and (2) running Jekyll locally to build your site.  

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

# 3. Anatomy of bio.json