Analyzing the NYC Traffic Death Data
================

Set RStudio up for GitHub
-------------------------

### Configure Git

To send files back to GitHub after you have changed them, you will need to configure RStudio's version of Git with your name and email address.

1.  Go to Tools --&gt; Shell
2.  Type `git config user.name "Your Name"`, inserting your name
3.  Hit Enter
4.  Type `git config user.email "your@emailaddress.com"`, inserting your email
5.  Hit Enter
6.  Click Close

### Fork a GitHub repository

If you want to work on a project someone else has already started, you might want to make a copy of that project under your own GitHub account. That process is called "forking".

1.  Find a repository of interest, e.g., <https://github.com/datanews/mean-streets>
2.  Sign in if not already signed in
3.  Click on the Fork button at the top right-hand corner

### Find the correct URL GitHub Repository URL

1.  Go to the repository you want (either the original or your forked version, if you are forking)
2.  Click on the green "Clone or download" button
3.  Copy the URL from the box that opens

### Connect to the GitHub Repository

1.  Click the project button in the upper right-hand corner of RStudio
2.  Create a New Project
3.  If it asks you to save a file, you can hit Save or Don't Save
4.  Choose "Version Control"
5.  Choose "Git"
6.  Paste in the URL from GitHub (see above)
7.  Create a name for the folder the project will use
8.  Click "Create Project"

### Create the file where the R code and plots will go

This file was created specially to display well in GitHub. It was created with the following steps.

1.  Go to File --&gt; New File --&gt; R Markdown
2.  Click on "From Template"
3.  Scroll down and select "GitHub Document"
4.  Change title
5.  Save file with a meaningful name

### Saving back up to GitHub

Before pushing files to GitHub, you should "Knit" the analysis file by clicking the "Knit" button at the top. This will generate a standard markdown file that can be displayed easily by GitHub. This way, people looking at your files on GitHub will see all of your code and charts properly.

Note: you can only save files back to a repository you own. RStudio will create a project based on any repository on GitHub, but you won't necessarily be able to save back to it. If you want to store your files on GitHub, you should always Fork the repository to your account first.

1.  "Knit" the .Rmd file using the Knit button at the top of the window
2.  Save the .Rmd file and any other files
3.  In the upper right-hand window, click on "Git"
4.  Click "Commit" This basically creates a save point for your files -- something you can go back to later, if you need to.
5.  A new window will try to pop up. If your browser blocks it, authorize the pop-up to appear.
6.  Check the box next to all of the files in the top left-hand area
7.  Type a short message in the top right-hand box describing the changes you're making to the project in this particular upload e.g., "adding analysis file", "changing colors in figures"
8.  After the commit, you still have to "Push" or upload the files up to GitHub. Click the Push button, either in the Commit window or in the normal RStudio window.
9.  When it asks you to log in, use the username and password of the account you used to fork (or create) the repository

GitHub Documents
----------------

This is an R Markdown format used for publishing markdown documents to GitHub. When you click the **Knit** button all R code chunks are run and a markdown file (.md) suitable for publishing to GitHub is generated.

Including Code
--------------

You can include R code in the document as follows:

``` r
summary(cars)
```

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

Including Plots
---------------

You can also embed plots, for example:

![](traffic-death-analysis_files/figure-markdown_github/pressure-1.png)

Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.
