---
layout: page
title: Lectures and Assignments
---

[Lectures](http://nbviewer.ipython.org/github/jklymak/Phy411/tree/master/lectures/)

Each "Week" has a lecture associated with it. 

[Assignments](http://nbviewer.ipython.org/github/jklymak/Phy411/tree/master/assigments/)

There will be approximately weekly assignments, due the Wed after the end of the week, so Assignment 1 is due 17 Sep at 17:00 local time, Assignment 2 due 24 Sep, etc.  Assignments are of equal weight, and are 55% of your grade.  Late assignments are penalized 10% per day, fractions rounded up, weekends included. 

Assignments are due by email, subject must say: `Phy411 Assignment 01`, `Phy411 Assignment 02`, etc.  The email can contain a PDF of your assignment, or it can contain a link to your notebook if you keep the notebook on github or wakari.  

## Sharing Notebooks on Github ##

If you are writing notebooks on your machine, its pretty easy to share them by keeping them under version control on [github][github].  

  - Sign up for [github][github]
  - Create a repository on [github][github].  i.e. `Phy411Assignments`
  - On your local machine, use a GUI github client, or from the command prompt type 
  
```
% git clone https://github.com/yourname/Phy411Assignments.git
```

and you should get a copy of the directory in a level below your present one.
  
  - Copy your notebook into the new directory (or start editing a new one there)
  - Add your file (only need to do once:)
  
```
% git add Assignment01.ipynb
```

  - Commit your changes:
  
```
% git commit -a -m "added Assignment01.ipynb"
```

  - Push your changes to github: you will likely need your password.

```
% git push origin master
```

  - now you should be able to go to github and navigate to your new `Phy411Assignments/Assignment01.ipynb`.  Do so, and copy the link.  It will be something like
`https://github.com/yourname/Phy411Assignments/blob/master/Assignment01.ipynb`

  - go to [nbviewer.ipython.org](nbviewer.ipython.org) and enter the link above.  You should now see your Assignment in the nbviewer.  

  - copy the nbviewer link and send it to me.  You can just send me the tree version, which for the above would look like:

```
http://nbviewer.ipython.org/github/yourname/Phy411Assignments/tree/master/
```

I know that seems like a lot, but really, it is great to store things on [github][github] anyways as a back up to make sure your work is safe.  After that, its very easy to figure out the pathnames to send me for nbviewer, so its not as big a chore as this all sounds.  You simply have to remember to `add` (once), `commit`, and `push` your work.

[github]: https://github.com





