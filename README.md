## Getting Started

To get a local copy up and running, follow these simple steps:

1. **Clone the repository**
   ```sh
   git clone https://github.com/username/CSD1103-Project.git
   ```
2. **Navigate to the project directory**
   ```sh
   cd stationery-studio
   ```
3. **Open the project in your preferred code editor**
4. **Start developing!**

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

### How to Contribute

If you have a suggestion that would make this project better, please follow the steps below to contribute. This guide will help even beginners get started.

#### Step 1: Fork the Repository

1. **Fork the Project**:
   - Go to the project's GitHub page.
   - Click on the "Fork" button at the top right of the page. This will create a copy of this repository in your GitHub account.

#### Step 2: Clone Your Fork

2. **Clone the Forked Repository**:
   - Open your terminal or command prompt.
   - Type the following command, replacing `yourusername` with your GitHub username:
     ```sh
     git clone https://github.com/yourusername/CSD1103-Project.git
     ```
   - Navigate to the cloned directory:
     ```sh
     cd stationery-studio
     ```

#### Step 3: Create a New Branch

3. **Create a New Branch**:
   - It's important to create a new branch for your changes to keep the `main` branch clean.
   - In your terminal, type:
     ```sh
     git checkout -b feature/AmazingFeature
     ```
   - Replace `AmazingFeature` with a name that describes your feature or fix.

#### Step 4: Make Your Changes

4. **Make Your Changes**:
   - Open the project in your preferred code editor.
   - Make the necessary changes or additions.

#### Step 5: Commit Your Changes

5. **Commit Your Changes**:
   - After making your changes, you need to commit them to your branch.
   - In your terminal, type:
     ```sh
     git add .
     ```
     This command stages all the changes you made.
   - Now commit the changes:
     ```sh
     git commit -m 'Add some AmazingFeature'
     ```
     Replace `'Add some AmazingFeature'` with a meaningful commit message that describes your changes.

#### Step 6: Push to GitHub

6. **Push to GitHub**:
   - Push your changes to your forked repository:
     ```sh
     git push origin feature/AmazingFeature
     ```

#### Step 7: Create a Pull Request

7. **Create a Pull Request**:
   - Go to the original repository on GitHub.
   - You should see a notification about your recently pushed branch and an option to create a pull request.
   - Click "Compare & pull request".
   - Provide a description of your changes and submit the pull request.

Your contributions are now ready to be reviewed. Thank you for helping improve the Stationery Studio project!

## Handling Updates from the Main Repository

Sometimes, the `main` branch of the original repository will be updated while you are working on your branch. Here’s how to keep your local branch up-to-date:

1. **Add the Original Repository as a Remote**
   - First, add the original repository as a remote. This is usually named `upstream`.
     ```sh
     git remote add upstream https://github.com/username/CSD1103-Project.git
     ```

2. **Fetch the Latest Changes**
   - Fetch the latest changes from the original repository:
     ```sh
     git fetch upstream
     ```

3. **Merge the Latest Changes**
   - Switch to your `main` branch:
     ```sh
     git checkout main
     ```
   - Merge the changes from `upstream/main` into your local `main` branch:
     ```sh
     git merge upstream/main
     ```

4. **Rebase Your Feature Branch**
   - Switch back to your feature branch:
     ```sh
     git checkout feature/AmazingFeature
     ```
   - Rebase your branch with the updated `main`:
     ```sh
     git rebase main
     ```

5. **Resolve Conflicts (if any)**
   - If there are any merge conflicts, resolve them manually. After resolving conflicts, continue the rebase process:
     ```sh
     git rebase --continue
     ```

6. **Push Your Updated Feature Branch**
   - After rebasing, you need to force push your feature branch to update it on GitHub:
     ```sh
     git push --force origin feature/AmazingFeature
     ```

## Additional Git Commands and Troubleshooting

### Common Commands

- **Check the Status**
  - To check the status of your working directory and staging area:
    ```sh
    git status
    ```

- **View Commit History**
  - To view the commit history:
    ```sh
    git log
    ```

- **Discard Changes**
  - To discard changes in your working directory:
    ```sh
    git checkout -- <file>
    ```

- **Delete a Branch**
  - To delete a local branch:
    ```sh
    git branch -d feature/AmazingFeature
    ```
  - To delete a remote branch:
    ```sh
    git push origin --delete feature/AmazingFeature
    ```

### Troubleshooting

- **Error: 'Updates were rejected because the remote contains work that you do not have locally.'**
  - This happens when the remote branch has new commits that you don’t have. To resolve this, first, pull the latest changes:
    ```sh
    git pull origin main
    ```
    Then resolve any conflicts that arise and commit the changes.

- **Error: 'You have uncommitted changes.'**
  - You need to either commit your changes or stash them before switching branches. To stash changes:
    ```sh
    git stash
    ```
    After switching branches, you can apply the stash:
    ```sh
    git stash apply
    ```

- **Error: 'Merge conflicts'**
  - Conflicts occur when Git cannot automatically merge changes. Open the conflicted files and manually resolve the conflicts. After resolving, add the resolved files:
    ```sh
    git add <file>
    ```
    Then continue the merge or rebase process:
    ```sh
    git commit -m 'Resolved merge conflicts'
    ```

---

Happy coding! 🚀
