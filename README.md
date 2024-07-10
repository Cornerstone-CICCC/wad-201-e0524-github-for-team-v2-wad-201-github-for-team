# Github for Team

> In this section, You will form a group of three to setup branch protection rule.

## Scenario:

Your team's `main` branch cannot be broken at any time, so we need to block not to push the code change from local branch to main branch. Also, we, as a team, would like to review each others code in order to catch mistakes, improve code quality, and learn from each other.

## Solution: Branch Protection Rules

Protect the main development branch (`main`) to prevent direct pushes and enforce code reviews before merging changes.

## Steps:

1. Navigate to your GitHub repository.

2. Click on the "Settings" tab located at the right end of the menu bar of your repository.

3. In the left sidebar of the Settings page, click on "Branches."

4. Click `Add branch protection rule` button

5. Add `main` branch to `Branch name pattern` input

6. Add a checkmark to the following options:

- Require a pull request before merging
  - Require approvals
- Require status checks to pass before merging
  - Require branches to be up to date before merging
- Do not allow bypassing the above settings

> browse around to see anything interesting and test out with your team

7. Save by clicking `create` button
   Require Pull Request Reviews:

8. Find out how the branch protection rule works for your collaboration with the exercise below.
   Things to try:

- Try to push your code change to `main` branch directly
- In Pull Request, try to merge your branch in to `main` before getting approval from your team
- In Pull Request, try to merge when your branch is not up to date

# Git Practice Exercise: Collaborative Code Editing with Conflict Resolution

> In this practice exercise, you will simulate a collaborative text editing project involving three students: Student 1, Student 2, and Student 3. You'll work through various Git actions using text files and focus on resolving conflicts that arise due to newer changes being pushed while pull requests are open. This exercise will guide you through the steps of conflict resolution in Git.

## Scenario:

You're working on a collaborative short story using Git. Each student will contribute a paragraph to the story.

## Steps:

### Step 1: Set Up the Repository

- Student 1 (S1): Clone the repository to your local machine.
- S1: Create a text file named `story.txt` and write the opening paragraph. Commit and push this version.

### Step 2 - 1: Student 1 Adds a Paragraph

- Student 1 (S1): After step 1, create a new branch named `add-paragraph-s1` for your work.
- S1: Open `story.txt`, add another paragraph, and save the file.
- S1: Commit your changes to the `add-paragraph-s1` branch.
- S1: Push the branch to the remote repository.
- S1: NOTE: **_DO NOT MERGE YET_**, Create a pull request to merge the `add-paragraph-s1` branch into the `main` branch.

### Step 2 - 2: Student 2 Adds a Paragraph

- Student 2 (S2): Wait until S1 finishes step 1 and then clone the repository to your local machine.
- S2: Create a new branch named `add-paragraph-s2` for your work.
- S2: Open `story.txt`, add your paragraph, and save the file.
- S2: Commit your changes to the `add-paragraph-s2` branch.
- S2: Push the branch to the remote repository.
- S2: NOTE: **_DO NOT MERGE YET_**, Create a pull request to merge the `add-paragraph-s2` branch into the `main` branch.

### Step 2 - 3: Student 3 Adds a Paragraph

- Student 3 (S3): Wait until S1 finishes step1 and then clone the repository to your local machine.
- S3: Create a new branch named `add-paragraph-s3` for your work.
- S3: Open `story.txt`, add your paragraph (after S1's paragraph), and save the file.
- S3: Commit your changes to the `add-paragraph-s3` branch.
- S3: Push the branch to the remote repository.
- S3: NOTE: **_DO NOT MERGE YET_**, Create a pull request to merge the `add-paragraph-s3` branch into the `main` branch.

### Step 3: Conflict Arises

- S2: Merge the `add-paragraph-s2` pull request into the `main` branch.
- S3: Try to merge the `add-paragraph-s3` pull request into the `main` branch, but it is not allowed because there is a conflict since both S2 and S3 changed the same file.
- S3: In your local repository, switch to `main` branch and pull the recent changes.
- S3: Switch back to `add-paragraph-s3` and merge `main` branch into it.
- S3: Resolve the conflict by editing `story.txt` to include both S2 and S3 paragraphs in the correct order.
- S3: Commit the resolved conflict and push the branch to the remote repository.
- S3: Go back to your PR and check if now the branch can be merged to main. if so, please do.

### Step 4: Another Conflict

- S1: Try to merge the `add-paragraph-s1` pull request into the `main` branch, but it is not allowed because there is a conflict.
- S1: In your local repository, switch to `main` branch and pull the recent changes.
- S1: Switch back to `add-paragraph-s1` and merge `main` branch into it.
- S1: Resolve the conflict by editing `story.txt` to include all three students' paragraphs in the correct order.
- S1: Commit the resolved conflict and push the branch to the remote repository.
- S1: Go back to your PR and check if now the branch can be merged to main. if so, please do.

### Step 4: Wrapping Up

- S1, S2, and S3: Confirm that the `main` branch now contains all four paragraphs of the story.
- S1, S2, and S3: Delete the branches related to your contributions.
- S1, S2, and S3: Your collaborative Git exercise with conflict resolution is complete!

> Note: Conflict resolution involves careful consideration and communication among team members. In real-world scenarios, team members should coordinate and communicate effectively to handle conflicts, ensuring that no changes are lost during resolution.
