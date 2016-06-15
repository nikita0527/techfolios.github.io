---
layout: userguide
title: Quick Start
---

# 1. Join GitHub

To get started with TechFolios, all you need is an account at GitHub. You don't need to download any software or even know how to use git. Everything you need to do when starting out can be done in a browser.  

If you haven't already, [sign up for GitHub](https://help.github.com/articles/signing-up-for-a-new-github-account) and [verify your email address](https://help.github.com/articles/verifying-your-email-address/). Choose your username wisely, as that will become part of the URL to your portfolio site.

Before proceeding, [login](http://github.com/login) to your GitHub account.

# 2. Configure template

In this step, you'll make a personal copy of the TechFolio template and configure it to be displayed as your portfolio.
 
**A.** Go to [https://github.com/techfolios/template](https://github.com/techfolios/template).
  
**B.** Press the "Fork" button on the top left of the page.
  
**C.** Choose your personal account (if GitHub presents you with a choice). Your browser will now display the home page for your copy of the template.
  
**D.** Click on "Settings" tab (top middle of the screen), and rename the repo from "template" to USERNAME.github.io, where USERNAME is your GitHub account name. Press the "Rename" button to save the new name. This will take you back to the home page. 
  
**E.** Now let's fix the summary line to link to your portfolio. Here's what it looks like now:

```yaml
Technical Portfolio https://techfolios.github.io/template -- Edit
```
     
Click on "Edit" to edit this summary line.   Change "http://techfolios.github.io/template" to "http://USERNAME.github.io/", where USERNAME is your GitHub account name.  **NOTE**: make sure you delete "template" from the URL! Click "Save" to save. When you're done the summary line should look similar to this:

```yaml
Technical Portfolio https://USERNAME.github.io/ -- Edit
```

**F.** Finally, scroll down to the file named "_config.yml".  Click on that file name to display its contents. Click on the pencil button on the top right of the screen to bring up a browser-based editor with the contents of the file. The top section will look like this:
   
```yaml
# REQUIRED CHANGES
# Edit next line, providing your own name.
title: Molly Maluhia | Professional Portfolio
# Edit next line, replacing 'techfolios' with your github username
url: "https://techfolios.github.io"
# Edit next line so that baseurl is "" if your repo is <username>.github.io
baseurl: "/template"
```
     
Edit `title:` to include your own name, edit `url:` to point to your portfolio, and edit `baseurl:` to be the empty string. When you're done editing, that section of _config.yml should look similar to this:
  
```yaml
# REQUIRED CHANGES
# Edit next line, providing your own name.
title: MY NAME | Professional Portfolio
# Edit next line, replacing 'techfolios' with your github username
url: "https://USERNAME.github.io"
# Edit next line so that baseurl is "" if your repo is <username>.github.io
baseurl: ""
```  

Go to the bottom of the page and click "Commit changes" to save these changes.   

**G.** You're done!   If you now click on the link containing your portfolio URL on the summary line, you should see the following page:

<img style="" src="images/techfolio-personal-template.png" class="img-responsive">

Note how the url in this screen image includes a personal GitHub account name.

# 3. Configure home page

Here's a two minute video illustrating these steps:
{% include youtube.html id="DIbVvGHOhow" %}


<p style="text-align: center; padding-top: 10px">
  <a href="/userguide.html" class="btn btn-primary btn-md" role="button">Go to User Guide <span class="glyphicon glyphicon-chevron-right"></span> </a>
</p>

# 4. Configure projects page

# 5. Configure essays page

# 6. Configure resume page









