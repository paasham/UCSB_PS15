# UCSB_PS15
POLS 15 section and HW code

How-to:

The set-up is as follows. There is a GitHub repo (https://github.com/paasha/UCSB_POLS15) where each week you can push section materials and homeworks. You can also use this to push exams at a specified time.

In a nutshell, the system works by creating a link which automatically pulls the latest changes from the repo to the user's JupyterHub workspace. This is a one-way sync, so that the user can never push their edits to the repo, they can only pull from the repo. The link https://bit.ly/POLS15_Update is simply a shortened version of the link https://pols15.lsit.ucsb.edu/hub/login?next=%2Fhub%2Fuser-redirect%2Fgit-pull%3Frepo%3Dhttps%3A%2F%2Fgithub.com%2Fpaasha%2FUCSB_POLS15%26urlpath%3Drstudio%2F.

You will notice that this links contains several arguments, including the URL of your JupyterHub (https://pols15.lsit.ucsb.edu) and the URL of the repo that you want to pull from (https://github.com/paasha/UCSB_POLS15).

If you want to create your own link to pull from your own GitHub repo, you can use the link generator here: https://jupyterhub.github.io/nbgitpuller/link. This link generator will generate a long link for you, and you can then shorten it using your favorite link shortening service. 

Note that what the system does is a git pull, which combines a git fetch and a git merge command. Say a student starts working on a homework by adding text to an answer, and then clicks the update link. Since the repo will contain the homework assignment where there is no text for the answers, this should not overwrite the student's work since it is a merge. But, never underestimate the creative ways in which user error can occur! For that reason, I recommend that you instruct students to set up their RStudio workspace with two folders at the root:

- Homeworks (this is the folder where they can work on their assignments)
- UCSB_POLS15 (this is the root folder of the GitHub repo, which every week will be populated with sub-folders such as "Week 1", "Week 2", etc.)
