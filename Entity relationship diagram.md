<img width="458" height="337" alt="picture" src="https://github.com/user-attachments/assets/cd91d07d-1d09-4441-81b9-8d87ca667ada" />



##Entities


#IT Ticket Table: 1:M relationship with Ticket Activity, 1:M relationship with notification log.

#Columns: ID · Title · Category · Priority. Status 



#Requester Table: 1:M relationship with IT ticket

#Columns: Name · Email · Department. Phone · Manager


#IT Agent/Support Table: 1:M relationship with IT Ticket Activity, 1:M relationship with knowledge base
#Colums: Name · Email · Team. Manager. Workload · Availability

#SLA configuration Table: 1:M relationship with IT Ticket
#Columns:Priority levels

#Knowledge Base Table: 1:M relationship with IT Ticket

#Ticket activity table

#Notification Log Table

<img width="3508" height="4963" alt="techcare_erd_full" src="https://github.com/user-attachments/assets/18d9a122-1f59-4a07-b7cf-cb955434cd33" />

