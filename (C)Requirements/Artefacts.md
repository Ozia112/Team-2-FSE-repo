# Artifacts 
## Requirements

#### 1. Functional Requirement: Login

- User Story:
As a registered user, I want to be able to log into the system using my username and password to access my courses and materials.

- Acceptance Criteria:
    -  The system must allow the user to enter their username and password.

    -  The system must verify the user's credentials.

    - If the credentials are valid, the system must redirect the user to the main page.

   -  If the credentials are invalid, the system must display an error message.

- Use Case:

   - User: Person who wants to access the system.

   - Authentication System: Service that verifies the user's credentials.

- Scenario:

**Scenario 1:** Successful Login

Context: The user is on the login page.

Actions:

The user enters their correct username and password.

The user submits the form.

Expected Result: The system verifies the credentials, logs the user in, and redirects them to the main page with a welcome message.


****Scenario 2:**** Incorrect Credentials

Context: The user is on the login page.

Actions:

The user enters an incorrect username and/or password.

The user submits the form.

Expected Result: The system displays an error message indicating the credentials are incorrect.

**Scenario 3**:Password Recovery

Context: The user has forgotten their password.

Actions:

The user selects the "Forgot my password" option.

The system redirects the user to the password recovery page.

The user enters their registered email address.

The system sends a recovery link to the user's email.

Expected Result: The user can follow the recovery process to reset their password and regain access to the system.

#### 2. Functional Requirement: Activity Bar
- User Story:
As a user, I want to quickly access different sections of the application through the Activity Bar to improve my workflow.


- Acceptance Criteria:
    - The Activity Bar must contain icons for the main sections of the application.

    - Clicking on an icon should change the view to that section.

- Use Case:

User: Person using the application and navigating through the Activity Bar.

- Scenario:

**Scenario 1**: Successful Navigation

Context: The user is on the main screen of the application.

Actions:

The user clicks on an icon in the Activity Bar.

Expected Result: The application changes to the corresponding view, and the user can interact with that section.

**Scenario** 2: Icon Customization

Context: The user wants to customize the Activity Bar.

Actions:

The user opens the settings menu of the Activity Bar.

The user drags and drops icons to rearrange them.

The user hides some icons.

Expected Result: The Activity Bar updates according to the user's preferences, and changes are reflected immediately.

Scenario 3: Personalized Activity Bar on Start

Context: The user has previously customized the Activity Bar.

Actions:

The user opens the application.

Expected Result: The Activity Bar displays the icons in the user's customized arrangement.

#### 3. Functional Requirement: Filter Bar
- User Story:
As a user, I want to filter data by date to view only the records from a specific period.

- Acceptance Criteria:
   - The user must be able to select a date range.

   - The system must display only the records within the selected date range.

- Use Case:
Data Filtering with Filter Bar: This use case describes the process by which a user can apply filters to the data displayed in the application using the Filter Bar.

Actors:
User: Person using the application and applying filters through the Filter Bar.

- Scenario:

**Scenario 1**: Date Filtering

Context: The user wants to view records from a specific period.

Actions:

The user selects a date range in the Filter Bar.

The user applies the filter.

Expected Result: The system displays only the records that fall within the selected date range.

**Scenario 2**: Category Filtering

Context: The user wants to view records from a specific category.

Actions:

The user selects one or more categories in the Filter Bar.

The user applies the filter.

Expected Result: The system displays only the records that belong to the selected categories.

**Scenario 3**: No Matching Results

Context: The user applies a filter, but there are no data that match the selected criteria.

Actions:

The user selects filtering criteria.

The user applies the filter.

Expected Result: The system displays a message indicating no results were found.

**Scenario 4**: Modifying Filters

Context: The user wants to change the filtering criteria.

Actions:

The user modifies the filtering criteria in the Filter Bar.

The user applies the new filters.

Expected Result: The system updates the displayed data according to the new filtering criteria.

> Written by `TM-02`
