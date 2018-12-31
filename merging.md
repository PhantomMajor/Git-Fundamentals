[Go back to contents](README.md/#Table-of-Contents)

# Merging #

It is the reverse of branching. Merging combines the two separate timelines into the master branch.

It also combines each of their individual committs into one _coehesive_ timeline.

- The committs have to be combined in a proper order.
- If a file has been changed in both the branches:
    + It is called a _merge conflict_
    + Decision has to be made as to which changes will be kept in the final version.

Git merges intelligently, resolving as many conflicts as it can, itself.


## Basic Merging ##

First, get in the master branch.
Second, to merge:
```shell
$ git merge branch_that_has_to_be_merged
```

If there is a merge conflict (i.e. the same file has been edited in both the branches), then:

Auto-merging is done by Git automatically, if the conflict is not on the same lines.


## Merge Conflicts ##

When there is a change in the same line.

**Resolving a merge conflict-**

Easiest way to resolve a merge conflict is to edit the conflicted file.
After opening the conflicting file in the text editor, punctuations (called the _conflict markers_) are added automatically.

It looks like:

```

<<<<<< HEAD
foofoofoofoofoo
======
fiifiifiifiifii
>>>>>> branch_name
```

- The angled brackets show that this whole area is one conflict.
- The row of equal signs shows us the two versions (and hence lets us compare the two versions)
- The labels to the right of the angle brackets show the branch to which it belongs.

Case 1: If we simply remove all the conflict markers, then we can keep both the changes:
```
foofoofoofoofoo
fiifiifiifiifii
```

Case 2: We can resolve it by incorporating both the changes into some manual cahnge:
```
foifoifoifoifoi
```

We now have to add the merged file in the staging area, and then commit the merge manually!
