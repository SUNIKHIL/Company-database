Employee Table ->
Contains employee details including personal data, salary, reporting structure, and branch assignment.
Implements a self-referencing relationship using super_id to model the company hierarchy.

<img width="691" height="400" alt="Screenshot 2026-03-03 072747" src="https://github.com/user-attachments/assets/603dcd2f-88a4-49f0-9b02-c9d7f3041eb1" />


Branch Table -> Stores company branch details including branch ID, branch name, and assigned manager.
Each branch is uniquely identified by branch_id and linked to an employee as manager.

<img width="616" height="244" alt="Capture" src="https://github.com/user-attachments/assets/212a18c5-0202-491e-a4c5-2073d8bf281d" />

Client Table -> Maintains client information and the branch responsible for handling each client.
The branch_id acts as a foreign key to associate clients with specific company branches.

<img width="574" height="353" alt="client" src="https://github.com/user-attachments/assets/ffa62c74-caff-449d-b0e7-6d2b49d47d94" />

Works_With Table -> Represents the many-to-many relationship between employees and clients along with total sales.
Uses a composite primary key (emp_id, client_id) to ensure unique employee-client relationships.

<img width="519" height="397" alt="works_with" src="https://github.com/user-attachments/assets/2bceb724-0007-4307-9bb3-d4bad4274fea" />

Branch Supplier Table -> Tracks suppliers serving each branch and the type of supplies provided.
Implements a composite primary key (branch_id, supplier_name) to prevent duplicate supplier entries per branch.

<img width="568" height="332" alt="branch_suppliers" src="https://github.com/user-attachments/assets/dd71c9ac-2c8f-4aac-8e5f-44be1ff24f10" />


