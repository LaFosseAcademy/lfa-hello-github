### Study Notes

[git CLI cheatsheet](https://github.com/getfutureproof/fp_guides_wiki/wiki/git-CLI-Cheatsheet)

# Instructions
🥳 **Are you coming here for the first time?** \
_Welcome! Follow the [Exercises](#exercises) below!_

👋 **Are you returning here to add or change something in your roster?** \
_Head on down to [Returners](#returners) for tips on how to make this smooth for you and us!_

# Exercises

### 1. Fork & Clone

- Hit 'Fork' on this repo (it's in the top right!)
- Make sure you are now looking at **your fork** (it will say `<your-github-username>/fp_study_notes_hello_github` at the top of the page)
- Click the green 'Code' button and copy the SSH option if you have already setup git in your terminal, or the HTTPS option if not.
- Clone down **your fork** using `git clone <what you copied>` in your terminal
- Move into the project folder with `cd fp_study_notes_hello_github`

### 2. futureproof your fork
_Okay, bad pun but it's true! Throughout the course we will be asking you to contribute to this repo again, so we want to make sure you can always get the latest version to work on_

- Add us as a remote with `git remote add upstream https://github.com/getfutureproof/fp_study_notes_hello_github.git`
- Check that all is well so far by running `git remote -v` - You should see something similar to the following:

```
origin	  https://github.com/<your-github-username>/fp_study_notes_hello_github.git (fetch)
origin	  https://github.com/<your-github-username>/fp_study_notes_hello_github.git (push)
upstream	https://github.com/getfutureproof/fp_study_notes_hello_github.git (fetch)
upstream	https://github.com/getfutureproof/fp_study_notes_hello_github.git (push)
```

### 3. Make a Change
NB: If you have left it a while since doing that fork, clone and adding the upstream remote please sync your repo to our before continuing by running: \
`git pull upstream main`

- Open it up in a text editor (if you have setup VS Code, you can do this from the command line using `code .`)
- Make a change! In the `students` array, add a new JSON object with a key of "name" and string value of your name and another key of "github" and string value of your GitHub username to `<your-cohort>/roster.json` and save the file (Windows/Linux: <key>ctrl</key>+<key>s</key> / MacOS: <key>command</key>+<key>s</key>). **_See example below and in other cohorts' rosters._**
- Check the git status of the project with `git status` - `<your-cohort>/roster.json` should show in red as there are unstaged changes

```json
{
  "name": "Loki Laufeyson",
  "github": "VariantL1130"
}
```

### 4. Stage your Change

- Stage your change with `git add .` (or `git add <your-cohort>/roster.json`)
- Check the status again - `<your-cohort>/roster.json` should now show in green as the changes have been staged but not yet committed

### 5. Commit your Change

- Commit your change with `git commit -m "add <your-name>"`. The `-m` is a flag for 'message' and you must leave a message with every commit!

### 6. Push your Change 

- Check your `git status` again - there should be nothing to commit now but an indicator that your local version is one commit ahead of the origin
- As it suggests, use `git push` to push up your work to GitHub!

### 6. Make your first PR

- You made your own fork of this, now use the GitHub browser interface to see if you can make a Pull Request back to `getfutureproof/fp_study_notes_hello_github`. Try and request review from @getfutureproof-admin. We will merge your PR when we receive it!


---

# Returners

### 1. Sync your repo
- Locate your local repo for this project (clone down your fork again if you deleted it before for any reason) and `cd` into the folder
- Run `git remote -v` and make sure your output is similar to that in [Step 2](#2-futureproof-your-fork) above
- Run `git pull upstream main` to get the latest updates from our central version of the repo

### 2. Make, Stage, Commit, Push your changes, and open a PR
- You know how to do this now! If you'd like a recap, check out steps 3,4,5,6 above.
