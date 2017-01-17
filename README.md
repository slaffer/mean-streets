# Steal this data: Using R and GitHub for Open, Collaborative Research

## Why use GitHub and R?

GitHub is a website where you can share data and code publicly or within a small group of collaborators.  Sharing data projects on GitHub can be a great back-up solution and can also help you build a portfolio of data projects.  

"Stealing" and improving projects that have been shared on GitHub is also a great opportunity to contribute to a larger effort or to learn new skills from more experienced coders and analysts.  

If you already use RStudio to work on data projects, you can easily use the built-in "projects" to connect straight to an existing GitHub repository. This repository includes instructions for how to do this. (Note: some instructions are specific to Duke University.)

## About Version Control

GitHub is a tool for something called "version control."  Version control systems help programmers keep track of changes to code over time.  Why is this important?  Sometimes important code is accidentally deleted, or a new part of the code breaks an old part.  Sometimes two people want to be working on the same code at the same time.  Version control systems manage "versions" of files so that problematic changes can be reversed, different edits to a file can be merged back into a single file, etc. 

This is something we encounter regularly as software consumers.  Our favorite programs all have new versions that come out periodically.  Other programs may control our versions for us -- think about Google Docs, where you can see changes that have been made and go back to previous versions.  You may even have done some version controlling yourself without knowing it.  Have you ever played a video game where you had to manually save?  Choosing the right time to save can be the difference between playing a whole level over again and starting right before the big boss fight at the end.

Using R for your data analysis project is a great first step toward open, reproducible science, but version control systems like GitHub are the next, big step.  Using GitHub can really supercharge your data analysis project by giving you a safe place to store code and encouraging safe code development practices.

## Creating new versions

So, when is a good time to complete a "version?" In version control software, you usually have to decide when to wrap up a version, like the video game example above.  You can save the files on your computer whenever you want, but they don't get stored in the version control system (or the "repository") until you decide it's time to send an update.  In general, it's better not to go through an entire "video game level" without creating a new version.  

You don't have to create a new version for every line of code you write, but don't wait until the boss fight, either.  Adding regular versions to your repository, especially after adding major analysis steps and new functions, will help you get back to "the last stable point" if anything goes wrong.  Also, by adding useful messages each time you create a version, it will be much easier to remember what changes happened in each version.

## Create an RStudio Project to pull files from GitHub

RStudio has a feature called ["Projects"](http://r4ds.had.co.nz/workflow-projects.html) that can be used to organize all of the files for a single analysis project.  (Even if you don't use GitHub, you should definitely use Projects!)  Conveniently, RStudio Projects can easily be created from files that are stored on GitHub.  Just follow the steps below.

### Fork a GitHub repository

If you want to work on a project someone else has already started, you might want to make a copy of that project under your own GitHub account first.  That process is called "forking".  It's not absolutely necessary, but you have to do this if you later want to save files back up to GitHub.

1. Find a repository of interest, e.g., <https://github.com/datanews/mean-streets>
2. Sign into GitHub if not already signed in
3. Click on the Fork button at the top right-hand corner

### Find the correct URL GitHub Repository URL

1. Go to the repository you want (either the original or your forked version, if you are forking)
2. Click on the green "Clone or download" button
3. Copy the URL from the box that opens

### Connect to the GitHub Repository

1. Click the project button in the upper right-hand corner of RStudio
2. Create a New Project
3. If it asks you to save a file, you can hit Save or Don't Save
4. Choose "Version Control"
5. Choose "Git"
6. Paste in the URL from GitHub (see above)
7. Create a name for the folder the project will use
8. Click "Create Project"

## Code files, GitHub style

RStudio has a template that creates a file that's specially designed to display well in GitHub.  Follow these steps to create a GitHub Document where the R code and plots will go:

1. Go to File --> New File --> R Markdown
2. Click on "From Template"
3. Scroll down and select "GitHub Document"
4. Change title
5. Save file with a meaningful name

## Saving back up to GitHub

### Configure Git

Note for Duke users on the RStudio Docker container: To send files back to GitHub after you have changed them, you will need to configure RStudio's version of Git with your name and email address.

1. Go to Tools --> Shell
2. Type `git config user.name "Your Name"`, inserting your name
3. Hit Enter
4. Type `git config user.email "your@emailaddress.com"`, inserting your email
5. Hit Enter
6. Click Close

### Create and upload the new version

Before pushing files to GitHub, you should "Knit" the analysis file by clicking the "Knit" button at the top.  This will generate a standard markdown file that can be displayed easily by GitHub.  This way, people looking at your files on GitHub will see all of your code and charts properly.

Reminder: you can only save files back to a repository you own.  RStudio will create a project based on any repository on GitHub, but you won't necessarily be able to save back to it.  If you want to store your files on GitHub, you should always Fork the repository to your account **before** creating your RStudio Project.

1. "Knit" the .Rmd file using the Knit button at the top of the window
2. Save the .Rmd file and any other files
3. In the upper right-hand window, click on "Git"
4. Click "Commit"

    This basically creates a save point for your files -- something you can go back to later, if you need to.

5. A new window will try to pop up.  If your browser blocks it, authorize the pop-up to appear.
6. Check the box next to all of the files in the top left-hand area
7. Type a short message in the top right-hand box describing the changes you're making to the project in this particular upload

     e.g., "adding analysis file", "changing colors in figures"

8. After the commit, you still have to "Push" or upload the files up to GitHub. Click the Push button, either in the Commit window or in the normal RStudio window.
9. When it asks you to log in, use the username and password of the account you used to fork (or create) the repository

* * *

**Original Documentation**

* * *

# Mean Streets

Data on 268 New York City traffic deaths in 2014.

# Background

In early 2014, New York City Mayor Bill de Blasio announced his ["Vision Zero" plan](http://www.nyc.gov/html/visionzero/pages/home/home.shtml) to prevent traffic deaths through new policies, enforcement, and educational initiatives.

WNYC's [Transportation Nation](http://www.wnyc.org/section/transportationnation/) and [Data News](http://datanews.tumblr.com/) teams sought to track every death resulting from a New York City traffic collision in 2014.

Data is compiled based on collision reports from the NYPD Office of the Deputy Commissioner for Public Information (DCPI), news reports, and information from the New York City and New York State Departments of Transportation.

`traffic-deaths.csv` includes the following details for each collision, when available:

* Date
* Time
* Location (borough, police precinct, intersection, latitude, longitude)
* Victim information (name, gender, and age)
* Victim type (pedestrian, driver, cyclist, or passenger)
* Vehicle description
* Incident summary
* Criminal charges filed
* Related news stories

# Related Resources

* [The Mean Streets Tracker](http://project.wnyc.org/traffic-deaths/)
* [The Mean Streets Memorial](http://project.wnyc.org/memorial/)

# Credits/Contact

transponation@gmail.com  
(347) 352-5686

WNYC Transportation Nation:

* Kat Aaron
* Andrea Bernstein
* Kate Hinds
* Jim O'Grady

WNYC Data News:

* John Keefe
* Jenny Ye
* Kio Stark
* Louise Ma
* Noah Veltman
