# **Setting up Github**

### **Register a github account using your <ins>pace email</ins>**
### **Initial Git set up: You only need to do this once**

<br>

```console
git config --global user.name your_github_username	
```
<br>

```console		
git config --global user.email your_github_email
```
<br>

**mac users**: if you run into an **`xcrun`** error: invalid active developer path, check [<ins>this solution</ins>](https://apple.stackexchange.com/questions/254380/why-am-i-getting-an-invalid-active-developer-path-when-attempting-to-use-git-a): 


```bat
xcode-select --install
```

<br>

### **Forking the main repository (only need to do this once)**

<br>

When you fork, you create a copy of the main repository as your own repository in your space. 

<br>

1. Go to the main repository, **test**, created by owner **artichokew**: https://github.com/artichokew/test

<br>

2. On the top right corner, click the button **Fork**

<br>

3. On the forking page, make sure the following:

    - [x] The Owner is yourself (your github id).
    - [x] You put a description indicating this repo is a forked from owner: artichokew. This is optional but best practice. 
    - [x] Check “copy the main branch only”

<br>

4. Click the green botton **Create Fork**. Note that in your forked repo, the url has changed from **artichokew/test** to **winnieywl/test**. This means this repo has been copied to your github page. 

<br>

###  **Connecting (Cloning) to your Fork Repository (only need to do this once per repo** 

<br>

1. In your shell/terminal, change into the folder you want to save the cloned repository folder. 

    ```bat
    cd "C:\Users\winni\OneDrive\git"
    ```

<br>

2. Clone your forked repository

    ```console
    git clone https://github.com/winnieywl/test
    ```
<br>

This step will create a folder under **C:\Users\winni\OneDrive\git**, with the name of the repository as its name, **test**.       


This step also downloads ALL content posted in the github repository, **test**, to the folder, **test** under **C:\Users\winni\OneDrive\git**     

<br>

### **Downloading the latest content from the upstream repo**
Professors may make changes to their course materials. Those changes will not auto-update in your forked repo. To make sure you have the latest version of the course content, do the following in your shell/terminal:

1. In your shell/terminal, change into the repository folder on your pc. Hit enter.

    ```bat
    cd "C:\Users\winni\OneDrive\git\test"
    ```

<br>

2. Connect to the main repository, **test**, by **artichokew**

    ```console
    git remote add upstream https://github.com/artichokew/test.git
    ```

<br>

3. Pull the latest change from the upstream repo by **artichokew**

    ```bat
    git fetch upstream 
    ```

<br>

4. Sync with the upstream repo

    ```console
    git merge upstream/main
    ```

<br>

### **Submitting an Assignment and Create a Pull Request**

Let’s say, you are asked to submit your Stata script in a folder called "midterm"

1. You want to make sure you have the latest version of **test** from artichokew. Repeat **steps 1, 3 and 4** from section **Downloading the latest content from the upstream repo**

<br>

2. Check your forked repository folder and see that **midterm** folder is there. 

<br>

3. Copy and paste the latest version of your work into **midterm**, give it a unique name like **Winnie_Liu_385_midterm**!

<br>

4. Update the forked repo on your github page. 

    ```console
    git add *
    ```
<br>

5. Commit changes

    ```console
    git commit -m "You must put a comment here, like Winnie Liu Midterm"
    ```
<br>

6. Push your change onto github

    ```bat
    git push
    ```
<br>

###  **<ins> Mac Users Stop here </ins>: You only need to do this step once. Windows users please ignore this and go to step 7. You will see an output asking you for username and password. Type in your username, but instead of password, get a personal access token here: https://github.com/settings/tokens)**       
         
<br>         

Check all scopes and click “generate token” all the way at the bottom. 

Copy the token in the green area and paste into your terminal as your password. Note: you will not see what you pasted there, so be careful and only paste it once. 

<br>

7. In your forked repo on github, you should see the changes you made.

<br>
<br>

## **References**:

[**Creating a pull request through forked repo**](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork)

[**About pull requests**](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)

[**Forking a repo**](https://docs.github.com/en/get-started/quickstart/fork-a-repo)
