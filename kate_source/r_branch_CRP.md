# Branch

Branch creates and checks out a new branch starting from the commit at which the stash was originally created and then applies the changes recorded in the stash to the new working tree and index. If that succeeds, it then drops the stash. This is useful if the branch on which you ran git stash save has changed enough that git stash apply fails due to conflicts. Since the stash entry is applied on top of the commit that was HEAD at the time git stash was run, it restores the originally stashed state with no conflicts.

*NEXT TOPIC*: [Diff](r_diff.md)

**Parent topic:**[Stash List \(STASHL\) Command](r_stash_list.md)

