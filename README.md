README.md
The repo holds test data for the 'End Goal' goal managemet approach.
Ideailly the various versions of the software in different laguages use the 
same structure, or at least have compatable rules for importig and exporting
to a neutral strucure.

Work is needed to update the variations below to match the eng structure, 
which is curently he latest.

In particular, the Rust eng version uses a Mongo sty;le Object ID for the
Goal Id, Objective IDF, and task Id.  Nothing adequately supports the 
optional layer of "SubObjective" in the hierachy.  

# Rust eng command line

# iOS End Goal
The swift version might not be using a flat OID scheme to generate IDs.

## In this scheme:
Subobjectives are not supported.
Attributes use camel cas instead of snake case names 
 - (todoMaxTask: vs todo_max_tasks:)


# React Task Blotter 
The JS version uses a hieracical path style ID where the task ID include the
parent objective ID and Goal ID.


Removing this structure will make building the Python file system representation
a little harder. but it is worth ist to simplify ID creation on the other
platforms.

## In this scheme:
EffortDomain is called UserDomainT
 - uses an attribute sprint_max_tasks instead of todo_max_tasks:
Goals are called Endeavors.
Objectives are called stories.
Subobjectives are not supported.
Tasks are included. 
the in_progress value in the status enum uses a space instead of an underscore.


# Python Tlog command line
Has a very human editable markdown based syntac that ia great for creating tasks
in file.
## In this scheme:
Goals are called Endeavors.
Objectives are called stories.
Subobjectives are not supported.
Tasks are included. 
the in_progress value in the status enum uses a space instead of an underscore.


