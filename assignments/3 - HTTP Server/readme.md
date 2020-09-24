# CS 346 Assignment #3 - HTTP Server
In this assignment, you will finish implementing a basic HTTP server using a [pre-built template](https://github.com/HSU-F20-CS346/http-server).   A walkthrough of how everything works will be done in class.  A video recording of this will be posted on Canvas.

# Getting Started
Begin by creating a private repository in the course's [GitHub organization](https://github.com/HSU-F20-CS346).
Your repository name **__must__** be in the following format: ```p03-{HSU LOGIN}```.  Thus, my project repository
name would be ```p03-asc564```.  When creating your repository, be sure to initialize your repository with a readme
and add a VisualStudio .gitignore template.  License doesn't matter so much -- I typically choose Apache.  

Once created, your repository should have a "src" directory that contains your solution file and 
a project directory.  See the [the http server](https://github.com/HSU-F20-CS346/http-server) repository on
how I expect things to be set up.    

**__NOTICE:__** Failing to set up your repository correctly will result in reduced assignment credit.  

# Project Requirements
In order to receive full credit, your program must meet the following requirements.

## Requirements
At minimum, you will need to implement a basic http server that properly serves web pages to a web browser (I'm using a Chrome derivative).  Throughout the starter code, you will find PA3 TODOs.  For full credit, you will need to implement all of them.  

1. Enumerations.cs
2. RequestHeader.cs
3. GetRouteHandler.cs
4. PostRouteHandler.cs
5. RouteHandlerFactory.cs

Each of the above files has a TODO comment with details on what is expected. 

## Indicators of success
After implementing all requirements, your web server should properly serve HTML web pages.  This can be verified by examining the home page:

![home page](success_indicators.png)

Note the three red circles.  The top right indicates that you are serving ICON files correctly.  The telephone indicates that you are serving images correctly.  Lastly, the darker background indicates that you are serving CSS correctly.  

### Login page
The login page will simulate login behavior based on the supplied user name and password.  If the user enters "luckylogger@humboldt.edu" with password "password", the server should direct the user to success.html.  Otherwise, the user should be redirected to failure.html.

In order for this behavior to work properly, you will need to implement HTTP POST functionality in the server (see TODO items).

## Adding additional files to your server
The server should serve everything in the "public" folder.  If you are testing this in Visual Studio, you will need to adjust the properties for each file that you would like to serve.  Under "Copy to Output Directory" select either "Copy always" or "Copy if newer."

![Copy always](file_properties.png)

## Advanced (Bonus) Requirements
Unlike the prior assignment, there are no mandatory advanced requirements -- these are just suggestions for getting bonus points.

1. You add support for additional MIME types (e.g. MP3, JavaScript, etc.)
2. You tie user logins to a SQLite database.  
3. You improve the HTTP server in some way (e.g. compression, supporting HTTPS, etc.)
4. You implement additional HTTP Methods (e.g. PUT, DELETE, etc.)
5. Anything else that inspires you (check with me first)

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
The official deadline is Monday, October 12, 2020 by midnight.  Submit your reflection and buddy report on Canvas.  Be sure to include a licecap demo of your project in the root of your repository.  Include a link in your main readme.md
