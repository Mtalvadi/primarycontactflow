# Case - Primary Contact Finder

## Pre-requisite :
-	Custom field named – “Account Roles” is created with picklist datatype on the Contact object.
-	It contains values – “Primary Contact”, “Primary Contact Spouse”, “Event Guest”, “Business Partner”.
-	Record triggered type (Case - Primary Contact Finder) flow is configured and activated.


## 1st Scenario

While creating a new case on the Account :-

Condition : If the custom field  “Account Roles” of picklist datatype under the Contact record is NULL 

Expected outcome : The “Contact Name” lookup field on the case which is being created should be updated with the only 1 contact that is affiliated to the account.

![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/80e8ae74-be12-4512-848c-8d45e81b8c67)
![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/3ce2b90c-17a0-49e6-8639-4c3f0e03851b)
![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/1d4df746-c4af-4c7b-9ce2-35ccbf9d23ef)

Solution output : In above demo, “Andy Young” which was the only contact record on the account and the Account Roles field was NULL, the contact name value has been updated to Andy Young after the case is created. 

![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/21ddd4c8-72be-4fb9-81d8-de17b094a88a)

## 2nd Scenario

While creating a new case on the Account:-

Conditions  : 
1)	If there are multiple contacts on the Account
2)	If the custom field  “Account Roles” of picklist datatype under the Contact record is NULL for ALL the contact records 

Expected outcome : The “Contact Name” lookup field on the case which is being created should be updated with the oldest contact (based on Created Date field value) that is affiliated to the account.

![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/3c6bbb6d-cab3-4aee-9a83-87cd18b30ee7)

![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/cbf3ebb8-3633-4003-a50f-f17c791e0bf3)  ![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/bdcf4194-0444-48d0-836e-7c15da7b3bbf)

![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/dd223e2e-b32e-4fe5-a830-9bc78b996b97)

Solution output : 
In above demo, since contact record – “Andy Young” was created on “20 February 2024” & contact record – “David Smith” was created on “28 February 2024”.
the “Contact Name” lookup field on the case which is being created has updated the Contact name value to - Andy Young on the case as it was the oldest contact record on the account.

![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/e0fcce93-869b-496c-aeb9-21660a685169)
![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/ff7a1a8b-b7ad-42cf-b196-0afce5aac0c4)

## 3rd Scenario

While creating a new case on the Account, 

Condition:  
-	If the account contains multiple contact records
-	If the custom field  “Account Roles” of picklist datatype under any contact record contains value as – “Primary Contact” 

Expected outcome : The “Contact Name” lookup field on the case which is being created should be updated with the contact whose Account Roles field contains “Primary Contact” value that is affiliated to that account.

![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/182cdc2d-4b34-4f65-8656-50c9bf5a281b)

![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/99145ae4-4c3a-49dc-b826-b668895ad42e) ![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/97a949ab-5905-4da6-8ce6-6b24265308a5)

![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/64881137-b37d-406d-87ef-fcc634700c36)

Solution output : 
In above demo, since the contact record – “Roger Penrose” contains the value in the “Account Roles” picklist field, the Contact Name field is updated to Roger Penrose after the case is created.

![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/340bf2be-8392-4b73-9920-c4124eca22c6)

![image](https://github.com/Mtalvadi/primarycontactflow/assets/83495051/2895a170-ef59-427a-8501-a369d331e267)

















