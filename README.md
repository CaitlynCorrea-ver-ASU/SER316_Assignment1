# README for Assignment 1 Task 2 for SER 316


---


**Description of Branch Structure:**

    - main is the initial branch and the start of the 'number guessing game'

    The following all stem from main:
    - the dev branch holds changes that are shared between branches(?), source of encouragement message for players feature 
    - the feature branches each have a feature they are set to implement:
        - feature1: quit and play again
        - feature2: maxAttempts and gameOver 
        - feature3: hint feature
    - hotfix: contains fix to the number generator
    - documentation: holds a concise documentation of branches and their commits



---


**Description of Branch Changes:**
    main:
    - the initial number guessing game branch

    feature1:
    - stems from main
    - add feature to quit the game
    - add play again loop
    - improve feedback messages for guessing
    - add quit feature version 1.1 

    feature2:
    - stems from main and dev 
    - add encouragement message for players --- comes from dev branch actually
    - add maxAttempts and gameOver state
    - implement the maxAttempts and gameOver components


    feature3:
    - stems from main
    - hard to understand due to poor commit messages
    - add hint feature

    dev:
    - stems from main
    - add encouragement message for players

    hotfix:
    - stems from main
    - fix issue with randomInt to include a max range



---


**Learning Summary**

    merge: combines the commit history of two branches. A merge of branches can either fast-forward or three-way merge. A fast-forward is when the target branch is ahead of current one (aka they have not diverged), and the branch commit pointer is moved to the latest commit of the current one. When branches have a diverged history of commits this becomes a three-way split merge. The diverged histories will need to be combined with a merge commit.
    rebase: used to add a series of commits to the end of a target branch to ensure the branch is caught up into a linear sequence of commits. Not recommended on branches/commit history that is actively being used by other developers.
    squash: condense commits into a single (hopefully cleaner) commit and in turn commit history. 
    cherry-pick: add a specific commit from one branch onto the current active branch (useful for merging bug fixes onto one branch without need of full branch merges)

    what was observed in the git history for feature1 vs feature2 vs feature3?
        feature1: added play again loop, feedback messages, and quit game functionality. Thanks to very focused changes and commit messages we were able to easily analyze and combine with dev branch using merge
        feature2: added maximum attempts and game-over condition to game functionality. This branch was stemmed from both main and dev with its own functionality added. Required a bit more of deatailed observation to determine what sections of code to remove in order for a successful combination.
        feature3: added a hint system functionality. The original commits were unhelpful and required condensing in order to make the branches history more clear

    when would each strategy be used?
        - merge: when combining completed feature branches into a share branch all while preserving the overall branch history
        - rebase: when updating a feature branch with recent changes from another branch while maintaining linear history
        - sqaush: combining smaller comits into more concise combined commits
        - cherry-pick: when adding a specific change (such as a bug fix), without adding unwanted commits from other branches

    Overall I have learned that a clean commit history (with descriptive and consistent message structures) helps to maintain branches and code overall. When merging code of different branches it is important to ensure that each snippet of code does not interfere with the other and to determine what changes must be made to keep the functionality of the combos.

    
