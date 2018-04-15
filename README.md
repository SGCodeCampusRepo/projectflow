# How to Manage a Development Project using Agile and Kanban

## Initializing the project
* The project leader creates a repo on Github to hold the application code
* All team members then clone the repo onto their local machines
* Create a Github Project on your repo page by following the steps detailed in the next section

## Design and Planning Phase
* Prototyping with **User Stories** and Wireframing with hand sketches
  * Create a Kanban board with **Github Projects**
    1. Create a **To Do** column and set it to auto-populate issues
    2. Create an **In Progress** column
    3. Create a **Review** column
    4. Create a **Done** column
  * Create a card in the **To Do** column for each feature you want to build
    * User Stories should have the following form: **<USER>** needs to be able to **<DO SOMETHING>** in order to **<ACHIEVE GOAL>**
    * Example:
      * Members of my E-Commerce site need to be able to view their purchase history in order to keep track of their buys
  * When all the cards are done, score and label each card in terms of the effort needed to implement that feature using a fibbonacci score (eg. 1, 2, 3, 5, 8, 13, 21, 34, ...)
  * If a feature has a high score, this is usually an indication that the feature is too complex; in which case break it down further into simpler User Stories and rescore
* Order the cards in the **Todo** column in order of how you want them prioritized keeping the effort scores in mind

## Build phase
* For each card/feature
  * pull the card off **ToDo** into **In Progress**
  * no single team member should be working on more than one card at any one time
  * pull from the remote repo to your local machine
  * create a branch on your local machine for the current card/feature and commit code to this local branch as you work
  * When the feature is done 
    * commit the local branch to the remote repo by running ```git push origin <BRANCH_NAME>```
    * on the repo GitHub page, select the option to activate a **pull request** for the branch you have just committed
    * move your card from **In Progress** to **Review**
    * link the pull request to the User Story/feature card by pasting the pull request URL into the card
    * assign one of your team-mates to review your code from the pull request page
    * both reviewer and reviewee can leave their comments on the pull request page
  * For the Reviewer: 
    * add your comments (if any) to the pull request page
    * possible actions after review:
      * reject by closing the pull request
      * accept by merging
  * All team members update the merged branch by pulling from GitHub
    * **rebase** their branches if necessary

## Extra considerations
* Conflicts can happen when you ```rebase```, ```merge```
  * change your local file before adding and committing and rebasing or merging
  * reset the master trunk before you merge your branch (not recommended)
* open issues for bugs you have found
* Nuclear option for forcing a change on your GitHub repo
  * git push —force
