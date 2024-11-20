
# Search and filter bar 

- A bar with a search icon and a blue button to filter options and courses

## Description

- The search bar has a bar and a blue button for filtering and is located just above the first course that appears

- When you click on the search bar, a command will open where when you write, the most similar thing to what was written will appear. In this bar you can search for teacher names, platform name, course name or search for the assigned task.

- By clicking on the blue filter button the user will be able to organize which courses appear first, they will be able to filter the tasks by date on which they were marked 

- When using the search bar or the filter button, after clicking you will be redirected to what you have searched for or the options you wanted to filter, be it a course, a teacher, view homework assignments

- When using the search bar if you type a course, the full name of the course, what semester it belongs to, and the name of the teacher will appear.

  - If you search for the name of the platform, the full name will appear 

  - If you search for the teacher's name, their full name and the subject they teach will appear.

  # Artifacts 
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
