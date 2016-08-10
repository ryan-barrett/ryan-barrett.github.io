# Learn Git Lab

1. Create a fork of the [learn-git repository](https://github.com/sf-wdi-27-28/learn-git) by clicking "Fork" on the top right.

  ![screen-shot-2015-10-20-at-17 26 49](https://cloud.githubusercontent.com/assets/7833470/10625501/b15a2bee-7758-11e5-8b12-2c84b785801b.png)

2. You'll see a screen like this while GitHub is forking the repo. Forking creates a copy of the original repo on your own GitHub account.

  ![screen-shot-2015-10-20-at-17 21 15-1](https://cloud.githubusercontent.com/assets/7833470/10625502/b422f2e8-7758-11e5-8cf1-09ae4fd7d946.png)

3. Now you have your own copy of the repo! Copy the "clone URL" from the top.

  ![screen-shot-2015-10-20-at-17 22 43](https://cloud.githubusercontent.com/assets/3010270/13687431/17d1d2e6-e6d0-11e5-8a5f-9f1575f03aa9.png)

1. Make a `wdi` directory. This is where you will put all your work from this class.
  ```
  ➜ mkdir ~/wdi
  ```

4. Use the "clone URL" to clone the repo onto your local machine. Make sure you're in your `~/wdi` directory before you clone!

  ```zsh
  ➜  cd ~/wdi
  ➜  git clone <clone-url>
  ```

5. Change directories into the repo you just cloned (in this example, `learn-git`).

  ```zsh
  ➜  cd learn-git
  ```

6. Open this project in Atom.

  ```zsh
  atom .
  ```

1. Back in Atom, open `index.html`. In the `<body>` tags, create an `<h1>` tag with your name and add a gif of your liking in an `<img>` tag. "Copy Image Address" from [giphy.com](http://giphy.com/).

6. Now that you've changed the repo, it's time to commit your changes. Back in your terminal, type

  ```zsh
  ➜  git status
  ```
  This shows you the files that have been modified, created, or deleted. Notice that they are listed as `untracked`.

1. Now you're ready to `add` your changes. Type
  ```
  ➜  git add .
  ```
  Then `git status`. Notice that your new file has gone from `untracked` to `Changes to be committed`.

1. Next step is committing. Type

  ```
  ➜  git commit -m "modifying index.html"
  ```
  Then `git status`. Notice that the new status is `Your branch is ahead of 'origin/master' by 1 commit.`. This indicates that your the version of the repo on your computer (aka the __local__ version) includes your changes but the version hosted by GitHub (aka the __remote__ version) does not.

1. To get your changes on to the remote version of the repo, type

  ```
  ➜  git push origin master
  ```
  Now `git status` will tell you that `Your branch is up-to-date with 'origin/master'.` __!!!__

7. Once you're done with the assignment and have committed and pushed ALL of your changes to GitHub, it's time to make a pull request back to the original repo. Go to your forked copy of the repo on GitHub, and click the "Pull Request" button.

  ![screen-shot-2015-10-20-at-17 25 24](https://cloud.githubusercontent.com/assets/3010270/13687969/7ed9d38c-e6d3-11e5-9510-ac0fbf1f22e9.png)

8. GitHub takes you to a new view and asks if you want to create the pull request. Click the green button, and that's it - you've now created a pull request to submit this lab!

  ![screen-shot-2015-10-20-at-17 25 49](https://cloud.githubusercontent.com/assets/7833470/10625507/bc97d38a-7758-11e5-8fe9-e4846e06e454.png)

1. Repeat! Add some new content to your file and repeat this Git flow.
