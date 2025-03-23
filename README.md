This is an assignment for you to get familiar with SSH and Git, if you are not already. You can experiment with your own repository, and this assignment is not graded.
# Set up your SSH

- SSH stands for Secure SHell and is a communication protocol that encrypts communication between the client (you) and the server you want to connect to. It works using two encryption keys: a public key (shared with the server) and a private key (which you NEVER share). These keys are long, seemingly random numbers that are mathematically related. If a message is encrypted with one of the keys, it can be decrypted with the paired key, and vice versa.
- In your terminal/PowerShell, use `git config` to set your GitHub username and email:
    - `git config --global user.name "your_user_name"`  
    - `git config --global user.email "your_email@lehigh.edu"`  
    - `git config --global color.ui auto`
- Generate an SSH key using `ssh-keygen`:
    - Do **not** enter a passphrase when prompted. If you do, you will be asked for it every time you use SSH. The passphrase essentially becomes a password, and one of the benefits of SSH is avoiding that!
    - On Windows 10/11: <https://phoenixnap.com/kb/generate-ssh-key-windows-10>
    - On macOS/Linux: <https://www.digitalocean.com/community/tutorials/how-to-create-ssh-keys-with-openssh-on-macos-or-linux>
- Add your new SSH key to your GitHub account:  
  <https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account>
- After uploading your public SSH key to GitHub, you're ready to create a project repository or clone an existing one.

# Git

- Git is a powerful version control system widely used for tracking changes in source code during software development.
- Full tutorial: <https://github.com/git-guides>
- If you want to create a new repository on GitHub (i.e., you're not cloning from an existing one), navigate to the directory you want to use as the top level of your new project and run:
    - `git init`
- To clone an existing repository from GitHub (for most of our programing assignments):
    - Log in to your GitHub account.
    - Either create a repository or navigate to the one you want to clone.
    - For programming assignments, a repository has already been created for you under a classroom account on GitHub (classroom.github.com).
    - After accepting the assignment, you can access your own repository.
    - On the “Code” tab, click the green “<> Code” dropdown in the upper right. (If “SSH” is not selected, click on it.) Your repository’s clone URL will include your GitHub username.
    - Copy the SSH URL (e.g., `git@github.com:your_repo.git`).
    - Clone your repository by running the following in your terminal/PowerShell:
        - `git clone git@github.com:your_repo.git`
- Stage changes using `git add`, for example:
    - `git add your_file.py` or `git add .`
- Commit your changes:
    - After modifying files, use `git commit` to commit your changes. For example: `git commit your_file.py`
    - This will launch an editor where you can write a commit message describing your changes.
    - Running `git commit` saves the staged changes as a permanent snapshot in Git's history.
- Push your latest version to GitHub:
    - Use `git push` to send your committed changes to the remote repository.