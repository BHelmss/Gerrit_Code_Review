# Gerrit_Code_Review

## Project Overview
Author: Brendan Helms

Date: November 24, 2024

Abstract: This project demonstrates the implementation of a Gerrit review workflow for secure software engineering. I created a new text file, staged and committed it using Git, pushed it to a Gerrit server, and facilitated a code review process with a new reviewer account. The workflow involved creating and managing branches, handling SSH authentication, reviewing changes, and merging updates, ensuring a collaborative and secure development process. The project highlights my ability to use Git and Gerrit for version control and code review in a team setting.

## Objectives
- Create, stage, and commit a new file using Git, ensuring proper version control practices.  

- Push changes to a Gerrit server, setting up a branch and resolving authentication issues.  

- Establish a code review process by creating a reviewer account and facilitating multi-user reviews.  

- Manage updates, merge changes, and create a commit point to finalize the review workflow.

## Project Steps and Findings
1. File Creation and Staging  
Created a new file text5.txt using the command echo "This is a text5 file for Gerrit review workflow" > text5.txt, verified with cat.  

2. Stage the file using git add text5.txt and confirmed with git status.

3. Committing and Pushing to Gerrit  
Committed the file with a message using git commit -m "Add text5.txt for review", verified with git status.  

4. Encountered an error when pushing to the Gerrit server due to a missing branch; resolved by creating branch1 on the server and fetching updates with git fetch gerritdemo.  

5. Disabled the Change-ID requirement in the repository settings to successfully push the commit.

6. Setting Up a Reviewer  
Attempted to create a new user via SSH on port 29418 but faced a permission error; resolved by generating an SSH key pair (id_rsa, id_rsa.pub) and adding the public key to the Gerrit server.  

7. Created a new Reviewer1 account using SSH, temporarily adding it to the Service Users group for visibility.

8. Code Review and Collaboration  
As admin, reviewed the text5.txt file, gave it a +1 rating, and assigned Reviewer1 for further review.  

9. Logged in as Reviewer1, reviewed the change, and gave a +1 rating, notifying the admin for final approval.

10. Final Changes and Approval  
As admin, edited text5.txt via the Gerrit interface, adding a second line to create Patchset2, then gave a +2 approval to finalize the change.  

11. Fetched Patchset2 to the local repository using git fetch gerritdemo refs/changes/04/12345/2 and merged it into branch1.  

12. Created an empty checkpoint commit to mark the completion of the review process.

## Key Takeaways
- Gained hands-on experience with Git commands (add, commit, push, fetch) and Gerrit for version control and code review.  

- Learned to troubleshoot SSH authentication issues by generating and configuring SSH keys for secure communication.  

- Demonstrated the ability to facilitate a collaborative code review process, ensuring secure and efficient software development workflows.

## Tools Used
- Git: Version control system used for staging, committing, and pushing changes.  

- Gerrit: Code review tool used to manage the review workflow and collaborate with reviewers.  

- SSH: Protocol used to authenticate and communicate with the Gerrit server.

## Conclusion
This project showcases my ability to implement a secure software engineering workflow using Git and Gerrit. By creating a file, pushing it to a Gerrit server, setting up a reviewer, and managing the review process, I’ve demonstrated proficiency in version control, collaboration, and secure development practices. These skills prepare me for roles in software engineering and cybersecurity where collaborative code review and secure workflows are essential.
