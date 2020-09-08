# CS 346 Assignment #1 - Port Scanner
In this assignment, you will implement a chat client for a pre-built [chat server](https://github.com/HSU-F20-CS346/chat-server).  A walkthrough of how everything works will be done in class.  A video recording of this will be posted here once available.

# Getting Started
Begin by creating a private repository in the course's [GitHub organization](https://github.com/HSU-F20-CS346).
Your repository name **__must__** be in the following format: ```p02-{HSU LOGIN}```.  Thus, my project repository
name would be ```p02-asc564```.  When creating your repository, be sure to initialize your repository with a readme
and add a VisualStudio .gitignore template.  License doesn't matter so much -- I typically choose Apache.  

Once created, your repository should have a "src" directory that contains your solution file and 
a project directory.  See the [the chat server](https://github.com/HSU-F20-CS346/chat-server) repository on
how I expect things to be set up.    

**__NOTICE:__** Failing to set up your repository correctly will result in reduced assignment credit.  

# Project Requirements
In order to receive full credit, your program must meet all Basic and Advanced requirements.

## Requirements
At minimum, you will need to implement a basic chat server that properly communicates with the pre-built chat server.  This means that your program must:

1. Prompt the user for authentication
2. Send new chat messages from the local client to the server
3. Receive new chat messages from the server and display them on the screen

## Advanced (Bonus) Requirements
Unlike the prior assignment, there are no mandatory advanced requirements -- these are just suggestions for getting bonus points.

### GUI (some bonus points)
Instead of a console-based application, you develop a GUI-based chat application in Winforms, WPF, or Xamarin

### Upgraded client (more bonus points)
You refactor the chat client to make it more robust.  Suggestions for improvement:
1. Gracefully handle exceptions
2. Allow users to backup / save chat messages to a CSV file
3. Allow users to securely store their credentials for faster login

### Upgraded server (more bonus points)
You refactor the server to make it better.  Any changes that you make should be backward compatible with the basic chat client that I provide.  Probably the easiest way to do this is to expose additional TCP ports on which your advanced features run.  Suggestions for improvement:

1. Actually implement authentication
2. Actually use encryption during the authentication process 
3. Store users and messages in a SQLite database
4. Allow clients to get messages sent before their log-in
5. Implement an idle timeout on the server
6. Gracefully handle exceptions (i.e. don't allow them to crash the chat server!)
7. Anything else you can think of

# GitHub Workflow
I spent 100+ hours over the summer looking at git commits and github issues and learning about "good" github workflow.
I would like to incorporate what I learned into my teaching.  To that end, you should:

* Create up an "automated kanban" project board in github.
* Make cards for each project requirement, place them in the "To do" column.  
* When you begin working on a given requirement, drag the associated card to the "In progress" column and convert
the card into an issue
* After doing the initial commit that contains the starter code, all changes should be worked on in a separate branch
* Be sure to tag future commits with the issue number to which they correspond. 
* Once a feature is complete:
   * you should create a pull request to bring the new changes into the main branch.  
   * you close the issue by moving the card to the completed "Done" column in your project board.

## Tips on writing commit messages
Good commit messages should be atomic, accurate, precise and have a rationale:
* **__Atomic__**: Whether the commit focuses on a single concern.
* **__Accurate__**: Whether the commit message identifies exactly those changes that were made—no more, no fewer
* **__Precise__**: Whether the commit message unambiguously describes the changes that were made
* **__Rationale__**: Whether the commit message includes a rationale for the changes made. A best practice for providing such a rationale is to tag the issue or issues addressed by the commit. 

## Tips on writing issues
Good issues should be atomic, have a good title, and describe WHO, WHAT, and WHY. 
* **__Atomic__**: Issue focuses on exactly one concern. 
* **__Title__**: Issue title is short and descriptive.
* **__WHO__**: Issue identifies who is affected by the change. 
* **__WHAT__**: Issue describes what is being changed.  
* **__WHY__**: Issue provides a rationale for the code change. 

An easy way to hit all of this is to create issues whose title is in the following format:

```As a <User Type>, I can <Perform Action> so that <Reason why User Type would want to perform action>```

Example:

```As a IT administrator, I can scan a given port on a server so that I can tell whether or not a given service is running on that server.```

Additionally, acceptance criteria (how you know when the issue is done) should be provided in the issue's description. 
Acceptance criterial are ideally listed as checkboxes using brackets in markdown [].  Note that it is acceptable to create acceptance criteria as you
go alone.  Acceptance criteria themselves should be atomic. E.g. "Allow user to specify either TCP or UDP" is a good
acceptance criteria whereas "Complete basic project requirements" is not.  

Here's an example checklist in markdown

- [x] Task 1
- [ ] Task 2

Note that all checkboxes should be checked before closing an issue.

# Design Diary Prompt
Design diaries should be a paragraph or two.  You will be graded on content (i.e. it shows 
deep thought) rather than syntax (e.g. spelling) and structure.  Below are some prompts that can be used to get 
you thinking.  Feel free to use these or to make up your own.
* Describe a particular struggle that you overcame when working on this programming assignment.
* Conversely, describe an issue with your assignment that you were unable to resolve.
* Provide advice to a future student on how he or she might succeed on this assignment.
* Describe the most fun aspect of the assignment.
* Describe the most challenging aspect of the assignment.
* Describe the most difficult aspect of the assignment to understand.
* Provide any suggestions for improving the assignment in the future.

Your design diary will be submitted on canvas and **__should not__** be included in your repository.

# Buddy Report
You will be assigned one or two buddies at the beginning of the assignment.  You are **__not__**
responsible for your buddy's progress.  Rather, the purpose of this is to build your social 
circle and to to give you someone to check in with as you work on your project.  
Give your honest appraisal of each of your buddies' progress:

* Did they seem like they gave a good, honest effort?  
* Did they get stuck somewhere?
* What ideas were shared / what was discussed during your interactions?
* What did you learn from them?
* Anything else you want to add.

A report for each buddy only needs to be a paragraph.  This Buddy Progress Report is _*in no way*_ 
connected to your Buddy's grade.  It is, however, tied to your grade so be sure to provide an accurate report!

Your buddy report will be submitted on canvas and **__should not__** be included in your repository.

# Grading
* Completing the basic requirements, github workflow, design diary, and buddy report will result in full credit
* Completing one or more bonuses will result in extra credit if and only if all requirements 
have been implemented.  

# Due Date
The official deadline is Tuesday, September 22, 2020 by midnight.  Submit your reflection and buddy report on Canvas.  Be sure to include a licecap demo of your project in the root of your repository.  Include a link in your main readme.md
