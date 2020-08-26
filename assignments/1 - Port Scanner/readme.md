# CS 346 Assignment #1 - Port Scanner
In this assignment, you will extend [the Echo Service](https://github.com/HSU-F20-CS346/Example-EchoService) 
sample project by building a port scanner that you can use to determine if a given TCP or UDP 
port is open on a specified server.  

# Getting Started
Begin by creating a private repository in the course's [GitHub organization](https://github.com/HSU-F20-CS346).
Your repository name **__must__** be in the following format: ```p1-{HSU LOGIN}```.  Thus, my project repository
name would be ```p1-asc564```.  When creating your repository, be sure to initialize your repository with a readme
and add a VisualStudio .gitignore template.  License doesn't matter so much -- I typically choose Apache.  

Once created, your repository should have a "src" directory that contains your solution file and 
a project directory.  See the [the Echo Service](https://github.com/HSU-F20-CS346/Example-EchoService) repository on
how I expect things to be set up.    

**__NOTICE:__** Failing to set up your repository correctly will result in reduced assignment credit.  

# Project Requirements
In order to receive full credit, your program must meet all Basic and Advanced requirements.

## Basic Requirements
At minimum, Your program should accept command-line parameters in the following sequence:

```
PortScanner <IP ADDRESS> <PORT> <Protocol (default TCP if empty)>
```
Examples:
```
PortScanner google.com 80 
```

```
PortScanner 216.58.206.206 80 TCP
```

```
PortScanner google.com 7 UDP
```

Your port scanner should indicate whether or not the specified port is ```OPEN``` or ```CLOSED```.

## Advanced Requirement #1
Your program should also be able to scan a range or ports:

```
PortScanner <IP ADDRESS> <BEGIN PORT>:<END PORT> <Protocol (default TCP if empty)>
```

Example:
```
PortScanner 127.0.0.1 22:80 TCP
```
The above example would scan the google.com domain for ports 22-80 inclusive.  Your program should 
report the status of each port:
```
Port 22: OPEN
Port 23: CLOSED
Port 24: CLOSED
...
Port 80: OPEN
```

## Advanced Requirement #2
In addition to a port range, your program should accept the word COMMON as a valid port range.  
Your program should then scan all "common" ports at that given IP address.  For a list of all
common ports, see [this Wikipedia article](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers).
Common ports range between 1 and 1023 and are listed in the table as having an "Official" IANA status.  

Example:
```
PortScanner 127.0.0.1 COMMON TCP
```

## Bonus #1
In addition to outputting to the screen, you also write the results to a CSV file.  

## Bonus #2
You build a GUI for your application using either WinForms or Xamarin / WPF.  

## Bonus #3
Come up with something yourself!  Just okay it with me first :)

# Tips
Not sure where to start?  Try running the EchoService client with and without the server running. 
What do you notice?

The default TcpClient timeout is a little long which will make scanning multiple ports take too long.  
[This StackOverflow article's accepted answer](https://stackoverflow.com/questions/17118632/how-to-set-the-timeout-for-a-tcpclient)
shows how you can lessen the timeout.  

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
deep though) rather than syntax (e.g. spelling) and structure.  Below are some prompts that can be used to get 
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
* Completing the basic requirements, github workflow, design diary, and buddy report will result in a C
* Completing all above requirements and **__one__** advanced requirement will result in a B
* Completing all above requirements and **__all__** advanced requirements will result in a A
* Completing one or more bonuses will result in extra credit if and only if all requirements 
have been implemented.  