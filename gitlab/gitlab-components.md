# Projects, Groups, Issues, Branches, and Merge Requests

## Groups and Projects

`Account` is like a tree root.

`Group` is like a non-leaf element in the tree.

`Project` is like a leaf element in the tree.

`Project` = a Git repository in which a code is stored.

`Group` = a collection of (software-related or non-software-related) projects or other (sub)groups.

Up to 20 levels of subgroups within a group can be used.

For groups, you can:
- invite other GitLab users to be members of a group;
- assign them a role within that group;
- grant a user, group, or role permission to view or edit any projects within that group.

## GitLab Issues

`Issue` = like a story or ticket assigned to a project.

An `issue` can also contain `labels` and `weight` (metric like story points).  

`Scoped labels` are mutually exclusive and marked with double colons `::`. 
An example could be either `Status::Healthy` or `Status::At Risk` or something else. 
That means that an issue cannot have both these scoped labels.

`Due date` can be, for example, due in 3 days, although `weight` can be 3 days. 

## Merge Requests (MRs)

`Merge requests` are a concept that is specific to GitLab and not to Git.

Create a branch in GitLab GUI: 
- `Repository` (left-hand navigation pane) -> 
- `Branches` (left-hand navigation pane) ->
- `New Branch` (top-right button) ->
- `Create Branch` (button).

Commit in GitLab GUI: 
- `Repository` (left-hand navigation pane) -> 
- `Files` (left-hand navigation pane) -> 
- Branch name (dropdown) -> 
- File to edit -> 
- `Edit in Web IDE` to open an in-browser ->
- Make changes ...
