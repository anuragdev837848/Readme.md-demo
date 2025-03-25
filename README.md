# IO-People Documentation

## Table of Contents
1. [Apps: UI](#1-apps-ui)
   - [Desktop](#desktop)
   - [Mobile](#mobile)
2. [Assets](#2-assets)
3. [CustomRoles](#3-customroles)
4. [Facets](#4-facets)
5. [ForeignField](#5-foreignfield)
6. [Models](#6-models)
   - [Certificates](#certificates)
   - [Education](#education)
   - [Link](#link)
   - [People](#people)
   - [Work Experience](#work-experience)
7. [Settings](#7-settings)
8. [Statics](#8-statics)
9. [Workflows](#9-workflows)

---

## 1. Apps: UI
Describes the code responsible for rendering different routes and styles on both desktop and mobile devices.

### Desktop
The desktop application contains the following routes:
- **`/`**:
  - Home Page.
  - Shows all the People.
  - Search feature using people name.
  - Filter feature using joining date, champion, domain, job title, leadership title, and status.
  
- **`/<person_id>`**:
  - People Basic info.
  - Shows details of people like Manager, Job title, Email, etc.
  
- **`/<person_id>/professional`**: 
  - People Professional info.
  - Shows details of people like Work experience, Education, Certificate.

- **`/<person_id>/projects`**: 
  - Project of a particular user.
  - Shows details of people like Work experience, Education, Certificate.

### Mobile
The mobile application contains the following routes:

**-- No Content Available --**

---

## 2. Assets

Stores files and React projects.
- **Blog.svg**
- **Facebook.svg**
- **Instagram.svg**
- **LinkedIn.svg**
- **Website.svg**
- **X.svg**
- **Youtube.svg**

---

## 3. CustomRoles

Used to define and manage custom roles.
- **Admin**: Stores userIds to grant admin access.

---

## 4. Facets

Generates computed static data from the database, which is then used in filters.

**-- No Content Available --**

---

## 5. ForeignField

Handles background processes to update source field details in the target.

**-- No Content Available --**

---

## 6. Models

APIs which interact with services and schema for defining the model structure.

### Certificates  
- **Services**:  
  - `mongodb`  
- **APIs**:  
  - **Certificate**: Read one certificate using _id.
  - **Certificates**: Read all certificates of a person using personId.
  - **CreateCertificate**: Creates a certificate and notifies the user via email.
  - **DeleteCertificate**: Deletes one certificate using _id.
  - **UpdateCertificate**: Updates one certificate using _id and notifies the user via email.

### Education  
- **Services**:  
  - `mongodb`  
- **APIs**:  
  - **Education**: Read one education using _id.  
  - **Educations**: Read all education records of a person using personId.  
  - **CreateEducation**: Creates education and notifies the user via email.  
  - **DeleteEducation**: Deletes one education record using _id.  
  - **UpdateEducation**: Updates one education record using _id and notifies the user via email.

### Link  
- **Services**:  
  - `mongodb`  
  - `elasticsearch`  
  - `search`  
- **APIs**:  
  - **CreateLink**: Creates a link.  
  - **DeleteLink**: Deletes one link using _id.  
  - **ReadAllLinks**: Reads all links of a person using personId.  
  - **ReadOneLink**: Reads one link using _id.  
  - **UpdateLink**: Updates one link using _id.

### People  
- **Services**:  
  - `mongodb`  
  - `elasticsearch`  
  - `search`  
- **APIs**:  
  - **PeopleSearch**: Used for searching, sorting, and querying people.  
  - **CreatePerson**: Creates a person and adds it to the employee context.  
  - **DeletePerson**: Deletes one person using _id.  
  - **ExistingUser**: Checks for an existing user using personId.  
  - **PeopleIdByEmail**: Gets all people using email IDs.  
  - **PersonAttendancePercent**: Calculates the percentage of a person.  
  - **Person**: Reads one person using _id.  
  - **UpdatePerson**: Updates one person using _id.

### Work Experience  
- **Services**:  
  - `mongodb`  
  - `elasticsearch`  
  - `search`  
- **APIs**:  
  - **ReadOne**: Reads one work experience using _id.  
  - **ReadAll**: Reads all work experiences of a person using personId.  
  - **Create**: Creates work experience and notifies the user via email.  
  - **Delete**: Deletes one work experience using _id.  
  - **Update**: Updates one work experience using _id and notifies the user via email.

---

## 7. Settings

Stores project configuration settings.
- **checkinModelId**: Stores CheckIn modelId.
- **domain**: Stores domain URL.
- **filesApi**: Stores FilesApi URL.
- **holidayModelId**: Stores Holiday modelId.
- **projectsAppId**: Stores Projects appId.
- **timeoffModelId**: Stores Timeoff modelId.
- **toUsers**: Stores an array of userIds to whom mail will be sent.

---

## 8. Statics

Stores static files that can be modified via APIs.
- **employeeId**: Automatically increments the `employeeId` in the `Person` model to ensure a unique ID for each person.

---

## 9. Workflows

Handles processes running in the background.

**-- No Content Available --**

---
