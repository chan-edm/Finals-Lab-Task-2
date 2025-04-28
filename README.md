# Finals-Lab-Task-2
## MySQL Database Creation:Sample screenshot and how it works depend of what he needs.

# Step By Step Process
### 1. Create the student table:
- Define username as a VARCHAR(50).
- Set username as the Primary Key.
# Screenshot and Structure sample:
https://github.com/chan-edm/README/blob/c75dbf0fa07128c4fa1c8b514d7dd253a56c83cf/Images/final%202%20task%201.png
https://github.com/chan-edm/README/blob/c75dbf0fa07128c4fa1c8b514d7dd253a56c83cf/Images/final%202%20task%201%20sample.png

### 2. Create the assignment table:
- Define shortname as a VARCHAR(50) and set it as the Primary Key.
- Define due_date as a DATE NOT NULL.
- Define url as a VARCHAR(255), which can be null.
# Screenshot and Structure sample:
https://github.com/chan-edm/README/blob/c75dbf0fa07128c4fa1c8b514d7dd253a56c83cf/Images/final%202%20task%202.png
https://github.com/chan-edm/README/blob/c75dbf0fa07128c4fa1c8b514d7dd253a56c83cf/Images/final%202%20task%202%20sample.png

### 3. Create the submission table:
- Define username and shortname both as VARCHAR(50).
- Define version as an INT.
- Define submit_date as a DATE NOT NULL.
- Define data as TEXT.
- Set a composite primary key of (username, shortname, version).
- Add foreign keys referencing the student and assignment tables.
# Screenshot and Structure sample:
https://github.com/chan-edm/README/blob/c75dbf0fa07128c4fa1c8b514d7dd253a56c83cf/Images/final%202%20task%203.png
https://github.com/chan-edm/README/blob/c75dbf0fa07128c4fa1c8b514d7dd253a56c83cf/Images/final%202%20task%203%20sample.png

# Table Relationships
### 1. **`student` table**
- **Primary Key:** `username`
- **Relationships:**
  - **One-to-Many** relationship with `submission`
    - One student (`username`) can have **many submissions**.
# Screenshot and Structure sample:

### 2. **`assignment` table**
- **Primary Key:** `shortname`
- **Relationships:**
  - **One-to-Many** relationship with `submission`
    - One assignment (`shortname`) can have **many submissions** from different students (or multiple versions from the same student).
# Screenshot and Structure sample:

### 3. **`submission` table**
- **Composite Primary Key:** `(username, shortname, version)`
- **Relationships:**
  - **Many-to-One** with `student`
    - Each submission belongs to **one student**.
  - **Many-to-One** with `assignment`
    - Each submission is for **one assignment**.
  - Overall, it represents a many-to-many relationship between students and assignments, with a version to track multiple submissions.
# Screenshot and Structure sample:


# Er Diagram sample:
https://github.com/chan-edm/README/blob/c75dbf0fa07128c4fa1c8b514d7dd253a56c83cf/Images/final%202%20eer%20diagram%202.png
https://github.com/chan-edm/README/blob/c75dbf0fa07128c4fa1c8b514d7dd253a56c83cf/Images/final%202%20eer%20diagram.png
