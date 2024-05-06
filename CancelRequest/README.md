# Cancel Request UseCase
## Actor: 
- Employee
## Goal: 
- The employee wants to cancel an approved vacation time request.
## Preconditions:
- The employee has a vacation time request that has been approved and is scheduled for some time in the future or the recent past (previous 5 business days). See also main flow preconditions.

## Case flow:
1. The employee navigates to the VTS home page through the intranet portal application, which identifies and authenticates the employee with the privileges necessary for using the VTS.
2. The VTS home page contains a summary of vacation time requests, outstanding balance per category of time, and the current status of all active vacation time requests for the previous 6 months and up to 18 months in the future.
3. The employee selects a vacation time request to cancel, one that is in the future (or recent past) and has been approved.
4. If the request is in the future, the employee is prompted to confirm the cancellation. If the request is in the recent past, the employee is prompted to confirm the cancellation and provide a short explanation. If the employee approves the cancellation and provides the required information, an e-mail notification is sent to the manager, and the state of the request is changed to canceled. The time allowances used to make the request are returned to the employee. The employee can also abort the cancellation, effecting no changes to the current requests.
5. The employee is returned to the main VTS home page. The summaries are updated to reflect any changes made to the employee’s outstanding vacation time requests.

## Flowcharts:
![cancelReqFlowchart](https://github.com/AbdoAyman753/VTS/assets/49798366/5ccca1f7-1f25-4382-b868-c6daa8c18f87)

## Sequence Diagrams:
![cancelReqEmpSeq](https://github.com/AbdoAyman753/VTS/assets/49798366/e51a7a4d-89f8-468d-97a9-a4963796ba9f)
## State Machine:
![cancelStateMachine](https://github.com/AbdoAyman753/VTS/assets/49798366/d82d7765-2660-4b1d-9d52-f96364a29da6)
## Psuedo code:
```
signInToPortal();
redirectToVTS();
getApprovedRequests();
approved = cancelApprovedReq(req_id);
if(approved)
  returnEmpAllowance();
notify();

cancelApprovedReq(req_id){
  validateCanelation(req_id);
}
validateCanelation(req_id){
  if(req > 5 working days in past || req in future)
    return valid
}
```
