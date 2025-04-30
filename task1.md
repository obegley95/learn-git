# Task 1

1. Install Git and generate SSH keys

    ```bash
    ssh-keygen -t rsa -C "<your_email@example.com>"
    ```

    It generates: ~/.ssh/id_rsa (private) and ~/.ssh/id_rsa.pub (public).
    Copy public key to clipboard:

    ```bash
    cat ~/.ssh/id_ed25519.pub
    ```

    Then:

    Go to <https://github.com/settings/keys>
    Click New SSH key
    Paste the contents of your public key
    Save it

2. Set user.name and user.email in Git

    ```bash
    git config --global user.name "Your Name"
    git config --global user.email "<your_email@example.com>"
    ```

    Check it:

    ```bash
    git config --global --list
    ```

3. Create and Clone a New GitHub Repository On GitHub:

    Go to <https://github.com/new>
    Create a repo, e.g., my-song
    Do not initialise with README or .gitignore
    Clone it locally via SSH:

    ```bash
    git clone <git@github.com>:your-username/my-song.git
    cd my-song
    ```

4. Create song.txt with half your favorite song

    ```bash
    nano song.txt # Or use your editor to paste the first half of the lyrics
    ```

5. Commit and Push

    ```bash
    git add song.txt
    git commit -m "add first half of my favorite song"
    git push origin main
    ```

6. Verify the file on GitHub

    Go to your GitHub repo page: <https://github.com/your-username/my-song>
    Confirm song.txt is there with the lyrics.

7. Use GitHub Web UI to Add Second Half

    On the GitHub repo page, click song.txt.
    Click the edit icon.
    Add the second half of the lyrics.
    At the bottom, enter commit message: finish my song.
    Commit the change.

8. Pull the Change to Local Repo

    ```bash
    git pull origin main
    ```

    Now verify:

    ```bash
    cat song.txt
    ```
