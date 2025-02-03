# Software Requirements and Use Cases

## Your Project Title
--------
Prepared by:

* `Tair Kareneyev`,`StaffersSE`

---

**Course** : CS 3733 - Software Engineering

**Instructor**: Sakire Arslan Ay

---

## Table of Contents
- [1. Introduction](#1-introduction)
- [2. Requirements Specification](#2-requirements-specification)
  - [2.1 Customer, Users, and Stakeholders](#21-customer-users-and-stakeholders)
  - [2.2 User Stories](#22-user-stories)
  - [2.3 Use Cases](#23-use-cases)
- [3. User Interface](#3-user-interface)
- [4. Product Backlog](#4-product-backlog)
- [4. References](#4-references)

<a name="revision-history"> </a>

## Document Revision History

| Name | Date YYYY-MM-DD | Changes | Version |
| ------ | ------ | --------- | --------- |
|Revision 1 |2025-02-02 |Initial draft |0.1        |
|Revision 2 |2025-02-03 |Final draft |1.0        |
|      |      |         |         |

----
# 1. Introduction
StaffersSE is a web-based platform designed to simplify hiring process of undergraduate student for research positions. Developed to meet the needs of faculty members who are seeking for research assistance, StaffersSE allows qualified undergraduates students to connect with available opportunities posted by faculty, simplifying hiring process and application management.

Purpose:

Make the matching process of undergraduate candidates with research positions efficient and user-friendly.
Simplify the application and review process for faculty members.
Enhance transparency between students and faculty.

Target Audience:

Faculty Members: Looking for efficient ways to recruit and manage undergraduate student researchers.
Undergraduate Students: Seeking research opportunities that align with their academic interests and career goals.

Benefits:

Reduces administrative and bureaucratic load by automating parts of the hiring process - less time on hiring process, more time on research.
Filtering and search capabilities to better match skilled students with specific needs of research projects - better matching process.
Clear application statuses and feedback features so that students understand where they stand in the selection process - transparency.
Better access to research opportunities for undergraduates, which helps them gain experience while helping faculty members - more opportunitites.
Generally, it is more effective, user-friendly recruitments platform comparing to the traditional, non-digital way (physical paper, physical meetings and ect).

----
# 2. Requirements Specification

This section specifies the software product's requirements. Specify all of the software requirements to a level of detail sufficient to enable designers to design a software system to satisfy those requirements, and to enable testers to test that the software system satisfies those requirements.
----
## 2.1 Customer, Users, and Stakeholders

Customer:

* The primary customer is an academic institution (or individual departments) that want an effective solution for faculty to hire undergraduate students for research positions.

Users:

* Faculty Members: They will use the system to post research opportunities, review applications, and manage candidate applications.
* Undergraduate Students: They will use the system to search for available research positions, submit applications, and track application statuses.

Stakeholders:
* University Department Heads: Interested in promoting research opportunities and ensuring quality candidate matching
* IT Department: Responsible for the maintenance, security, and general operation of the platform.

----
## 2.2 User Stories

* As a faculty member, I want to post research positions so that I can hire qualified undergraduate candidates for my research projects.

* As a faculty member, I want to review and manage applications so that I can effectively select the best candidates for my research projects.

* As a faculty member, I want to filter applications by criteria (e.g., GPA, major) so that I can quickly find the most suitable candidates.

* As an undergraduate student, I want to search for available research positions so that I can find opportunities 

* As an undergraduate student, I want to apply filter during search for available research positions so that I can find opportunities that match my academic interests and career goals.

* As an undergraduate student, I want to track the status of my applications so that I know if I am being considered or need to apply for other positions.

* As an undergraduate student, I want to withdraw my pending positions so that I dont have to work in positions that I am not interested in.

* As an undergraduate student, I want to apply for desired positions so that I can get hired, do research and gain experience.

----
## 2.3 Use Cases

Actors:

* Faculty Member: Responsible for posting research positions and reviewing applications.

* Undergraduate Student: Responsible for searching and applying for research positions.

| Use case # 1      |   |
| ------------------ |--|
| Name              | Manage Research Positions and Applications  |
| Participating actor  | Faculty Member  |
| Entry condition(s)     | Faculty member is logged in and has navigated to the "Manage Positions" section. A research position draft exists or a new position is being created. |
| Exit condition(s)           | The research position is successfully posted or updated, and any submitted applications are available for review.  |
| Flow of events	           | 1. The faculty member selects "Create New Research Position."
|                            | 2. The system displays a form to enter position details (title, description, requirements, deadline, etc.).
|                            | 3. The faculty member fills in and submits the form.
|                            | 4. The system validates the input and posts the research position, making it visible to students.
|                            | 5. The faculty member navigates to the "Applications" section to review submissions.
| Alternative flow of events | - If the input validation fails, the system displays error messages and prompts the faculty member to correct the entries.
|                            | - If the system encounters an error while posting the position, it notifies the faculty member.
| Iteration #         | #	Iteration 2  |

| Use case # 2      |   |
| ------------------ |--|
| Name              |  Search and Apply for Research Position  |
| Participating actor  | Undergraduate Student  |
| Entry condition(s)     | The student is logged in and navigates to the "Available Positions" section.  |
| Exit condition(s)           | The student's application is successfully submitted and acknowledged by the system.  |
| Flow of events	           | 1. The student accesses the "Available Positions" page.
|                            | 2. The system displays a list of current research positions with brief details.
|                	           | 3. The student selects filter criteria (e.g., academic interests, research type, faculty name).
|                	           | 4. The system applies the filters and updates the list of available positions.
|                            | 5. The student selects a specific research position to view full details.
|                            | 6. The system displays complete information about the position, including requirements and application deadline.
|                            | 7. The student clicks on "Apply" and fills in the application form with the required information (e.g., personal statement 
|                            | resume, etc.).
|                            | 8. The system validates and submits the application, then confirms successful submission to the student.
| Alternative flow of events | - If the students application data is incomplete or invalid, the system prompts for corrections before submission.
|                            | - If the position is no longer available (e.g., the deadline has passed or the position has been filled), the 
|                            | system informs the student and prevents the application submission.
|                            | - If the student does not apply any filter in step 3, defaut filter is "show most recent".
| Iteration #         | #	Iteration 1  |

| Use case # 3      |   |
| ------------------ |--|
| Name              | Filter Applications by Criteria  |
| Participating actor  | Faculty Member  |
| Entry condition(s)     | Faculty member is logged in and has navigated to the "Applications" section with applications already submitted for research positions.  |
| Exit condition(s)           | The system displays a filtered list of applications based on the faculty member’s selected criteria.  |
| Flow of events	           | 1. The faculty member accesses the "Applications" section.
|                            | 2. The system displays a list of all submitted applications.
|                            | 3. The faculty member selects filter criteria (e.g., GPA, major, graduation year).
|                            | 4. The system applies the filters and displays the updated list of applications.
|                            | 5. The faculty member reviews the filtered list.
| Alternative flow of events    |  - If no applications meet the selected criteria, the system displays a message indicating no matching results. |
|                             | - If invalid filter criteria are selected, the system prompts the faculty member to correct the inputs.
| Iteration #         | # Iteration 3  |

| Use case # 4      |   |
| ------------------ |--|
| Name              | Track and Withdraw Application  |
| Participating actor  | Undergraduate Student  |
| Entry condition(s)     | The student is logged in and has at least one submitted application.  |
| Exit condition(s)           | The student successfully views the application status or withdraws an application if desired. |
| Flow of events |1. The student navigates to the "My Applications" section.
|                            | 2. The system displays a list of the student’s submitted applicati\ons with current statuses (e.g., Under Review, Accepted, Rejected).
|                            | 4. The student selects an application to view detailed information.
|                            | 5. If the student chooses to withdraw, they click on the "Withdraw" button.
|                            | 6. The system confirms the withdrawal and updates the status of the application to "Withdrawn."  |
| Alternative flow of events    |  - If the students application data is incomplete or invalid, the system prompts for corrections before submission. |
|     |  - If the position is no longer available (e.g., the deadline has passed or the position has been filled), the system informs the student and prevents the application submission. |
| Iteration #         | #	Iteration 1  |

----
# 3. User Interface

Here you should include the sketches or mockups for the main parts of the interface.
You may use Figma to design your interface:

  Example image. The image file is in the `./images` directory.
  <kbd>
      <img src="images/figma.jpg" border="2">
  </kbd>
  
----
# 4. Product Backlog

Professor Arslan told me not to do it and assume it is submitted

----
# 5. References

None