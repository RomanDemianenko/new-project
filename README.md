# New Project Git Repository Setup

This README provides step-by-step instructions on how to set up a new Git repository for the 'new-project' and create a development branch where new features can be developed independently of the main branch.

## Setting Up a New Git Repository

Before starting, ensure that Git is installed on your system. If it's not, you can download and install it from [Git's official site](https://git-scm.com/downloads).

### Initializing the Repository

1. Open your terminal.
2. Navigate to the directory where you want to create your project:
```
cd path/to/your/directory
```
3. Initialize a new Git repository:
```
git init new-project
```
4. Move into the newly created `new-project` directory:
```
cd new-project
```
### Creating a README file
1. You can use two commands to create file and fill it
```
echo "Some initial content for the README" > README.md
```
or
```
cat init > README.md
```
2. Add the file to the staging area:
```
git add README.md
```
### Connecting to a Remote GitHub Repository

1. Create a new repository on GitHub named 'new-project'.
2. Link your local repository to the remote GitHub repository:
```
git remote add origin git@github.com:RomanDemianenko/new-project.git
```

## Creating the Development Branch

1. By default, you'll be on the `main` branch. To create a new branch named 'development':
```
git checkout -b development
```
2. You are now on the `development` branch.

### Updating the README.md File

1. Open the `README.md` file in a text editor and add appropriate content.:
```
nano README.md
```
2. Add the file to the staging area:
```
git add README.md
```
3. Commit your changes with a message:
```
git commit -m "Add README.md with instructions"
```

### Pushing Changes to GitHub

1. After committing your changes, push them to the `development` branch on GitHub:
```
git push -u origin development
```
## Merging Changes from 'development' to 'main'

Once you're ready to merge your development work into the `main` branch:

1. Switch back to the `main` branch:
```
git checkout main
```
2. Merge changes from `development` into `main`:
```
git merge development
```
3. Push the updated `main` branch to GitHub:
```
git push origin main
```

## Conclusion

You now have a `new-project` repository set up with a `main` branch for production releases and a `development` branch for ongoing work. Remember to keep your branches in sync and manage your merges according to your project's workflow.
