README.md
Test data for the 'End Goal' goal management approach across various 
language imlementations.

# Overview
The repo holds test data for the 'End Goal' goal management approach.
Ideally the various versions of the software in different languages use the 
same structure, or at least have compatible rules for importing and exporting
to a neutral structure.

Work is needed to update the variations below to match the eng structure, 
which is currently the latest.

In particular, the Rust eng version uses a Mongo sty;le Object ID for the
Goal Id, Objective IDF, and task Id.  Nothing adequately supports the 
optional layer of "SubObjective" in the hierarchy.  

# Rust eng command line

# iOS End Goal
The swift version might not be using a flat OID scheme to generate IDs.

## In this scheme:
SubObjectives are not supported.
Attributes use camel case instead of snake case names 
 - (todoMaxTask: vs todo_max_tasks:)


# React Task Blotter 
The JS version uses a hierarchical path style ID where the task ID include the
parent objective ID and Goal ID.


Removing this structure will make building the Python file system representation
a little harder. but it is worth ist to simplify ID creation on the other
platforms.

## In this scheme:
EffortDomain is called UserDomainT
 - uses an attribute sprint_max_tasks instead of todo_max_tasks:
Goals are called Endeavors.
Objectives are called stories.
SubObjectives are not supported.
Tasks are included. 
The in_progress value in the status enum uses a space instead of an underscore.


# Python Tlog command line
Has a very human editable markdown based syntax that is great for creating tasks
in file.
## In this scheme:
Goals are called Endeavors.
Objectives are called stories.
SubObjectives are not supported.
Tasks are included. 
The in_progress value in the status enum uses a space instead of an underscore.
