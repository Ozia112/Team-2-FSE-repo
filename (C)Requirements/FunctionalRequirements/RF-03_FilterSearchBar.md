
# Search and filter bar 

- An element that is used for searching and a button with filtering options

## Description

- The search element has a text field, an A-Z button and a filtering button, it is located in the notifications section, it can be viewed at the top by entering the notification section

- When you click on the search text field, a command will open where as you type, the most similar thing to what you wrote will appear, next to it there is an A-Z button that allows you to enter the data alphabetically

- When you click on the filter button, a command will open that will cover the search text field, where two icons will appear, in the first icon there is “all courses” and in the second there is “all activities” and the filter button is still maintained so that when you click again that section closes

- When you click on the “all courses” icon, a command opens that displays some items that are the subjects in which you are registered, these items depend on their number depending on how many subjects have registered to close this section an “x” button opens to close the icon command

- Clicking on the “all activities” icon also opens a command that displays some items but these are ‘tasks’,  ‘exams’ and ‘news’ these are general and to close the command the “x” button also appears in the corner to close the icon command

- The use of the icons can be combined, you can grab a task and specify which course it is from and so on with the other variants, when using any of them the filtering of the choice is done to find what you are looking for faster

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
