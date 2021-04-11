# Pop

Pop removes a single stashed state from the stash list and applies it on top of the current working tree state \(for example: do the inverse operation of Git stash save\). The working directory must match the index. For simplicity sake, ZIGI validates that the current workspace is clean before performing a stash pop. This is because numerous conflicts could arise that would require manual intervention and the authors were unable to find a reliable methodology to resolve those conflicts programmatically.

*NEXT TOPIC*: [Pop Conflict Resolution](r_pop_conflict_resolution.md).

-   **[Pop Conflict Resolution](r_pop_conflict_resolution.md)**  


**Parent topic:**[Stash List \(STASHL\) Command](r_stash_list.md)

