# ADCS-Git-Demo
Welcome to the ADCS git tutorial. Please follow the steps below to get set up, and follow along to learn how to make your changes show up in github.

## Setup
You will need to follow the following tutorials (if you have not done so already)

- [GitHub SSH Setup Tutorial](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) ***OR*** [GitHub HTTPS Cloning Information](https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls)
- [Download Git Bash](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

## Steps
Follow these steps to learn how to use git!
### Clone the Repo
The first step is getting a local copy of the repository.
1. Go to the top right of the page and click the big green "Code" button.
2. Select either "HTTPS" or "SSH" Depending on your preference.
3. Press the two squares on the right of the url to copy the repo URL
4. Open Git Bash in the folder you want to have the local copy (right click in the folder on windows and select "Git Bash Here")
5. In the Bash terminal, run `git clone <url you copied> <destination directory`. For example, `git clone https://git-scm.com/book/en/v2/Getting-Started-Installing-Git git_tutorial`.

### Local Branches
Congratulations! You've downloaded the repository. Now we need to learn how to use branches to make changes to the files.
1. In bash, enter the folder you created using the `cd` command. For example, `cd git_tutorial`.
2. Create a local branch: `git checkout -b <branch_name>`. This creates a version of the entire repository at the exact moment in time you created the branch, entirely local to your computer. This means that if someone makes changes to the original branch (master), your work won't be affected!

### Making changes
Now that we have a local branch, we can make changes to the repository.
1. Ccreate a new file called `your_name.txt` and fill it with a fun fact about yourself.
2. Save your file, and run `git status` in Bash. You should see your new file!

### Uploading changes to the server
Now that we have changes to make, we need to tell GitHub about them so everyone can see our changes.
1. Run `git add <file_name>` to tell git that you want to upload your new file. The file name actually matches "regular expression" patterns, so we can add mroe than one file at once. For example, we could add all .txt files with `git add *.txt`.
2. Run the command `git commit -s`. This will open up a weird and confusing text editor - but not to fear!
    1. Press `i` to edit in the text editor. Add a message about what your commit is, for example `added new file, aidan.txt`.
    2. Press `esc`, then `w`, then `q`. This saves the commit message file and quits the editor.
3. Now run the command `git log`. You should see your new commit at the top of the list!
4. If you run `git status` again, you'll see your changes are no longer there.
5. Now we need to push our changes to the server. Run `git push`. An error should pop up, copy and paste the suggested command and run it. (note that `ctrl+c` and `ctrl+v` do not usually work in Bash, try `shift+ins` and `ctrl+ins` instead)
6. Your commit should be sent to the server! You can now check in the GitHub website of the repo under the "branch" tab for the branch you created.

