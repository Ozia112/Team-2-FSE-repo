# Process Description (FIS Project Stage 1)
## Introduction
The following document will break down the general project activities and their expected outcomes. It will also provide a detailed explanation of how the iterations for the second stage of the project will work, special cases for certain tasks, and the protocols for correct naming and documentation of participation in the project.

## ID’s Assignation.
The assignment of Identifiers for team members will be implemented to increase the flexibility of team job changes in case a member is absent or previously assigned roles change in the next stages of the project. The enumeration is assigned in order of integration into the team at the time it was formed. At some point in the process, members may change their identifier with prior notice in case it is needed due to an emergency.
The assignment with team members (09/21/2024) is as follows:
- `TM-01`: Isaac Ortiz
- `TM-02`: Paola Parra
- `TM-03`: Rolando Cabrera
- `TM-04`: Álvaro Pantoja
- `TM-05`: Cristofer Barrera
- `TM-06`: Adrián Rosado
- `TM-07`: Alexander Castañeda
### Roles and Responsibilities
- `Project Manager`: _Responsible for the overall management of the project, in charge of distributing tasks across the different stages among all members, taking into account their skills._
- `Repository Manager`: _Responsible for organizing the project to improve readability and ensuring that repository navigation is user-friendly for those visiting the directory._
- `Log Keeper`: _Responsible for recording and organizing the logs of all project members in a readable and easy-to-analyze format to enable quick and efficient data analysis._
- `Task Owner`: _Members who have been assigned a specific project task._
- `Assistant`: _Members assigned to assist the task owner in solving the issues related to the specific task._
---
## Workflow
### Iterations
The workflow will be structured in six-day iterations (except in specific cases), during which the different activities have been distributed. At the beginning of each iteration, a general report will be made on all changes implemented, objectives achieved, possible corrections, and the resolution of any questions the team may have regarding the previous iteration or upcoming activities.  

![Iterations](https://github.com/Ozia112/Team-2-FSE-repo/blob/TM-01-Branch/assets/Stage2/(D)Process/iterations_process.png)

### Protocols 
The work protocols will be managed in brief iterations that will be reviewed every two to three days, except in emergency cases where immediate intervention is required for a specific task.
#### Rules
- Create and move your tasks in the GitHub project section as required.
- At the bottom of the document, write the name of the person who created it with the following statement: "> Written by `TM-00`". If the file was modified by an assistant, add a sub-quote: "Assistant: `TM-00`."
- After completing a commit on a task, immediately create a pull request (PR) to update the repository as soon as possible. (Changes will only be reviewed in the Stage 2 branch.)
-	Each folder must contain a README.md file, serving as an explanatory text of the folder and its table of contents to allow for smoother navigation for the reader.
##### Naming
- Name your files using PascalCase (ExampleFileName)
- The images used for tasks should be stored in specific folders depending on which file they are used in, following this structure: "assets/Stage2/ExampleTask/".
- Activity folders now will be named with their ID in parentheses followed by their category. Example: (D)Process.
-	Images should always be saved in the folder named assets, and they must have descriptive names in English to ensure image references in markdown files are well-structured.
- File names must always be written in English. If the task was originally written in Spanish, this should be specified next to the file name with “(esp)” beside the file version. The final file must be entirely in English, and it does not need to specify the language as it is assumed to be in English.
### Meetings 
At the start of each iteration, a personal meeting will be scheduled to discuss project planning. Preferably, it will be scheduled for Mondays. In the event of any circumstances preventing this, the meeting will be held via video call or rescheduled as soon as possible. The same applies to the end of each iteration, with meetings held in person on Fridays whenever possible, and in case of an emergency, via video call.
#### Possible dates for in-person/video call meetings:
- Monday, October 7 (Planning) / Friday, October 11 (Review)
- Monday, October 14 (Planning) / Friday, October 18
- Sunday, October 20 (Short iteration planning) / Tuesday, October 22 (Short iteration review and reassessment for project reassignment)

### Logs 
- The general log for both video call and in-person meetings will continue to be recorded by ``TM-03`` and now also by ``TM-07`` simultaneously.
- Time and record the duration spent on a specific task.
- Report any changes made in a personal log within the folder where the assigned activity is performed. The  file name should follow this structure: [.] Team ID [_] Binnacle. Example: .TM-01_Binnacle.
- Activity reports must include the following information:
   - Activity ID
   - Description of changes/tasks completed
   - Date
   - Duration of the activity
   - Example:
>---   
>### 06/10/2024 
   > D2.0 Creation of the file and sections: Introduction, Project (GitHub), Milanote, Task Assignment, Timeline, and Task List. Time lapsed: 06:30:50
   > 
>---




### Repository changes
Once progress has been made on the work in the repository, a commit should be made, and the change should be applied to the main branch of the corresponding project stage (FIS-Project-Stage-1) through the creation of a pull request, where the changes to be implemented can be reviewed.
Each day, before starting the assigned activities, the team member must create a pull request to copy the files from the main project branch into their personal branch to work with the updated files and avoid accidental overwriting or duplication of unwanted files.
Below are the steps to follow to create the mentioned pull requests:
##
![Pull request step1](https://github.com/Ozia112/Team-2-FSE-repo/blob/TM-01-Branch/assets/Stage1/click_in_the_pull_request_section.png)
> Click in the pull request section
##
![Pull request step2](https://github.com/Ozia112/Team-2-FSE-repo/blob/TM-01-Branch/assets/Stage1/create_pull_request.png)
> Click in the create new pull request button
##
![Compare branchs](https://github.com/Ozia112/Team-2-FSE-repo/blob/TM-01-Branch/assets/Stage1/compare_branches_reference.png)

> Make a comparision between the two branches to create a copy

### Workflow protocol
The workflow follows simple Git protocols for faster work, so no other person is needed to confirm changes to the main branch. All changes must be stored in different files for modular management, as outlined in the following diagram:
![Flujo de trbajo](https://github.com/Ozia112/Team-2-FSE-repo/blob/TM-01-Branch/assets/Stage1/work_flow_graph.png)
### Branch Creation
To be able to work in an orderly manner on the project, the creation of personal branches for each team member is completely necessary. The creation of these branches must follow rules and protocols so that order is maintained in the course of the work.
#### Branch Rules:
>    - Branch names should be composed of the team member’s ID followed by the word “Branch”. Example: TM-01-Branch
>    - The source Branch for the personal Branch it must be the main branch of the project stage (FIS-Project-Stage-1)
>    - In your Branch you need to create a directory for your work with the main category of your task followed by the word “_task”, for example if your task assigned is BA1.1 you need to create a directory named as B_task
>    -	Team members must keep their personal branches organized and clean, with their corresponding files placed in their assigned folders for images and task categories.
>    - The usage of assets like images need to be upload in the folder named “assets”  

Time lapsed: 02:34:26 07/10/2024
>Written by `TM-01`.
