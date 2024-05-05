# Vacation Tracking System (VTS)
Analysis and Design using UML and diagrams to build a vacation tracking system that provide individual employees with the capability to manage their own vacation time, sick leave, and personal time off, without having to be an expert in company policy or the local facility’s leave policies.


## Requirements:
#### Functional:
- Uses e-mail notification to request manager approval and notify employees of request status changes.
- Enables manager approval (optional).
- Is implemented as an extension to the existing intranet portal system, and uses the portal’s single-sign-on mechanisms for all authentication.
- Keeps activity logs for all transactions.
- Enables the HR and system administration personnel to override all actions restricted by rules, with logging of those overrides.
- Allows managers to directly award personal leave time (with system-set limits).
- Provides access to requests for the previous calendar year, and allows requests to be made up to a year and a half in the future.
- Provides a Web service interface for other internal systems to query any given employee’s vacation request summary.
#### Non-Functional:
- Uses existing hardware and middleware.
- Implements a flexible rules-based system for validating and verifying leave time requests.
- Interfaces with the HR department legacy systems to retrieve required employee information and changes.


## Constrains:
- Is implemented as an extension to the existing intranet portal system.
- Uses the portal’s single-sign-on mechanisms for all authentication.
- Uses existing hardware and middleware.
- Interfaces with the HR department legacy systems.


## Domain:
- **User Management**: This includes functionalities for adding, editing, and deleting user accounts. Users may include employees, managers, and administrators, each with different levels of access and permissions.
- **Vacation Requests**: Users should be able to submit vacation requests through the system. This involves specifying the dates of the vacation, the reason for the request, and any additional notes.
- **Approval Workflow**: There should be a workflow for managers to review and approve/reject vacation requests. This may involve multiple levels of approval depending on the organization's hierarchy.
- **Availability Tracking**: The system should display employees' availability based on approved vacation requests, making it easy for managers to see who is available and when.
- **Accrual and Balances**: The system should keep track of employees' vacation balances, including accrued time off, used time off, and remaining balances. This may vary depending on factors like seniority, employment status, or company policy.
- **Web-Centric and Portal Integration**: The system should be built as a web app and can be accessed through portal.
- **Calendar Integration**: Integration with calendar application to automatically sync approved vacations with employees' calendars.
- **Notifications**: Automated notifications throw emails to inform users about the status of their vacation requests, and alerts for managers regarding pending approvals.
- **Reporting and Analytics**: Generate reports on vacation usage, trends, and patterns to help HR or managers make informed decisions about resource allocation and staffing.
- **Compliance and Legal Requirements**: Ensure the system complies with labor laws and company policies regarding vacation time, such as minimum vacation requirements and accrual rates.
- **Security and Access Control**: The authentication should be made through portal and then redirected to the VTS from there, and HR accounts should be separated from their personal employee accounts.
- **User Interface**: An intuitive and user-friendly interface that makes it easy for employees to submit requests, managers to review them, and HR to manage the system settings and policies without extra training.

By addressing these aspects, a Vacation Tracking System can streamline the process of managing employee vacations, enhance communication between employees and managers, and ensure compliance with company policies and legal requirements.


## Actors:
1. Employee: The main user of this system. An employee uses this system to manage his or her vacation time.
2. Manager: An employee who has all the abilities and goals of a regular employee, but with the added responsibility of approving vacation requests for immediate subordinates. A manager may award subordinates comp time, subject to certain limits set in the system.
3. Clerk: A member of the HR department who has sufficient rights to view employees’ personal data and is responsible for ensuring that employees’ information in all HR systems is up to date and correct. An HR clerk can add or remove nearly any record in the system. In the real world, HR clerks may or may not be employees; however, if they are employees, they use two separate login IDs to manage these two different roles.
4. System Admin: A role responsible for the smooth running of the system’s technical resources (e.g., Web server, database) and for collecting and archiving all log files.


## ERD:
![Screenshot 2024-05-05 181101](https://github.com/AbdoAyman753/VTS/assets/49798366/81863e88-7600-4c52-b1e3-ac69224f596a)

## UseCases:
- [Manage Time](https://github.com/AbdoAyman753/VTS/blob/main/ManageTime/README.md)
- [Withdraw Request](https://github.com/AbdoAyman753/VTS/tree/main/WithdrawRequest)



