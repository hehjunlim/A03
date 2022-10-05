# A03
Tutorial on how to use Github and Definitions

How to Set Up Git, Webstorm, and Github on a Mac-
1. Install Webstorm from this [link](https://www.jetbrains.com/community/education/#students)
2. Create a Github account on this [website](https://github.com/)
3. Download Git from this link in Terminal utilizing [Homebrew](https://git-scm.com/download/mac)
4. When copy and pasting in quotations, please copy without the quotations. 
5. Now it is time to connect your machine with a Github account through an SSH key. 
6. Open Terminal and type this in "ssh-keygen -t rsa -b 4096 -C "<your email address>". The email address you put in should be the email address that you used to make your account on Github.com. 
7. A new SSH key will automatically be created. 
8. Next, you will be prompted to enter a directory to save the key. Press Enter to accept the default location, which is a .ssh folder in the home directory. 
9. Press Enter and Enter again to confirm the empty passphrase.
10. Run the following in Terminal, "cd ~/.ssh" and then "ls". 
11. Find “id_rsa” and “id_rsa.pub” in the list of contents. “id_rsa” is the private version of your key and “id_rsa.pub” is the public version of your key. 
12. run the following in Terminal: " eval "$(ssh-agent -s)" "
13. Check if .ssh directory contains a file named config. If it does, make the following its contents:
Host *
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/id_rsa
If your .ssh subdirectory does not contain a file named config, then create one and name it config (with no extension), and paste the above as its content. 
14. Add the key to the agent by pasting this into Terminal: ssh-add -K ~/.ssh/id_rsa
15. Run the following in Terminal to copy the public version of your key to the clipboard: pbcopy < ~/.ssh/id_rsa.pub
16. Go to Github account, and click your profile pic in the top right corner of your Github account and select “Settings” from the drop-down menu. 
17  Under Personal Settings, select ' SSH and GPG Keys ' . 
18. click the button "new SSH key".
19. For the title, give the key a name that describes the machine associated with it. (Example, "Personal Computer")
20. In the Key field, and press Command-v to paste the key from the clipboard buffer. The pasted key should have your email address at the end. 
21. Create a new Respitory by clicking "Create a New Repository" on the homepage of account. 
22. Please create a name for Respitory and make it public and check the box that states "Initialize this repository with README file". 
23. To create a local version of the repository, click the green drop-down button titled "Code" and copy the URL in the "SSH" option. 
24. On Terminal, and go to the directory where you want the local version of the repository. For example, you can create a directory called “projects”, that houses all the projects that you plan to work on. To do that, run the following in Terminal: mkdir ~/Desktop/projects
25. Run this in terminal to navigate to this directory: cd ~/Desktop/projects
26. Paste "git clone <repository_URL>" into the terminal by typing the keys Command + V. Replace <repository_URL> with the repository URL that you copied earlier. 
27. If you get prompted about the authenticity of the host and whether you want to continue connecting, answer yes.
28. Run the following in Terminal: ls
29. In order to push the changes to the remote repository from the changes made in Github.com, please put following into Terminal: git push 
                                                                                                               
Glossary:

**Branch**
>A tool that allows you to allow you to develop features, fix bugs, or safely experiment with new ideas in a contained area of your repository.

**Clone**
>Copying the respitory from Github.com to your local machine. 

**Commit**
>An individual change to a file (or set of files). 

**Fetch**
>Adding changes from the remote repository to your local working branch without committing them. 

**GIT**
>An open source program for tracking changes in text files. 

**Github**
>An Internet hosting service for software development and version control using Git. 

**Merge**
>Taking the changes from one branch (in the same repository or from a fork), and applies them into another.

**Merge Conflict**
>A difference that occurs between merged branches. They happen when people make different changes to the same line of the same file, or when one person edits a file and another person deletes the same file. 

**Push**
>Sending your committed changes to a remote repository on GitHub.com. For instance, if you change something locally, you can push those changes so that others may access them.

**Pull**
>When changes are fetched and merged. 

**Remote**
>The version of a repository or branch that is hosted on a server, most likely GitHub.com. Remote versions can be connected to local clones so that changes can be synced.

**Repository**
> The most basic element of GitHub. They contains all of the project files (including documentation), and stores each file's revision history. Repositories can have multiple collaborators and can be either public or private.


Works Cited: 
