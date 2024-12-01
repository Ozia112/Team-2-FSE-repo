# Action Bar

- A bar containing a set of buttons that allow quick navigation through the platform.

## Description
- The action bar must have three main buttons that act as positions or states within the application.
- Only one button can be pressed at a time, and these buttons remain highlighted as long as the user is within that `action`.
- The actions are defined as the positions the application can be in. There are three in total:
  - Notifications
  - Home Page
  - Add Platform

### Notifications
- The user can access this section through the left button on the action bar.
- In the `notifications` section, the user can see different `items` containing relevant information. These `items` are divided into three types:
  - `Task`
  - `Exam`
  - `News`  
  Each notification `item` includes:
    - Platform name
    - Start date
    - Expiration date (except for news, which do not have an expiration date)
    - Course name
    - Teacher name
    - A label indicating the type of notification
- By pressing the `view` option on the notification item, the user will be redirected to the specified `platform`, `course`, and `activity/news` in the notification.
- These notifications can be easily searched through [`RF-03`], the application's search and filter system.

### Home
- The user can access this section through the central button.
- In this section, the items of type: `item.platform` and `item.course` are displayed.  
#### For platform-type items:
  - :one: You can access the platforms you have previously registered by clicking or pressing them.
  - :two: The number of notifications contained in the platforms will be indicated and colored depending on the quantity:
    - `Green`: This color indicates that there are no pending notifications on the platform, low alert.
    - `Blue`: This color indicates a medium number of notifications, 1-3, medium alert.
    - `Red`: This color indicates the highest number of notifications, high alert.
    >*The colors can be extracted from the design guide in the documentation*
  - :three: In the upper left corner, information about the platform's status will be displayed:
    - `Green`: Online, the platform is functioning correctly and can be accessed without problems.
    - `Yellow`: The platform is under maintenance, it cannot be accessed because it is being worked on. Normally, students are notified before this happens.
    - `Orange`: The platform is out of service due to an unspecified problem. The user cannot access the platform because it is out of service.
     >*The colors can be extracted from the design guide in the documentation*
  - :four: The platform's name is displayed.
  - :five: The `item.platform` can be of two types:  
    - `Based.moodle`: This is the standard platform type, and all the information will be displayed.  
    - `NonBased.moodle`: This type of platform cannot display the status of the platform or the number of notifications. It can only redirect the user to the specified URL.  
    
#### For course-type items:
   - :one: The characteristics :two:, :three:, and :five: from `items.platform` are inherited.
   - :two: The course name is displayed.
   - :three: The semester number of the course is displayed.
   - The name of the professor in charge of the course is displayed.
- The items can be searched and filtered as specified in [`RF-03`].

#### Modes
The home section is divided into two modes: `course.mode` and `platform.mode`. Depending on which is activated, specific items will be displayed. By default, the courses mode will be shown whenever the user clicks on the home button. If the user wants to view the platforms, they must press the switch-type button to change to platform mode.

- The default mode can be changed in the settings menu. By default, this option will be set to course mode.
- When the user adds a platform through the add platform section, they will be redirected to the Home section in `platform.mode`.
#### Settings Menu
This menu can be accessed through the user icon in the application. The available options are:
- Default mode, and
- Log out.

### Add Platform
- The user can access this section through the right button on the action bar.
- In this section, platforms can be added by entering the URL in a text field indicated on the application. The application will detect the platform and create the item that will be displayed in the home page section in the platform mode.
- The platform will use the credentials previously entered when the user first logged in (`institutional email`). If the entered platform requires a username and password different from the institutional email, the application will ask for the email or username and password to log in, and if necessary, a captcha.
- The first time the user logs into the application, the add platform section will be displayed, and the others will be locked until the process of adding a platform is completed.
## UADY HUB's data behavior:
```mermaid
graph TD
    A[User enters email and password] --> B[Log in]
    B --> C[Institutional Email] --> G
    B --> C2[Password] --> G
    B --> D[Create platform item]
    D --> E[Request school platform URL]
    E --> F[User enters URL]
    F --> G[Use email and password on the platform]
    G --> H[Captcha, if necessary]
    H --> I[URL]
    I --> J[Fetch platform data]
    J --> K[Status: <br/>- Online<br/>- Maintenance<br/>- Offline]
    J --> K2[Platform name] --> L
    J --> K3[Enrolled courses] --> L
    J --> K4[Number of notifications] --> L
    
    K --> L[Display in items.platform]
    J --> 
    L --> M[Display in items.courses]
    subgraph Database
        C
        C2
        I
        
        K
        K2
        K3
        K4
    end
```
## ER graph
``` mermaid
erDiagram
    USER {
        string email
        string password
    }
    PLATFORM_ITEM {
        string url
        string platform_name
        string status
        int total_notifications
        int total_courses
    }
    COURSE {
        string course_name
        string platform_name
        string professor_name
        int notifications
        string semester
    }
    TASK {
        string description
        date due_date
    }
    EXAM {
        string description
        date exam_date
    }
    NEWS {
        string title
        string content
        date date
    }
    USER ||--o{ PLATFORM_ITEM : creates
    PLATFORM_ITEM ||--o{ COURSE : contains
    PLATFORM_ITEM ||--o{ TASK : contains
    PLATFORM_ITEM ||--o{ EXAM : contains
    PLATFORM_ITEM ||--o{ NEWS : contains
```
## Artifacts 
### User Story:
As a user, I want to quickly access different sections of the application through the Activity Bar to improve my workflow.


### Acceptance Criteria:
  - The Activity Bar must contain icons for the main sections of the application.

  - Clicking on an icon should change the view to that section.

### Use Case:

`User`: Person using the application and navigating through the Activity Bar.

#### Scenarios:

- **Scenario 1**: Successful Navigation

  - `Context`: The user is on the main screen of the application.

  - `Actions`:

    - The user clicks on an icon in the Activity Bar.

  - `Expected Result`: The application changes to the corresponding view, and the user can interact with that section.

> Description section written by `TM-01`  
> Artifacts section written by `TM-02`

[`RF-03`]: https://github.com/Ozia112/Team-2-FSE-repo/blob/Stage-3/Requirements/(C)Requirements/FunctionalRequirements/RF-03_FilterSearchBar.md
