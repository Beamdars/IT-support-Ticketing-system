# Business Requirement

##Ticket Management

The system developed must provide a self-service portal where staff can log can log IT support requests at any time without needing to call or email the IT team.
Each ticket must capture, at minimum: requester name, department, contact details, issue category, description, date/time submitted, and priority level.
The system has to automatically generate a unique ticket reference number upon submission and send a confirmation notification to the requester.
IT agents must be able to view, claim, update, reassign, and close tickets from a central agent dashboard.

## SLA prioritisation

Tickets must be categorised by priority ( High, Medium and Low), with a defined  response and resolution.
The system must track SLA timers from the moment a ticket is submitted and display real-time SLA status on the agent dashboard.
Automated alerts must be triggered when a ticket is approaching its SLA deadline (at 75% elapsed) and when an SLA is breached.
Unassigned or stalled tickets must automatically be escalated to the IT Manager after a  period of inactivity (configured into the system)

## Communication & Notifications

Requesters must receive automated email or in-app notifications at different milestones eg ticket received, ticket assigned, update added, and ticket resolved.
Requesters must be able to log into the portal at any time to view the current status of their tickets without needing to contact the IT team.
IT Agents must be notified immediately a new ticket is assigned to them or when a ticket they own is updated by the requester.

## Reporting

IT Managers must have access to a reporting dashboard showing: total tickets by status, SLA compliance rate, average response and resolution times, volume by category, and agent workload.
Reports must be exportable in at least Excel and PDF format.
The system must retain a full audit history for every ticket, including all updates, status changes, and agent actions.


# Acceptance Criteria: 
the system should meet some criteria, as highlighted in the business requirement before it is moved to production. Each criterion will be validated through User Acceptance Testing (UAT) conducted with representatives from IT and other departments/users

## Ticket management/logging
ID	  Acceptance Criterion	                                                                                            How It Will Be Measured
AC-01	A staff member can submit a ticket via the self-service portal in under 3 minutes with no training.	          Timed UAT test with 5 first-time users. All must complete submission successfully.
AC-02	A unique ticket reference number is generated and emailed to the requester within 60 seconds of submission.	  Submit 10 test tickets and verify reference and email receipt time.
AC-03	All mandatory ticket fields (category, description, priority, contact details) are enforced.                	Attempt to submit incomplete tickets; system must block and show clear error messages.
AC-04	An IT agent can view, claim, update, reassign, and close any ticket from the agent dashboard.	                 Agent UAT walk-through covering all five actions on live test tickets.
AC-05	Two agents cannot be simultaneously assigned to the same ticket.	                                             Attempt to assign a ticket already owned by another agent; system must prevent it.


## SLA escalation
ID	Acceptance Criterion	                                                                                        How It Will Be Measured
AC-06	SLA timers begin automatically the moment a ticket is submitted and are visible on the agent dashboard.	   Submit test tickets and verify SLA countdown displays correctly by priority level.
AC-07	An alert is sent to the assigned agent when a ticket reaches 75% of its SLA time without resolution.	     Create test tickets with short SLA windows and confirm alerts set-off at the correct threshold.
AC-08	An escalation notification is sent to the IT Manager when any ticket breaches its SLA.	                   Allow a test ticket to breach SLA and confirm IT Manager receives notification within 5 minutes.
AC-09	Unassigned tickets automatically escalate to the IT Manager after the configured inactivity threshold.	   Leave a test ticket unassigned for the defined period and confirm escalation triggers.

## Communication
ID	Acceptance Criterion	                                                                                                   How It Will Be Measured
AC-10	Requesters receive automated notifications at all four key milestones: submitted, assigned, updated, and resolved.	  Trace a test ticket through all stages and confirm all four notifications are received.
AC-11	A requester can log into the portal and view the current status of all their tickets without contacting IT.	          UAT test: requester logs in and locates their open ticket without assistance.
AC-12	Agents receive an in-system and email notification within 2 minutes of being assigned a new ticket.	                  Assign test tickets to agents and measure notification delivery time.

## Data Reporting
ID	Acceptance Criterion	                                                                                                              How It Will Be Measured
AC-13	The manager dashboard displays ticket volumes by status, SLA compliance rate, average resolution time, and workload by agent.	   IT Manager UAT: confirm all five data points are visible and accurate against test data.
AC-14	Reports can be exported in both Excel and PDF format.	                                                                           Export a sample report in both formats and confirm completeness and formatting.
AC-15	A complete audit trail is maintained for every ticket, showing all updates, status changes, and agent actions with timestamps.	 Inspect the audit log of a test ticket after performing multiple actions; confirm all are recorded.





