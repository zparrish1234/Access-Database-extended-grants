# extended-grants-database-model

# Departmental Usage Overview
This data model was designed from the perspective of a Grants department 
for a nonprofit responsible for the entire grant cycle. This included but
not limited to grant opportunity tracking, application tracking, award tracking, 
budget management, compliance, grant impact tracking and financial reporting.

Different roles interact with the database in different ways:
- Vice President of Grants and Government Affairs is responsible for strategic oversight of grant funding and government relationships 
- Grants Manager is responsible for maintaining grantor contact information, pass-through reports, and budget revisions.
     - As well as the oversight for the Grant Administrators and Grant Writer
- Grants administrators manage post awards deliverables and some financial reporting.
- Grants Writer is responsible for grant opportunities, reapplying for grants and completing applications. 
- Leadership uses aggregated reports for oversight and planning.
- Finance Department uses aggregated reports for accruals, and revenue tracking.

 # Core Workflows Supported

1. Grant Opportunities
   - An opportunity comes from either a previous grant in past years / awards, or a contact.
2. Award
   - A new grant award is created and assigned an internal grant code
   - The original approved budget is recorded at both summary and line-item levels
3. Budget Revisions
   - Budget amendments are stored separately from the original award
   - Revision line items allow tracking increases and reallocations over time
4. Spending & Monitoring
   - Monthly spending is recorded against awards
   - Remaining balances are calculated dynamically from original + revised budgets
5. Reporting & Oversight
   - Staff can report on total spent vs budget
   - Leadership can identify overspent or underutilized grants
  
# Design Rationale

- Awards and budgets are separated to allow multiple revisions over time
- Line-level tables enable detailed reporting without overwriting historical data
- Monthly spending tables support trend analysis and auditability
- Lookup tables normalize codes to ensure consistent reporting

# Scope & Assumptions

This model represents a conceptual design intended to reflect real-world
grant administration workflows. It is not a deployed production system,
but a data modeling exercise focused on structure, logic, and reporting needs.
