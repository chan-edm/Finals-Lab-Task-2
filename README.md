# Finals-Lab-Task-2
## MySQL Database Creation:Sample screenshot and how it works depend of what he needs.

# Step By Step Process
### 1. Create the student table:
- Define username as a VARCHAR(50).
- Set username as the Primary Key.
# Screenshot and Structure sample:
![Image](https://github.com/user-attachments/assets/26651d0f-8362-4242-9761-b74f61818c6b)
![Image](https://github.com/user-attachments/assets/452a1bcc-32ce-41a1-98db-d8a0c3477ca1)

### 2. Create the assignment table:
- Define shortname as a VARCHAR(50) and set it as the Primary Key.
- Define due_date as a DATE NOT NULL.
- Define url as a VARCHAR(255), which can be null.
# Screenshot and Structure sample:
![Image](https://github.com/user-attachments/assets/f81c35e3-3664-4962-b68c-2cd6f03bd6c4)
![Image](https://github.com/user-attachments/assets/703fe1dc-3929-4975-b4e8-b088a4a89dd1)

### 3. Create the submission table:
- Define username and shortname both as VARCHAR(50).
- Define version as an INT.
- Define submit_date as a DATE NOT NULL.
- Define data as TEXT.
- Set a composite primary key of (username, shortname, version).
- Add foreign keys referencing the student and assignment tables.
# Screenshot and Structure sample:
![Image](https://github.com/user-attachments/assets/ced7306b-06a3-4ee6-8dc0-932cef16ac75)
![Image](https://github.com/user-attachments/assets/37a46c40-b6d5-4129-b618-84871c821256)

# Table Relationships
### 1. **`student` table**
- **Primary Key:** `username`
- **Relationships:**
  - **One-to-Many** relationship with `submission`
    - One student (`username`) can have **many submissions**.


### 2. **`assignment` table**
- **Primary Key:** `shortname`
- **Relationships:**
  - **One-to-Many** relationship with `submission`
    - One assignment (`shortname`) can have **many submissions** from different students (or multiple versions from the same student).


### 3. **`submission` table**
- **Composite Primary Key:** `(username, shortname, version)`
- **Relationships:**
  - **Many-to-One** with `student`
    - Each submission belongs to **one student**.
  - **Many-to-One** with `assignment`
    - Each submission is for **one assignment**.
  - Overall, it represents a many-to-many relationship between students and assignments, with a version to track multiple submissions.


# Er Diagram sample:
![Image](https://github.com/user-attachments/assets/3e8ab6dc-ac86-484c-abf9-b9e008cc5c90)
![Image](https://github.com/user-attachments/assets/3ea1a9bb-1722-4510-a332-d99753e10689)

[BACK TO PORTFOLIO](https://chan-edm.github.io/README/)
