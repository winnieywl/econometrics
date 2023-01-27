# **Creating an assignment on github classroom**

1. Go to organization [**Sagamore-Economics**](https://github.com/orgs/Sagamore-Economics/repositories), click the green button "New Repository"

2. Fill out sections: repo name should have no space, choose **Private**, check **`Add a README file`**, click **`create repository`** at the bottom. 

3. On the repo page, click **`Settings`**

4. On top of the page, you must check **`Template Repository`**

5. Push changes to the template repo (exam, exam instructions, etc)

6. Visit [**Github Classrooms - Class ECO 385**](https://classroom.github.com/classrooms/123283353-eco-385), Click the green button **`New Assignment`**

7. Set **assignment** title, a **deadline**, set **visibility** to be **private**, **grant student admin access**, click **`Continue`**

8. Add the template you just created by searching **Sagamore-Economics/assignment_name**. Leave **Add a supported editor** blank. Click **`Continue`**

9. Leave **`Grading and feedback blank`**, click **`Create Assignment`**

10. Copy the invitation link and send it to students. Until you send them the link, they will NOT be able to view this assignment at all. 

<br>

# **How to collect submission**

1. Go to [**eco 385 assignments here**](https://classroom.github.com/classrooms/123283353-eco-385), click into the assignment, hit “download” and “Download grades”, save under the same folder as my python script, run the python script to clone everyone’s repo into the same folder 🙂

    ```python
    # replace the value with the name of the grade csv
    csv = "gittask1-grades-1674848937.csv"


    # replace the value with the path of your folder
    your_folder = "\OneDrive\Python\github scrape"


    # you have to pip install gitPython first
    import pandas as pd
    import git
    works = pd.read_csv(csv)
    repo_urls = works.student_repository_url.values.tolist()
    for repo in repo_urls:
        git.Git(your_folder).clone(repo + ".git")
    ```