# Learn Git Training

1. Create a fork of the [this](https://github.com/sf-wdi-LABS/personal-portfolio) by clicking "Fork" on the top right.

  ![fork button](https://cloud.githubusercontent.com/assets/6520345/17564556/97ecdd00-5ee8-11e6-9ad0-a7b8104579ff.png)

2. You'll see a screen like the one below while GitHub is forking the repo. Forking creates a copy of the original repo on your own GitHub account. The forked repo is still online only and not on your computer.

  ![forking](https://cloud.githubusercontent.com/assets/6520345/17570801/c0d27e36-5f02-11e6-8d44-f485301831ed.png)

3. Now you have your own copy of the repo! In order to make this a live personal website, we're going to take advantage of GitHub's [*GitHub pages*](https://pages.github.com/) feature. All we need to do is change the repository name to `<fill in your GitHub username>.github.io`. Here's how:
  * Click on the settings tab toward the top of the page: ![settings tab](https://cloud.githubusercontent.com/assets/6520345/17564907/fc20986a-5ee9-11e6-8e7f-abc19c482a7b.png)
  * Find the repository name section and change it to `<username>.github.io` ![change repo name](https://cloud.githubusercontent.com/assets/6520345/17564950/2a69081a-5eea-11e6-8d17-8017954d8ad7.png)
  * Click the rename button.

4. Go to the website `<username>.github.io`!  You have a web presence now!! It's not perfect, but it will be a work in progress over the whole course and it's an excellent start! If you want to change the content, you're going to need a copy on your own computer to edit and improve.

4. Click the clone or download button and copy the "clone URL."

  ![clone button](https://cloud.githubusercontent.com/assets/6520345/17565250/87ec41b8-5eeb-11e6-8fc8-280aa6e14611.png)

  ![clone url](https://cloud.githubusercontent.com/assets/6520345/17565297/bc8e85ca-5eeb-11e6-870d-3029f9f7ed5b.png)

1. On your own computer, make a `wdi` directory in your home folder (`~`). This is where you will put all your work from this class. You can complete this in one command:
  ```
  ➜ mkdir ~/wdi
  ```

4. Use the "clone URL" to clone the repo onto your local machine. Make sure you're in your `~/wdi` directory before you clone!

  ```zsh
  ➜  cd ~/wdi
  ➜  git clone <clone-url>
  ```

5. Change directories into the repo you just cloned (in this example, `<username>.github.io`).

  ```zsh
  ➜  cd <username>.github.io
  ```

6. Open this project in Atom.

  ```zsh
  atom .
  ```

1. Back in Atom, open `index.html`. Take a moment to read through index.html and answer these questions for yourself:
  *
  <details>
    <summary>How many stylesheets does this webpage currently have? Where in the project can they be found and edited?</summary>
    <p>There are two stylesheets, `normalize.css` and `main.css`. `normalize.css` is in the `vendor/css` folder because it's a file developed by somebody else (a vendor) and you won't be editing it. `main.css` is in the `assets/css` folder and is the custom styling that you'll spend time adjusting.</p>
  </details>
  *  
  <details>
    <summary>In the `<head>` element, change the `<title>` of the page. Where can you observe the impact of this change?</summary>
    <p>On the tab in the browser, your site will display a new name. It used to be "First Training."</p>
  </details>
  *
  <details>
    <summary>If you were to write some Javascript to handle events on this page, what file would be the correct place to write that code?</summary>
    <p>You'd want to write your custom JS in the `assets/js/app.js` file. Once this file grows big enough you might want to create new JS files in the `assets/js` folder.</p>
  </details>

1. In the `<body>` of the document, replace the `<h1>` tag text with your name and add an image (or gif) of your liking using the `<img>` tag.

6. Now that you've changed the repo, it's time to commit your changes. Back in your terminal, type

  ```zsh
  ➜  git status
  ```
  This shows you the files that have been modified, created, or deleted. Notice that they are listed as `untracked`.

1. Now you're ready to `add` your changes. Type
  ```
  ➜  git add .
  ```
  Now enter `git status`. Notice that your new file has gone from `untracked` to `Changes to be committed`.

1. Next step is committing. Type the following:

  ```
  ➜  git commit -m "first edits to index.html"
  ```
  Now enter `git status` again. Notice that the new status is `Your branch is ahead of 'origin/master' by 1 commit.`. This indicates that your the version of the repo on your computer (aka the __local__ version) includes your changes but the version hosted by GitHub (aka the __remote__ version) does not.

1. To get your changes on to the remote version of the repo, type

  ```
  ➜  git push origin master
  ```
>***Note:*** *`origin` is the given name of the remote repository hosted on GitHub. `master` is the name of the main branch within the repository. (Typically `master` is the branch you update when you're ready to publish changes to the world.)*

  Now `git status` will tell you that `Your branch is up-to-date with 'origin/master'.` __!!!__

2. Check back in on your site to see the improvements deployed!

1. Repeat steps 11 onward at least three times to improve your site and practice this Git workflow.

# Deliverables

On Friday, we will be having a feedback session on your progress on the personal portfolio project. By then we expect to see:

* An updated README.md file. A readme is like the cover to the book of code you've written for this site. Don't publish a book without a cover! Describe this project in a few sentences - what are you trying to achieve with this page, what technologies are you using, etc. [This is a decent template](https://gist.github.com/zenorocha/4526327) for the way that a readme often looks. Make sure to link to the live site and include some sort of image (logo or screenshot). If you need help writing markdown language (the reason the file ends in `.md`), check out [this guide](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).
* A "My work" section of the page that includes (or will include) links to all repos that contain homework deliverables.
* A "Contact me" section of the page that includes (at least) a way to email you, a link to your GitHub profile, and a link to your LinkedIn profile.
* Some custom HTML, CSS, JS, and images. Put your own personal flare on the page and add some customizations. These could be really simple changes that add a bit of your aesthetic or they could be larger features like a navbar, a footer, a photo carousel, bootstrap integration, event listeners, or CSS animations. [Google for personal websites](https://www.google.com/search?q=personal+website&espv=2&biw=1280&bih=612&site=webhp&tbm=isch&tbo=u&source=univ&sa=X&ved=0ahUKEwjx-Krl6bfOAhUUI2MKHaoPDUEQsAQIQA&dpr=2#imgrc=OOkEvdqZczSU-M%3A), find one that you like, and imitate it!

We're really looking forward to seeing what you've built by Friday! Please reach out to your peers or instructors if you need help making progress on this project.
