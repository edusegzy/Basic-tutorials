# How to contribute

_All credit for the explanations below goes to Atlassian and its tutorial for the ["Forking Workflow"](https://www.atlassian.com/git/tutorials/comparing-workflows/forking-workflow)_

The snippets below have been adapted with the locations of our own repository for convenience.

Key points:

* Limits unintended access and mistakes.
* It is easy to setup, and it is not too complicated to follow.
* Every user owns his/her own remote repository (e.g., via his/her own GitHub account).
* "Forking" is nothing more than cloning between remote repositories. It is **not** a feature of Git.

### Procedure:
The following steps assume the developer is signed into his/her remote account on the remote server (e.g. github.com). This is not strictly a requisite, but it makes the explanation for "forking" simpler.

1. A developer 'forks' an 'official' server-side repository. This creates their own **server-side copy**.  
    ```Use the "fork" button on the repository ```  

2. The new server-side copy is cloned to their **local system**.  
    ```git clone https://github.com/<my_account>/Playground.git ```  

3. A **Git remote** path for the 'official' repository is added to the local clone.  
    ```git remote add upstream https://github.com/Tulsa-Data-Science/Playground.git ```  

4. A new local feature branch is created _(local system)_.  
    ```git checkout -b <name_of_my_branch> ```  

5. The developer makes changes on the new branch as needed  _(local system)_.  

6. New commits are created for the changes  _(local system)_.  
    ```git commit -a -m "My_commit_message"```  

  * If the main project has moved ahead, its changes can be incorporated on the developer's repository by pulling them directly:  
      ```git pull upstream master```  

7. The branch gets pushed to the developer's own server-side copy.  
    ```git push origin feature-branch```  

8. The developer opens a pull request from the new branch to the 'official' repository.  
    [Use "pull request" button on the main repository.](https://github.com/Tulsa-Data-Science/Playground/pull/new/master)

9. The pull request gets approved for merge (if applicable) and is merged into the original server-side repository