# Task Manager
## Overview
This project is a Task Management System designed to allow users to create, edit, view, and manage various types of tasks. The system supports user registration and login, managing personal and shared tasks, and tracking and changing task statuses.

## Task
A task consists of the following attributes:

* id: Unique identifier for the task.
* name: Name of the task.
* due_date (optional): Date by which the task should be completed.
* status: The current status of the task. Possible values are ON_HOLD, IN_PROCESS, DONE, OVERDUE.
* description: Description of the task.

## User
A user of this task management system can be any individual or group needing an effective way to organize and manage their tasks. Users can create, edit, and track various types of tasks, which can be either personal tasks or part of shared projects involving collaboration with other users. Each user has the following attributes:

* username
* password
  
## Dashboard
The dashboard displays the tasks the user wants to complete for the current day (not necessarily due on that day). Users can add or remove tasks from the dashboard. If a task is due on the current day and not completed, it is automatically added to the dashboard upon login. If a task's due date has passed, it is automatically removed from the dashboard upon login.

## User Functionalities
* register: Register a user with a username and password. Registered users are stored in a binary file which acts as a database. The system loads the registered users into memory upon restart.
* login: Log the user into the system.
* add-task: Add a new task with an optional due_date. If the task already exists, an appropriate error message is displayed. All tasks are added with the status ON_HOLD by default.
* update-task-name: Change the name of a task.
* start-task: Mark a specific task as started.
* update-task-description: Change the description of a task.
* remove-task-from-dashboard: Remove a task from the dashboard.
* add-task-to-dashboard: Add a task to the dashboard only if it is not OVERDUE. Adding a task does not change its due date.
* delete-task: Delete a task.
* get-task: Provide information about a task in a human-readable format. If there are multiple tasks with the same name, the command operates on the one with the lowest id.
* list-tasks: Provide information about all tasks for a specific user due on a particular day.
* list-all-tasks: Provide information about all tasks for a specific user.
* list-completed-tasks: Provide information about all completed tasks for a specific user.
* list-dashboard: Provide information about all tasks for the current day.
* finish-task: Mark a specific task as completed.
* logout: Log the user out of the system.
* exit: Terminate the program.

## Collaborations
A collaboration is a shared project where tasks are visible to all participants. Tasks in a collaboration have an additional attribute, assignee, indicating the user responsible for the task. A collaboration consists of:

* name: Name of the collaboration.
* id: Unique identifier for the collaboration.
* creator: User who created the collaboration.
* workgroup: Users working on the tasks within the collaboration.

## Collaboration Functionalities
* add-collaboration: Add a new collaboration.
* delete-collaboration: Delete a collaboration. Only the user who created the collaboration can delete it. Deleting a collaboration automatically removes all tasks within it from the participants' lists.
* list-collaborations: Provide information about all collaborations for the current user, including those they created and those they are part of.
* add-user: Add a user to the collaboration.
* assign-task: Assign an assignee to a task within the collaboration.
* list-tasks: Provide information about all tasks within the collaboration.

## Conclusion
This Task Management System offers comprehensive functionality for managing personal and collaborative tasks. It ensures tasks are efficiently tracked and managed, providing users with an organized and user-friendly platform for their task management needs.
