__Steps in a data analysis
* Define the question
* Define the ideal data set
* Determine what data you can access
* Obtain the data
	Clean the data
	Exploratory data analysis
	Statistical prediction/modeling
	Interpret results
	Challenge results
	Synthesize/write up results
	Create reproducible code

__Raw data
The original source of the data
Often hard to use for data analyses
Data analysis includes processing
Raw data may only need to be processed once
http://en.wikipedia.org/wiki/Raw\_data
__Processed data
Data that is ready for analysis
Processing can include merging, subsetting, transforming, etc.
There may be standards for processing
All steps should be recorded
http://en.wikipedia.org/wiki/Computer\_data\_processing

__R programming content
Data types
Subsetting
Reading and writing data
Control structures
Functions
Scoping
Vectorized operations
Dates and times
Debugging
Simulation
Optimization
__Something’s Wrong!
How do you know that something is wrong with your function?
What was your input? How did you call the function?
What were you expecting? Output, messages, other results?
What did you get?
How does what you get differ from what you were expecting?
Were your expectations correct in the first place?
Can you reproduce the problem (exactly)?

[https://support.rstudio.com/hc/en-us/articles/200484448-Editing-and-Executing-Code](https://support.rstudio.com/hc/en-us/articles/200484448-Editing-and-Executing-Code)
[https://support.rstudio.com/hc/en-us/articles/200484448-Editing-and-Executing-Code#executing](https://support.rstudio.com/hc/en-us/articles/200484448-Editing-and-Executing-Code#executing)


\_\_Git and GitHub commands 
The first thing that we should do is sort look at the structure of where the different files are and what the different commands are going to do.
So you can start off by looking here at the work space where you're actually working on files on your computer, so that's like the directories where you're working with the files.

Then there's an index. This tells Git what are the files that it should be controlling under version control.
And then there's the local repository; these are the files
that are stored or version controlled on your local computer.
Finally, there's the remote repository.
In our case, that will always be GitHub. So, the idea here is that you're starting off in your workspace and you create a
file.
And the first thing that you need to do is you need to add that file to the index so that Git knows to to monitor that
file and keep up with all of its changes.
And then what you need to do is you need to commit that file so that, you need to put a version of that file in your
local repository so that it can be stored and updated.
So as you make changes, you keep committing those changes to your local repository.

Finally, sometime when you have made a few
Commits and you want to update the remote repository,
then what you'll be doing is you'll be issuing a Push
Command to be able to put those changes into your
remote repository.
Okay, so the first thing that you're going to need to do is suppose you're working in a directory that is a repo that is
being under version control by Git.
So the first thing that you're going to want to maybe do is put new files under version controls, so what you need
to do is add them to the index.
And so to let know, Git know that they
need to be tracked, you can use the add
command.
So this is Gitadd., adds all the new files in your current
working directory that you are working in,
so this is presuming that you are in the
directory where you are adding new files.
Git add -u will actually update what
happens to the files that have changed names or were
deleted.
So gitadd., will just add all the new files, gitadd -u
deals with all the changes to files either adding or
deleting or sort of name changing.
And then gitadd -A does both of the previous things all in one command.
So before you try to commit things to your local repository, you need to make sure that you use the add command, so that
you can add things to the index.
Then once you've added them to the index, you can commit them to your local repo.
And so the way that you do that is you can use the git
commit command, so you do gitcommit, and then a flag, -m, and a message here.
And so the message is hopefully a useful description of
what are the changes that are happening in this command.
So, if I've added some new files, that message might say I've the following new files.
Or it might tell you a little bit about the things that
you've deleted or changed so that you can change your local repo.
This is only going to make changes to the local repo, it
won't make any changes to GitHub, this is still a local action.
So if you would like to put things up on GitHub, then what you can do is, still in that same working directory, you could type the command, git push.
And so what that will do is take all the changes that you've committed up until then and it will push them to the remote directory on Github.
Sometimes you might be working on a project, particularly in this class where there's a version that might be used by many other people, and you might not want to edit the version that's being used by everyone because if you make a lot of changes to it, it might break all the work that they're doing.
So one thing that you might do, first is you might actually create a branch.
So a branch is just another version of the same directory where you can make changes sort of independently.
So what you can do is you can use git checkout -b and then the
name of the branch that you want to do and that will create a new branch.
The default branch for all the repos that are created with Github is the master branch, but you can create a repo with
any other names they develop for development branch.
To see what branch you're on at any given time.
If you go into the current working directory where the repo is,
and you type git branch, it'll tell you what branch you're on.
If you want to switch back to the master branch, what you can do is, you can type git checkout master, and we'll check you out back to the master branch.
And so you can look at that branch. One thing that you can do is once you've made a pull request, or a push of your changes up
to your repo.
Suppose that you're working on a repo where you're on a different branch or you're working on a repo that
you forked from somebody else, then what you might want to do is merge your changes back into the original repo or into the original branch that you were working on.
To do this you need to issue a pull request. This is a unique fit, feature of Gitbhub. It actually isn't a feature of Git.
And so what you do is you go to the Github
website and you, if you go to the branch that you're interested in.
So if you go and pick which branch that you're working on then what you can do is you can actually click on this button over here which is compare and pull request.
And what that will do is it will issue a pull request to the individual that owns that other branch or repo.
So if it's yourself, you'll get a notification that there's been a pull request. If it's somebody else, they'll get a
notification. And then they can decide whether to merge that pull request into their repo or not if they think the changes are appropriate. So you can see all the changes that were made and confirm whether they were sort of appropriate and interesting or not.

So the best place to start is actually a [Github help](%20https://help.github.com/).
Git documentation is actually quite thorough, it takes
a little bit more reading and a little bit more doing. Although my experience has been that the best place to, to deal with this is to type sort of what you think you want to do into Google or into Stack Overflow and you find out the answers much more quickly that way.

\_\_Installing R Packages.
When you download R from the comprehensive R Archive Network CRAN, you get the base R system. Including a bunch of functions
that you can use to summarize data and make plots and things like that. It basically covers the basic function,
functionality that you'll need including implementing
the R language.
But the real reason R is so useful is that
there are a lot
of add-on packages that extend this basic
functionality in a bunch of different
directions.
Everything from cleaning data, to plotting
data,
to analyzing data and making interactive
applications.
So, R Packages are developed and published
by the larger
R community, hopefully including you at
the end of this course.
So, to obtain R Packages the primary place
that you're going to go is CRAN.
But for some biological applications, and
some big data applications, you might also
go to the Bioconductor Project that I have
linked to both the websites here.
You can also obtain information about the
available
packages on CRAN with the available
packages function.
And so what you would do is you can enter
R, start
up, and you'll get a prompt and you can
type this command: a.
And then give it the available packages
argument just like this.
And that will be a large number of
packages.
So you could just hit a after you hit that
you could just type a
and hit return and you would see all the
packages, but there would be thousands.
So instead you can use the head command to
look at say a certain number,
say just three of those, packages so these
are the first three in alphabetical order.
As of the making of this lecture there are
approximately
5200 packages on CRAN covering a wide
range of topics.
An equally large number available on
Bioconductor.
One thing that you can do is if you know
the
area that you're working in, but you don't
know the R package
you're after, you can go to the Task Views
link which
groups together many R packages that are
related to a specific topic.
So to install an R Package you primarily
use the function install.packages.
So what you would, you could do is just
use that with the package name as the
argument.
So for example if I want to install the
Slidify package what I
would do is I would just
type install.packages and then in quotes,
slidify.
And what that would do is that would go to
CRAN and it would install that package on
your computer.
Any package on which that package depends
will also be downloaded and installed.
This is actually one of the nicest parts
about
R, is that it's relatively straightforward
to install new packages.
You can also install multiple R packages
with a single
line, so what you do is you again, you
type, install.packages.
And now what you do is you enclose in
parentheses, with a C out front.
All the different package names separated
by commas,
and surrounded by parenth, or surrounded
by quotes.
And then what that would do is install the
slidify, ggplot2, and devtools packages.
You can also install packages relatively
straightforward procedure
in RStudio, so hopefully you've installed
R in RStudio.
You can go up to the Tools Menu and then
just go down
to Install Packages, and that will open up
a folder that will allow
you to pick the repository and then pick
the package that you want to
be able to install from, and it will
install that package for you.
Installing packages from Bioconductor is a
little bit different.
You don't use install.package, but it's
still quite since, straightforward.
So what you do is you go and you type this
command, source
and then this website right here, and that
will load the biocLite function.
And so then first you just type biocLite
by itself and what
that will do is it will install the basic
version of Bioconductor.
That's actually quite a few packages so be
prepared for a
lot of packages to be installed the first
time you run it.
Then the next time you want to install
specific
package you again would do just like you
would install.packages.
As you type biocLite and then c,
parentheses, and then
each package name in quotation part, marks
separated by a comma.
So that's how you install packages like
that.
You can also load the packages after
you've installed them.
So if you install it, it doesn't mean that
all of the functions are immediately
available to you.
You need to use the library command to
tell R which packages to load in.
So, for example, if you've installed the
ggplot2 library, and
you want to be able to use the functions
in
ggplot2, you need to type in the command
library(ggplot2) in
order to get access to that functions in
that package.
All packages need to be loaded, will be
loaded first, so for example if
you are missing some dependancies, then
you wont be able to load that package.
An important note here is that you should
not put the package names
In quotes when you are using library
otherwise you won't get correct loading.
[INAUDIBLE](#) some packages produce messages
when they are loading and some don't.
Either way you don't need to worry about
it.
So after you load a package the functions exported by that package will be attached at the top of the search list so what you can do is you can type library(ggplot2).
And then if you type search, open parentheses, close parentheses, you will see all of the functions that are part of the ggplot2 package.
So the summary is that R package is a powerful mechanism for extending the functionality of our R Packages could be obtained by CRAN or other repositories.
You install the packages, function could be used to install packages from the R console and then library is what you do to load the packages in to actually get access to the functions.

\_\_The basics of markdown.
So markdown is just a text file that's formatted in a very specific and simple way that sites like GitHub and also R and R Studio can recognize and can be used to do a lot of different
things.

The first thing that you want to be
able to do and so it's just a text file that
you're editing.
And the extension for the text file is
.md.
So you're going to create a file that's for example readme.mda that's a markdown file.
The first thing that you're going to do is create headings.
So, for example, if you do the double pound like this, followed by some text it will create a heading for a secondary heading.
So what will, what will happen is if you upload a .md file, say for example to GitHub, if you use two pound signs and then followed by some text.
You'll end up seeing that the get interpreted by GitHub as a heading.
So slightly larger, more bold text. You can also create smaller headings by using a triple ha, or triple pound sign then.
And then typing this is a tertiary heading.
And you'll see that GitHub interprets that
as a slightly smaller heading size.
The other thing that you can do with, Markdown in addition to
typing just plain paragraphs is that you can create lists very easily.
So, for example, if you type, is, this star, and they you type
first item in the list, asterisk, second item in the list, so forth.
You'll get an unordered list, in other words a list
with dots, starting at the beginning, nicely formatted by GitHub.
And so, those are the two basic things that you need to know right now.
You can use headings, and you can use lists to sort of organize your file.
And then you can just type plain paragraphs as well.
If you want to [UNKNOWN](#), know a lot more about markdown, you can try out this link right here or if once you've installed Rstudio, you can actually click the button, there's an MD button right in the middle of the screen, that if you click on that, you'll get a quick guide to markdown.
And so you will don't need R Markdown or any of the more technical details, until you get to reproducible research, but this will be useful, in terms of putting sum into your first few
directories on GitHub.




### Data Science Specialization

* Uses R 
* Nine courses 
* Goes from raw data to data products

$ git remote add origin https://github.com/yourUserNameHere/test-repo.git
$ git clone https://github.com/yourUserNameHere/repoNameHere.git