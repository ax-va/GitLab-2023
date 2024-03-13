## Common

SDLC = software development life cycle

QA = quality assurance

## GitLab Groups and Projects

GitLab account is like a tree root.

GitLab group is like a non-leaf element in the tree.

GitLab project is like a leaf element in the tree.

A GitLab project = a Git repository in which a code is stored.

GitLab group = a collection of GitLab (software-related or non-software-related) projects or other GitLab (sub)groups.

Up to 20 levels of subgroups within a GitLab group can be used.

For groups, you can:
- invite other GitLab users to be members of a group;
- assign them a role within that group;
- grant a user, group, or role permission to view or edit any projects within that group.

## GitLab Issues

Issue = like a story or ticket assigned to a project

An issue can also contain labels and weight (metric like story points).  

Scoped labels are mutually exclusive and marked with double colons `::`. 
An example is `Status::Healthy` and `Status::At Risk`. 
That means that an issue cannot have both these scoped labels.

Due date = ...