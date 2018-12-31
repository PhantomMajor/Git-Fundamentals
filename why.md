[Go back to contents](README.md/###Table-of-Contents###)

# Why Version Control Matters #

Version Control is used to manage the different versions and drafts of a document. It involves naming and distinguishing between a series of drafts which lead to a final version.

Track all the changes therefore helps in prototyping.

If there is no automated Version Control:

- Can't keep multiple copies of the files.
- A lot of projects will have dependent files.
- Features of one file mmight be dependent on the features of the other. To change one feature, we will have to rewrite on the copies of all the dependent files
- Can't keep copies of entire folders. It will take up a lot of disk space.
- When there are two or more devs on one task it becomes a BIG problem. Merging the changes to one version for the client also becomes very difficult.

_Version Control System_ manages and controls all this automatically.

# How it Works #

Revision control. Version Control. Source Control. These are all names for the same thing.

__Repositiory__: Collection of all the version of the particular project, along with some special information like:

    - What order did the changes occur in.
    - A description of each change.
    - Who is responsible for each change.

Version Control Systems do not keep a track of the changes automatically. We have to _explictly_ tell them when a version is finished so that it will track them. 

The act of telling a VCS that the version is finished is called __comitting__. Changes are committed in the repository. Because of this, versions are refered to as __commits__.

VCS also provides us with tools that will allow us to browse the project history.


## Why Git? ##

Git is a _distributed_ VCS. There is no central repo. Everyone has their own repo. Therefore interaction is possible even without a network connection.

Interactions are therefore fast and collaboration easy.
