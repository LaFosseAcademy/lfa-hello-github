### Study Notes
[git CLI cheatsheet](https://github.com/getfutureproof/fp_guides_wiki/wiki/git-CLI-Cheatsheet)

# Exercises
**Fork & Clone**
- Hit 'Fork' on this repo (it's in the top right!)
- On your fork (it will say `<your-github-username>/fp_study_notes_hello_github` at the top of the page), click the green 'Code' button and copy the SSH option if you have already setup git in your terminal, or the HTTPS option if not.
- Clone down your fork using `git clone <what you copied>` in your terminal
  
**Make a Change**
- Move into the project folder with `cd fp_study_notes_hello_github`
- Open it up in a text editor (if you have setup VS Code, you can do this from the command line using `code .`)
- Make a change! In the `students` array, add a new JSON object with a key of "name" and value of your name to `<your-cohort>/roster.json` and save the file (Windows/Linux: <key>ctrl</key>+<key>s</key> / MacOS: <key>command</key>+<key>s</key>)
- Check the git status of the project with `git status` - `<your-cohort>/roster.json` should show in red as there are unstaged changes

**Stage your Change**
- Stage your change with `git add .` (or `git add <your-cohort>/roster.json`)
- Check the status again - `<your-cohort>/roster.json` should now show in green as the changes have been staged but not yet committed
  
**Commit your Change**
- Commit your change with `git commit -m "add <your-name>"`. The `-m` is a flag for 'message' and you must leave a message with every commit!
- Check the status again - there should be nothing to commit now but an indicator that your local version is one commit ahead of the origin. As it suggests, use `git push` to push up your work to GitHub!

**Make your first PR**
- You made your own fork of this, now use the GitHub browser interface to see if you can make a Pull Request back to `getfutureproof/fp_study_notes_hello_github`. Try and request review from @getfutureproof-admin. We will merge your PR when we receive it!
