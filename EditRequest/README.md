# Edit Request UseCase
## Actor: 
- Employee
## Goal: 
- The employee wants to edit the description or title of a pending request.
## Preconditions:
- An employee has made a vacation time request, and that request has yet to be approved or denied by an authorized manager. See also main flow preconditions.

## Case flow:
1. The employee navigates to the VTS home page through the intranet portal application, which identifies and authenticates the employee with the privileges necessary for using the VTS.
2. The VTS home page contains a summary of vacation time requests, outstanding balances per category of time, and the current status of all active vacation time requests for the previous 6 months and up to 18 months in the future.
3. The employee selects a request to edit, one that is pending approval.
4. The VTS displays an editable view of the request. The employee is allowed to change the title, comments, or dates. The employee can also choose to delete or withdraw this request.
5. The employee changes request information and submits the changes to the system.
6. If the employee withdraws the request, the VTS prompts for confirmation before withdrawing the request. If changes are made only to the information, the changes are accepted, and the screen returns to the main VTS home page. If there are errors or problems with the information changes, the VTS redisplays the editing page and highlights and explains all problems.

## Flowcharts:
![editReqFlowchart](https://github.com/AbdoAyman753/VTS/assets/49798366/47a5bb77-ee9a-4aed-bf79-1c53a8c38399)

## Sequence Diagrams:
![editReqEmpSeq](https://github.com/AbdoAyman753/VTS/assets/49798366/47007973-6682-49ec-94b9-aadaa152f1b2)
