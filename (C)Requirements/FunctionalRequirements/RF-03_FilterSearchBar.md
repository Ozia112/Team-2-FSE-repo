
# Search and filter bar

- A search element and a button with filtering options

## Description

- The search element has a text field and a filtering button and is located right in the middle

- When you click on the search text field, a command will open where, as you type, the most similar thing to what you wrote will appear, just as at the top, three icons of course, platform and teachers will appear. You can click on it so that when you continue searching, it will focus on those three specific ones or you can use the text field and it will appear in general for any of the three

- When you click on the filter button, a command will open where an A-Z icon will appear, another date icon and two buttons, one for the course and another for the platform. You can filter in alphabetical order or by date and in those you can search for courses or platforms.

- The filter button can also be found in the home section, you go to notifications and there, once inside, the button appears where, likewise, when you click on it, it shows you an A-Z icon, another for the date, another for notifications and four buttons, one for the course, another for the platform, another for the teacher, another for the type and another for the name. You can activate several of these buttons at once and when you type, it shows you the fastest results.

- When using the search text field or the filter button after clicking, it will redirect you to what you have searched for or the options you have wanted to filter.


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
``` mermaid
usecaseDiagram
%% Diagrama de casos de uso para el login de Uadyhub
%% Usa este código en un editor compatible con Mermaid
---
title: Casos de Uso - Login Uadyhub
---

%% Define el diagrama de casos de uso
usecaseDiagram
    actor Usuario as "Usuario"

    rectangle Uadyhub {
        usecase UC1 as "Ingresar correo institucional"
        usecase UC2 as "Introducir contraseña"
        usecase UC3 as "Pulsar botón de log in"
        usecase UC4 as "Activar checkbox para guardar sesión"
        usecase UC5 as "Desplegar teclado al tocar un campo"
        usecase UC6 as "Autenticar usuario con credenciales"
    }

    %% Relaciones del actor con los casos de uso
    Usuario --> UC1 : "Toca el campo de texto"
    Usuario --> UC2 : "Introduce contraseña"
    Usuario --> UC3 : "Pulsa botón de log in"
    Usuario --> UC4 : "(Opcional) Marca/desmarca checkbox"

    %% Relaciones entre casos de uso
    UC1 --> UC5 : "Muestra teclado"
    UC3 --> UC6 : "Valida credenciales"
```