git
===

Website links
-------------

* https://github.com/
* The Pro Git book is available `here <https://git-scm.com/book>`_!

Useful Commands
---------------

add everything to the commit (including new file and files that were deleted):
::

  git add -A

commit all of the changes:
::

  git commit -m "some message about what you did"

push to remote account:
::

  git push origin master

view current tags:
::

  git tag

making a new tag:
::

  git tag -a V0.0.1 -m " new version 0.0.1"

committing a tag:
::

  git push origin master --tags

checkout a tag:
::

  git checkout -b [branchname] [tagname]

see which branch you are on:
::

  git branch

connecting to github:
::

   git remote add origin git@github.com:username/new_repo

* making a branch `look here <https://help.github.com/articles/fork-a-repo/>`_

Then make a `new repository <https://github.com/new>`_ using the interweb

* Check out `this link  <http://kbroman.org/github_tutorial/pages/init.html>`_ for more info.

Caching your github password:
::

  git config --global credential.helper 'cache --timeout=3600'
  # Set the cache to timeout after 1 hour (setting is in seconds)

Another way to connect to github it using ssh
----------------------------------------------
Initially the error was:
::

  febbo@febbo-HP-ZBook-17-G2:~/.julia/v0.5/VehicleModels$ git push origin master
  Permission denied (publickey).
  fatal: Could not read from remote repository.

  Please make sure you have the correct access rights
  and the repository exists.

* This was obtained when initially setting up the git repositories in julia after cloning a package and trying to push modifications back up to the remote repository.
* Information on this can be founds `at <http://docs.julialang.org/en/release-0.5/manual/packages/>`_ , or by following the two steps a fix may be obtained:

  1. Make an ssh key and add it to github, `following  <https://github.com/settings/ssh>`_.

  2. Check out `this <https://linux.die.net/man/1/ssh-agent>`_, or use the following commands:

    * A program to hold private keys for public authentication.

      type:
      ::

        ssh-agent

    * Initially the agent does not hold any private keys.

      So run:
      ::

        ssh-add


Mistakes I Made
----------------
* Make sure that you are working on the master branch!

    * Do not check out a tag and start making changes only to realize that you are not on the master branch!


* Trying to connect to github using ssh

  1) Create a github repository, with the name ( for example: huckl3b3rry87/LiDAR.jl )


  2) Then

  Type this in the terminal:
  ::

    febbo@febbo-HP-ZBook-17-G2:~/.julia/v0.5/LiDAR$ git remote add origin git@github.com:huckl3b3rry87/LiDAR.jl

  3) Then

  Try this:
  ::

    febbo@febbo-HP-ZBook-17-G2:~/.julia/v0.5/LiDAR$ git pull master

  4) Next

  Get this:
  ::

    fatal: 'master' does not appear to be a git repository
    fatal: Could not read from remote repository.

    Please make sure you have the correct access rights
    and the repository exists.

  Next we are going to `test the ssh connection <https://help.github.com/articles/testing-your-ssh-connection/>`_

  5) Attempt to ssh to GitHub
  By typing:
  ::

    febbo@febbo-HP-ZBook-17-G2:~/.julia/v0.5/LiDAR$ ssh -T git@github.com
    Hi huckl3b3rry87! You've successfully authenticated, but GitHub does not provide shell access.

  6) realize that you messed up
  by typing:
  ::

    git pull master

  and not:
  ::

    git pull origin master
