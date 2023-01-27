# **How to upload content to Github**



<br>

1. Copy the link of your repository, let’s say, https://github.com/Sagamore-Economics/assignment1   

<br>

2. In shell, cd into a directory you want to save the repo

    ```console
    cd "C:\Useuprs\winni\OneDrive\git"
    ```

<br>

3. Clone the repo:

    ```console
    git clone https://github.com/Sagamore-Economics/assignment1
    ```
    <br>

4. Now you created a folder within the directory called “assignment1”, cd into it. 

    ```console
    cd assignment1
    ```
<br>

5. Copy your exam files into this folder

<br>

6. Track the changes:


    ```console
    git add *
    ```
<br>

7. Commit the changes:

    ```console
    git commit -m "You must put a message here"
    ```
<br>

8. Push the changes up.

    ```console
    git push
    ```

<br>


### **Note: Everytime you make a change to files, you have to repeat steps 6-8. An easy way:**
<br>

    ```console
    git add * && git commit -m "You must put a message here" && git push
    ```