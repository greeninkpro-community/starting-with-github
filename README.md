# starting-with-github
To complete the assignment, here's a step-by-step guide:

1. **Check if Git is installed:**
   - Open your terminal and type `git --version`. If it returns a git version, then Git is installed. If not, download and install Git from [here](https://git-scm.com/downloads).

2. **Configuring Git:**
   - Set up your global config values using the following commands, replacing the placeholders with your information:
     ```
     git config --global user.name "Your Name"
     git config --global user.email "email@something.com"
     ```

3. **Create a GitHub account:**
   - Go to [GitHub](https://github.com/) and sign up if you haven't already.

4. **Setting up SSH keys:**
   - Open your terminal and navigate to your home directory (`cd ~`).
   - Check if the `.ssh` directory exists by typing `ls -a`. If it doesn't exist, create it with `mkdir ~/.ssh`.
   - Generate an SSH key pair using the command:
     ```
     ssh-keygen -t ed25519 -C "your_email@example.com"
     ```
     Press Enter for the file to save the key, and optionally set a passphrase.
   - Start the SSH agent with:
     ```
     eval "$(ssh-agent -s)"
     ```
   - Add your SSH key to the SSH agent:
     ```
     ssh-add ~/.ssh/id_ed25519
     ```

5. **Adding SSH key to your GitHub account:**
   - Follow the steps [here](https://docs.github.com/en/enterprise-server@3.1/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) to add your SSH public key to your GitHub account.

6. **Cloning the repository:**
   - Fork the repository [Github-Enablment-Task](https://github.com/gtech-mulearn/Github-Enablment-Task) to your GitHub account.
   - Clone the forked repository to your local machine using either SSH or HTTPS option. For SSH, use `git clone git@github.com:yourusername/Github-Enablment-Task.git` and for HTTPS, use `git clone https://github.com/yourusername/Github-Enablment-Task.git`.

7. **Working on the assignment:**
   - Change directory into the cloned repository folder (`cd Github-Enablment-Task`).
   - Create a new branch called `develop` with `git checkout -b develop`.
   - Create a directory with your full name inside the root of the app (e.g., `bijoy_sijo_book_app`) and change directory into it.
   - Create another directory inside your book app directory called `add_books_feature`.
   - Inside the `add_books_feature` directory, create two text files: `create_book.txt` and `list_all_books.txt`, and add the specified texts into them.
   - Stage and commit your changes.

8. **Managing branches and commits:**
   - If you mistakenly staged the `list_all_books.txt`, you can unstage it with `git reset HEAD list_all_books.txt`.
   - Checkout to the `main` branch (`git checkout main`), then create a new branch called `feature` (`git checkout -b feature`).
   - Make the specified changes to `list_all_books.txt` and commit them.
   - Check the log to see the changes you've made so far (`git log`).
   - Commit your changes.

9. **Pushing changes and raising a Pull Request:**
   - Push your changes to your forked repository (`git push origin feature`).
   - Once pushed, navigate to your forked repository on GitHub.
   - Open a Pull Request from your `develop` branch to the main branch of the original repository.
   - Give your Pull Request a meaningful title and description, then submit it.

10. **Merging changes:**
    - Once your Pull Request is reviewed and approved, you can merge the changes into the main branch of the original repository.

Congratulations! You've completed the basic Git & GitHub workflow assignment.
