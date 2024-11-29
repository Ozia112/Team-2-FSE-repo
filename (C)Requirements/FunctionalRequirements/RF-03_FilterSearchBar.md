
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

# Interface improvements

## Prototype 1
![image](https://github.com/user-attachments/assets/b720c98e-6c2b-42d6-bc92-9efbb98a5242)

## Prototype 2 
![image](https://github.com/user-attachments/assets/300a5bcc-05bd-4528-ac29-0b535bf54fb1)

### Prototype 1
In the first prototype, several issues were identified that limited the functionality and user experience:

- **Design limitation**: The initial design only allowed users to navigate to the notifications section without displaying any additional content.  
- **Static interaction**: There was no dynamic response or feedback from the system when using the filtering or search bar options.  

### Prototype 2
The second prototype addressed the issues found in the first version, introducing significant improvements:

- **Enhanced filtering system**: Clicking on the filtering options now presents two distinct choices.  
- **Dynamic navigation**: Selecting one of the filtering options provides additional related sub-options. Each subsequent click leads to a unique interface tailored to the user's chosen interaction.  
- **Improved interactivity**: The design now ensures that users receive relevant feedback and can explore related content seamlessly.

### Key Differences Between Prototypes
- **Navigation**: The first prototype had a static flow, while the second prototype implemented a more dynamic and interactive experience.  
- **Feedback**: The initial version lacked feedback mechanisms, whereas the improved version added responsive interactions based on user input.  
- **Usability**: The second prototype enhanced the user's ability to explore different functionalities, making the interface more intuitive and efficient.  

These changes demonstrate a clear focus on addressing user needs and improving the overall design and usability of the login and search bar functions.


> Description section written by `TM-04`  
> Artifacts section written by `TM-02`  
> Interface improvements section written by `TM-03`
