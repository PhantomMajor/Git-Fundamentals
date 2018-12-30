# Why Version Control Matters #

1. Track all the changes.
    Prototyping
2. Can't keep multiple copies of the files.
3. A lot of projects will have dependent files.
4. Features of one file mmight be dependent on the features of the other.
    To change one feature, rewrite on the copies of all the dependent files
5. Can't keep copies of entire folders. 
    Takes up a lot of disk space
6. Two or more devs on one task... BIG problem
    Merging the changes to one version for the client

_Version Control System_ manages and controls all this automatically.

# How it Works #

Revision control. Version Control. Source Control

Repositiory -- Collection of all the version of the particular project, along with some special information like:
    - What order did the changes occur in.
    - A description of each change.
    - Who is responsible for each change.

Version control Systems do not keep a track of teh changes automatically. We have to _explictly_ tell them when a version is finished so that it will track them. 

The act of telling a VCS that the version is finished is called __comitting__. Changes are committed in the repository. Because of this, versions are refered to as __commits__.

VCS also provides us with tools that will allow us to browse the project history.


# Why Git? #

Git is a _distributed_ VCS. There is no central repo. Everyone has their own repo. Therefore interaction is possible even without a network connection.

Interactions are therefore fast and collaboration easy.
