 | [git CLI cheatsheet](https://github.com/getfutureproof/fp_guides_wiki/wiki/git-CLI-Cheatsheet) |

:wave: **If it's your first time here, welcome!** :partying_face: Start at the top with **Getting Started** and work through the steps before moving onto 'Making Changes' and then 'Submitting Your Changes'.

:student: If you're already on the roster and are now coming back to add your additional materials, you can skip straight to **Making Changes**.

:technologist: If you're in LAP 3 or beyond, get outta here you don't need instructions, you know how to do this stuff in your sleep now!

:bulb: *Click the dropdown arrows below for step-by-step instructions*

:rotating_light: ***NB: The data in this repository is used on [your showcase site](https://cohorts.getfutureproof.co.uk/), so make sure the data you're adding is correct and consistent!*** :rotating_light:

<details>
<summary>
<strong>Getting Started</strong>:
Fork, Clone & Connect
</summary>
    
:fork_and_knife: **Fork** \
Forking is how you'll get your own copy of this code to work on

  - Hit 'Fork' on this central repository (it's in the top right!)
  - You'll know if you are looking at your fork if you see `<your-github-username>/fp_study_notes_hello_github` at the top of the page
  - If it says `getfutureproof/fp_study_notes_hello_github`, you're looking at the central repository instead
  
:inbox_tray: **Clone** \
Editing in the browser is not impossible, but it's not much fun either. Let's make use of that local development environment you've set up! Cloning will download a copy of your fork for you to work on outside of GitHub.

  - On **your fork**, click the green 'Code' button
  - Copy the URL shown
    - You can use either SSH or HTTPS option *(if you choose SSH, you'll need to have [setup your SSH key](https://github.com/getfutureproof/fp_guides_wiki/wiki/MacOS-Setup#setup-an-ssh-key-and-add-it-to-your-github-account))*
  - Clone down your fork using `git clone <what-you-copied> hello-github` in your terminal
    - eg. `git clone https://github.com/VariantL1130/fp_study_notes_hello_github.git hello-github` 
    - This will create a folder called `hello-github` containing all the files in this repo
    - Run `ls` in your terminal to check the new folder is there!
    - Run `cd hello-github` to **c**hange **d**irectory into the project folder
    
:link: **Connect** \
As you continue through the course, you will keep adding to this roster, and so will all your colleagues. That's a lot of changes and as changes are made, we need to make sure no content is overwritten! The easiest way to do this is to check that your fork has the latest updates before you make new changes. Before we can do that, we need to form a connection between your fork and our central getfutureproof version. Each location we are connected to is called a `remote`.


When you first clone down your repo, it will only have a remote connection to your fork on GitHub at first.
To see your existing remote:
  - Make sure you are in the project folder
  - Run `git remote -v` in your terminal. You should see something like this:
```
origin  git@github.com:<your-github-username>/fp_study_notes_hello_github.git (fetch)
origin  git@github.com:<your-github-username>/fp_study_notes_hello_github.git (push) 
```

Let's add another, remote connection, this time to the getfutureproof version of this repo Github

  - Run `git remote add upstream https://github.com/getfutureproof/fp_study_notes_hello_github.git`
  - Run `git remote -v` again and you should see something like this:
```
origin  git@github.com:<your-github-username>/fp_study_notes_hello_github.git (fetch)
origin  git@github.com:<your-github-username>/fp_study_notes_hello_github.git (push) 
upstream  git@github.com:getfutureproof/fp_study_notes_hello_github.git (fetch)
upstream  git@github.com:getfutureproof/fp_study_notes_hello_github.git (push) 
```
  
</details>

<details>
<summary><strong>Making Changes</strong>: Locate, Sync, Edit, Stage, Commit
</summary>

:compass: **Locate** \
Whenever you are setting to work on a project, make sure you are in the project's folder!

  - Navigate into the project folder if you're not already there
    - Run `pwd` and you should see something like `<some>/<folders>/<on>/<your>/<machine>/hello_github`
    - Run `ls` and you should see all the cohort names and a few other names including `README.md`, and `package.json`
  - Open up the code in a text editor
    - if you have setup VS Code and its [shell commands](https://code.visualstudio.com/docs/setup/mac#_launching-from-the-command-line), you can do this from the command line using `code .`

:last_quarter_moon: **Sync** \
Thanks to the remote connection you made to the central repo in Getting Started, you can now can always get the most up-to-date version of the our main branch.
  - Run `git pull upstream master`

:exclamation: We strongly recommend that you do this each time you make changes during the course. It can really cut down on **merge conflicts** which are not quite as bad as they sound but still nice to avoid where possible!

:pencil: **Edit**
  - Find your cohort's `roster.json` file
  - Make your changes!
  - If it's your first time here, we just need your name and github username
    - In the `students` array, add a new [JSON](https://www.w3schools.com/whatis/whatis_json.asp) object
    - The object will have two key value pairs **_See example below and in other cohorts' rosters._**
      - One has a key of "name" and string value of your name
      - Another has a key of "github" and string value of your GitHub username
    - Save the file (Windows/Linux: <key>ctrl</key>+<key>s</key> / MacOS: <key>command</key>+<key>s</key>). 

```json
  {
    "name": "Loki Laufeyson",
    "github": "VariantL1130"
  }
```

:european_castle: **Stage** \
Staging is when we tell git which changes we will want to track
  - After making changes, check the git status of the project with `git status`
    - `<your-cohort>/roster.json` should show in red as there are unstaged changes
  - Stage your change with `git add .` (or `git add <your-cohort>/roster.json`)
  - Check the git status again
    - `<your-cohort>/roster.json` should now show in **green** as the changes have been staged but not yet committed

:heavy_check_mark: **Commit** \
Commiting is when we tell git that it is time to make a note of the current state of the code, giving it a unique ID. As you continue coding, commit often - don't wait until you've finished an entire feature! These ID-tagged commits allow us see our code bases' history, really helpful for those times of *"hm, this was working earlier... now, what did I do..."*

:exclamation: Only the changes that are `green` when running `git status` will be committed
  - Commit your change with `git commit -m "add <your-name>"` eg. `git commit -m 'add Loki Laufeyson`.
  - :exclamation: The `-m` is a flag for 'message' and you must leave a message with every commit!
  - Check the status again - there should be nothing to commit now but an indicator that your local version is one commit ahead of the origin.
    
</details>



<details>
<summary>
<strong>Submit your changes</strong>: Push & PR
</summary>
    
:outbox_tray: **Push**
The push is when your latest changes will be sent back up to **your own fork** on GitHub
  - Use `git push` to push up your changes to your fork's `main` branch

:handshake: **Make your first PR** \
Last step is to submit your changes to be added into our version - which is the one that powers [your showcase site](https://cohorts.getfutureproof.co.uk/), so make sure the data you're adding is correct!
  - Use the GitHub browser interface to see if you can make a Pull Request back to `getfutureproof/fp_study_notes_hello_github`
  - We will review your PR when we receive it *(please allow up to 2 working days)*
    - If it all looks good, we will merge! Job done!
    - If there are any changes to be made, we will reply on the PR letting you know what we need
    - If we request changes:
      - Do not close the PR!
      - Make you changes using the edit, stage, commit steps above
      - When you push again, your existing PR will be updated automatically and we will re-review :smile_cat:

    
</details>


