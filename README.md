# IO-PEOPLE Documentation

## 1. Apps: UI

Describes the front-end code for rendering various routes and styles across desktop and mobile devices.

### Desktop
The desktop application contains the following routes:
- **`/`**:
    - Home Page
    - Shows all the People
    - Search feature using people name
    - Filter feature using joining date, champion, domain, job title, leadership title and status
  
- **`/<person_id>`**:
    - People Basic info
    - Shows details of people like Manager, Job title, Email, etc
  
- **`/<person_id>/professional`**: 
    - People Professional info
    - Shows details of people like Work experience, Education, Certificate

- **`/<person_id>/projects`**: 
    - Project of a particular user
    - Shows details of people like Work experience, Education, Certificate

- **`?page=0&view=avatar`**: 
    - Shows people in table ui

- **`?page=0&view=table`**:
    - Shows people in box ui with image

### Mobile
The mobile application contains the following routes:

- **`/`**:
    - Home Page
    - Shows all the People
    - Search feature using people name
    - Filter feature using joining date, champion, domain, job title, leadership title and status

- **`/<person_id>`**:
    - People Basic info
    - Shows details of people like Manager, Job title, Email, etc

- **`/<person_id>/professional`**:
    - People Professional info
    - Shows details of people like Work experience, Education, Certificate

- **`/<person_id>/projects`**:
    - Project of a particular user
    - Shows details of people like Work experience, Education, Certificate

- **`?page=0&view=avatar`**:
    - Shows people in table ui

- **`?page=0&view=table`**:
    - Shows people in box ui with image

## 2. Assets
Stores files and React projects.
- **Blog.svg**
- **Facebook.svg**
- **index.js**
- **Instagram.svg**
- **LinkedIn.svg**
- **Website.svg**
- **X.svg**
- **Youtube.svg**

## 3. CustomRoles
Used to define and manage custom roles.
- **index.js**: Used for storing Admin roles

## 4. Facets
Generates computed static data from the database, which is then used in filters.

**-- EMPTY --**

## 5. Foreign_Field
Handles background processes to update source field details in the target.

**-- EMPTY --**

## 6. Models
APIs which interact with services and schema for defining the model structure.

- **Models along with services**:
    - `certificates`
        - mongodb
    - `education`
        - mongodb
    - `link`
        - mongodb
        - elasticsearch
        - search
    - `people`
        - mongodb
        - elasticsearch
        - search
    - `work_experience`
        - mongodb
        - elasticsearch
        - search


- **Models along with apis**:
    - `certificates`
        - **certificate.js**: Read one certificate using _id
        - **certificates.js**: Read all certificate of person using personId
        - **create_certificate.js**: Creates certificate and notify the user on email
        - **delete_certificate.js**: Delete one certificate using _id
        - **update_certificate.js**: Update one certificate using _id and notify the user on email
    - `education`
        - **education.js**: Read one education using _id
        - **educations.js**: Read all education of person using personId
        - **create_education.js**: Creates education and notify the user on email
        - **delete_education.js**: Delete one education using _id
        - **update_education.js**: Update one education using _id and notify the user on email
    - `link`
        - **create.js**: Create link
        - **delete.js**: Delete one link using _id
        - **read_all.js**: Read all link of person using personId
        - **read_one.js**: Read one link using _id
        - **update.js**: Update one link using _id
    - `people`
        - **people_search**: Used for searching, sorting and querying people
        - **create_person.js**: create a person and add it in employee context
        - **delete_person.js**: Delete one person using _id
        - **existing_user.js**: Checks for existing user using personId
        - **people_id_by_email.js**: Get all the person using people email ids
        - **person_attendance_percent.js**: Calculate the percentage of a person
        - **person.js**: Read one person using _id
        - **update_person.js**: Update one person using _id
    - `work_experience`
        - **read_one.js**: Read one work experience using _id
        - **read_all.js**: Read all work experience of person using personId
        - **create.js**: Creates work experience and notify the user on email
        - **delete.js**: Delete one work experience using _id
        - **update.js**: Update one work experience using _id and notify the user on email


## 7. Settings
Stores project configuration settings.
- **checkin_model_id.js**
- **domain.js**
- **files_api.js**
- **holiday_model_id.js**
- **links.js**
- **projects_app_id.js**
- **timeoff_model_id.js**
- **to_users.js**


## 8. Statics
Stores static files that can be modified via APIs.
- **employeeId.js**

## 9. Workflows
Handles processes running in the background.

**-- EMPTY --**