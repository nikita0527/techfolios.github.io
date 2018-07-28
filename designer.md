---
layout: userguide
title: TFD
---

# 1. Motivation

TechFolio Designer (TFD) is a cross-platform desktop application, implemented using [Electron](https://electronjs.org/), which is intended to simplify the management of your professional portfolios. 

Prior to the development of TFD, creating a personal TechFolio required choosing between the following:

  1. Edit TechFolio files in the cloud using GitHub's browser-based editing tools.  This requires no setup, but it is easy to make errors while editing in the browser. In particular, it is very easy to make mistakes while editing the bio.json file.
  
  2. Edit TechFolio files locally. This requires learning to use a git client (so that you can download the files to edit, and upload them back to GitHub after you've finished), and using an IDE to edit the files. This requires some sophistication with git as well as knowledge of an IDE. In addition, as the IDE does not "know" about the structure of TechFolio files, it is still relatively easy to make errors.  
  
TFD provides a third alternative, one which builds in knowledge about the structure of TechFolio files and how they are represented at GitHub.  This means:
  
  * TFD provides a simplified interface to Git and GitHub. After authenticating, TechFolio provides simple menu commands to obtain your portfolio files from GitHub for editing and to upload them back to GitHub for publication. 
  
  * TFD provides editors for Projects and Essays. Since these editors are designed to be used only for TechFolio files, they can build in knowledge about Markdown and YAML front matter to prevent common problems.
  
  * TFD provides a simplified, form-driven user interface for editing the bio.json file. This ensures that the JSON file syntax is maintained.  

TFD is still under initial development, and does not yet implement all of the features we have planned. We hope that you will find it convenient to use even in its preliminary state.

# 2. Installation

## 2.1 Install git

TFD requires that you have `git` installed as a command line tool.  To install Git, please follow the appropriate instructions for your operating systems at the [Git Download Page](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). 

Before installing TFD, please verify that you have successfully installed git by opening a shell and typing `git --version`. (On Windows, be sure that the git command runs in a "regular" shell, not just a PowerShell.) For example:

<img style="" width="500px" src="images/designer/git-version.png" class="img-responsive">

## 2.2 Install TechFolio Designers

After you have installed git, go to the [TechFolioDesigner Release Page](https://github.com/techfolios/techfoliodesigner/releases) and download a copy of the latest release appropriate for your platform. We strive to have releases for Windows, Macintosh, and Unix.

Download the version for your platform and install in the appropriate manner.

  * For OSX, download the zip file containing the string "darwin-x64", unzip it, and move the application to your /Application directory.
  * For Linux, download either the .rpm or .deb file depending upon your Linux version, and install using the appropriate utility.
  * For Windows, download the .exe file and run it to perform the installation.
  
# 3. Using TechFolio Designer

Prior to using TFD, you should have completed steps 1 and 2 of the [QuickStart](quickstart.html).  This means that you have created a *username*.github.io repository at GitHub, and navigating to http://*username*.github.io will display the Molly Maluhia template techfolio.

## 3.1 Initial configuration

Once you have TFD installed, the first step is to configure it so that it can download your TechFolio files from GitHub and upload them after you've edited them.  This takes a few steps, but you only have to do them once. 

First, invoke TFD.  It will bring up the TechFolio "Splash" window, which will look like this:

<img style="" width="500px" src="images/designer/splash-window-initial.png" class="img-responsive">

As you can see from the red highlights, there is some missing information that TFD needs before you can proceed. 

TFD provides a "Config" menu to manage the interactions with GitHub. If you pull it down right now, it will look like this:

<img style="" width="300px" src="images/designer/config-menu-initial.png" class="img-responsive">

Several items are greyed out until you have logged in to GitHub. Let's do that now. 

### 3.1.1 Login to GitHub 

Click the "Login to GitHub" menu item in the Config menu and the following window should appear:

<img style="" width="500px" src="images/designer/signin-to-github-window.png" class="img-responsive">

As requested, type in your GitHub username and password and click "Sign in". If successful, you will now see the Splash window again, but now the "Console Logs" pane shows that some interaction occurred.

<img style="" width="500px" src="images/designer/signin-splash-window.png" class="img-responsive">

The bottom line requests that you "login to GitHub one more time".  Use the Config menu to do that, and you'll now get an authorization window that looks something like this:

<img style="" width="500px" src="images/designer/authorize-window.png" class="img-responsive">

After clicking the Authorization button, you'll once again see the Splash Window, with a second request to "login to GitHub one more time":

<img style="" width="500px" src="images/designer/signin-splash-again.png" class="img-responsive">

Please use the Config menu to click on the "Login to GitHub" menu item for the third (and final!) time. Now the Splash window should look like this:

<img style="" width="500px" src="images/designer/splash-window-logged-in.png" class="img-responsive">

The result of all this clicking is to provide TFD with an "personal access token" that it can use to both read and write to your public repositories on GitHub. 

### 3.1.2 Specify your TechFolio repo

The next step is to tell TFD which repository is your TechFolio repo.  From the Config menu, choose "Set GitHub repo name", which will bring up the following window:

<img style="" width="500px" src="images/designer/set-github-repo-name-window.png" class="img-responsive">

Note that it defaults to the expected value. You can just click "OK."  Now the Splash Window should show that the GitHub Rep name field has been set:

<img style="" width="500px" src="images/designer/splash-window-github-repo-set.png" class="img-responsive">

### 3.1.3 Clone your repo

As you can see, we still need to provide a local directory the contains the TechFolio portfolio.  In order to do that, we need to "clone" the repository from GitHub into someplace in our local file system.  To start this process, use the Config menu to select the "Clone repo into directory".  After selecting this item, a platform-specific File Chooser window will appear. Here's what mine looks like:

<img style="" width="500px" src="images/designer/file-chooser.png" class="img-responsive">

We now need to select a location into which a new directory (called *username*.github.io) will be created and which will hold your TechFolio files. I will choose "/Users/philipmjohnson/github" as the location and click "Open". After doing so, the File Chooser window disappears, and the bottom line of the Command Log pane in the Splash window now looks like this:

<img style="" width="500px" src="images/designer/clone-splash-window.png" class="img-responsive">

Notice that it tells you this process may take up to a minute to complete.

After a little while, the download completes, the Command Log pane tells you so, and the Local Directory row has now turned green and indicates the location of your TechFolio files:

<img style="" width="500px" src="images/designer/clone-splash-window-completes.png" class="img-responsive">

Just to prove the point, here's the window displaying the contents of my TechFolio files in the /Users/philipjohnson/github/ directory:

<img style="" width="500px" src="images/designer/github-techfolio-directory.png" class="img-responsive">

You're now ready to edit TechFolio files. Note that the "Bio", "Projects", and "Essays" menus now display the files associated with your project. For example, here's what my "Projects" menu looks like after cloning my TechFolio:

<img style="" width="200px" src="images/designer/projects-menu.png" class="img-responsive">

Note that TFD saves these settings, so the next time you run the system, you won't have to redo all of this information. You will have to select the "Login to GitHub" menu item each time you login, but this is just so that system can check to make sure that your Personal Access Token is still valid. You shouldn't have to enter your credentials again.

## 3.3 Editing bio.json

Editing the bio.json file is one of the most error-prone tasks when setting up your TechFolio, because the JSON syntax is fairly complicated and verbose, and GitHub provides little to no useful error messages when you make a mistake while editing this file. One of the goals of TFD is to make it much easier to edit the bio.json file by providing a form-based user interface.  To bring up this interface, use the "Bio" menu to select the Simple Bio Editor menu item:

<img style="" width="200px" src="images/designer/bio-menu.png" class="img-responsive">

### 3.3.1 Simple Bio Editor

After selecting the Simple Bio Editor menu item, the following window appears for me:

<img style="" width="800px" src="images/designer/simple-bio-editor-basics.png" class="img-responsive">

First, note that this window is tabbed and contains eight sections: Basics, Networks, Education, Work, Skills, Interests, Awards, and Activities.  These correspond to the major sections of the bio.json file.  You can edit any fields in the tab that you like, but you have to press the "Save" button at the bottom in order to save your changes to your local bio.json file. 

Here is what the Networks tab looks like for me:

<img style="" width="800px" src="images/designer/simple-bio-editor-networks.png" class="img-responsive">

Because this is a "Simple" editor, you are limited to three networks. If you need more, you can use the "regular" Bio editor (see below).

Finally, here is what the Work tab looks like for me:

<img style="" width="800px" src="images/designer/simple-bio-editor-work.png" class="img-responsive">

Again, you are limited to three work entries. 

### 3.3.2 "Regular" Bio Editor

The Simple Bio Editor gets some of its simplicity by limiting your choices. For example, you can't list more than three networks.  In the event that you want to go beyond what is available with the Simple Bio Editor, you can use the "regular" bio.json editor, which you can invoke by selecting "bio.json" from the Bio menu. The following window appears when I select this item:

<img style="" width="800px" src="images/designer/bio-json-editor.png" class="img-responsive">

Using this editor, you can now make any changes you like, but you must be careful to adhere to JSON syntax.

Note that once you edit the file, an "*" appears next to the file name in the title bar indicating that the buffer has been changed. To write out the file, use control-s on Windows and Unix, and command-s on Macintosh.

### 3.3.3 Publishing your changes

After making changes to your bio.json file, you will usually want to publish your changes so that they appear in your online techfolio.  To do that, you need to "push" the changes you made to your local copy of your files back to GitHub.

First, let's see if there are any changes!  To determine if you've made any changes since cloning the repo from GitHub, use the Config menu and select "Check local directory status". Here's what my Splash window looks like after selecting this item:

<img style="" width="500px" src="images/designer/splash-window-local-dir-status.png" class="img-responsive">

You can see that the "Local Directory Status" row has been updated with a timestamp and the information that the file bio.json has been modified. You can also see that the Command Log pane has been updated to indicate that this command was run.

Running the Check local directory status command is optional, but it's often useful to make sure you know exactly what has changed before you push changes. 

To publish your changes, select the "Push changes to GitHub" item from the Config menu. You'll see the Command Log update immediately with the message "Starting push of local dir to GitHub". In my case, the push completed after six seconds, as shown in the Command Log pane which now shows "Finished push":

<img style="" width="500px" src="images/designer/splash-window-after-push.png" class="img-responsive">























 












   


