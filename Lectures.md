---
layout: page
title: Lectures and Assignments
---

# Lectures

[Lectures](http://nbviewer.ipython.org/github/jklymak/Phy411/tree/master/lectures/)

Each "Week" has a lecture associated with it. 

# Assignments
[Assignments](https://github.com/jklymak/Phy411/tree/master/release/)

There will be approximately weekly assignments, due the Wed after the end of the week, so Assignment 1 is due Wed. 23 Sep at 17:00 local time, Assignment 2 due 30 Sep, etc.  Assignments are of equal weight, and are 55% of your grade.  Late assignments are penalized 10% per day, partial days rounded up, weekends included. 

Assignments are due by email, subject *must* say: `Phy411 Assignment 01`, `Phy411 Assignment 02`, etc.  The email can contain a PDF of your assignment, or it can contain a link to your notebook if you keep the notebook on github or wakari.  

## Getting the Assignments

### Use the github GUI

  - use a webbrowser and go to [https://github.com/jklymak/Phy411/tree/master/release/Assign01/][]
  - right-click or cmd-click on the file you want and `Download Linked File As...` (or whatever the syntax is for your browser).
  
### Get the files directly:

If you have `wget` on your machine (it is available as freeware on most operating systems), you can do:

  ``` wget https://github.com/jklymak/Phy411/raw/master/release/Assign01/Assignment-01.ipynb```

If you have `curl`

```curl -L "https://github.com/jklymak/Phy411/raw/master/release/Assign01/Assignment-01.ipynb" > Assignment-01.ipynb```


## Sharing Your Assignment on Github ##

If you are writing notebooks on your machine, its pretty easy to share them by keeping them under version control on [github][github].  

  - Sign up for [github][github]
  - Create a repository on [github][github].  i.e. `Phy411Assignments`
  - On your local machine, use a GUI github client, or from the command prompt type 
  
```
% git clone https://github.com/yourname/Phy411Assignments.git
```

and you should get a copy of the directory `Phy411Assignments` in a level below your present one.
  
  - Copy your notebook(s) into the new directory (or start editing a new one there)
  - Add your file (only need to do once:)
  
```
% git add Assignment01.ipynb
```

  - Commit your changes (you can do this, and *should* do this often)
  
```
% git commit -a -m "added Assignment01.ipynb"
```

  - Push your changes to github.  This stores it on github as well as your local machine. NOTE: You have not made a backup until you do this, so do this often too!  You will likely need your password:

```
% git push origin master
```

  - now you should be able to go to github and navigate to your new `Phy411Assignments/Assignment01.ipynb`.  Do so, copy the link and send it to me.  Please check your github page and make sure it renders so I can read it!  If you want to make changes before the due date, that is fine, just let me know you have made changes.  No changes allowed after the due date, or you will receive a late penalty as above based on the newest time stamp.  

I know that seems like a lot, but really, it is great to store things on [github][github] anyways as a back up to make sure your work is safe.  After that, its very easy to figure out the pathnames to send me for nbviewer, so its not as big a chore as this all sounds.  You simply have to remember to `add` (once), `commit`, and `push` your work.

[github]: https://github.com





