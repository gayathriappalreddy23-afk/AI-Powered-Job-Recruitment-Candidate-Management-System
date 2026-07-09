AI-Powered Job Recruitment & Candidate Management System
Project Overview:
The AI-Powered Job Recruitment & Candidate Management System (AIRCMS) is a
Salesforce-based recruitment platform designed to streamline and intelligently manage
the end-to-end hiring lifecycle — from candidate application and screening to offer
approval and onboarding.
The system centralizes candidate records, job openings, interview processes, recruiter
activities, hiring approvals, and AI-driven evaluation insights into a single intelligent
workspace.
Built using Salesforce Admin capabilities, Flows, Approval Processes, Lightning
Experience, and Agentforce AI, the application eliminates manual resume screening and
inconsistent hiring decisions by introducing intelligent candidate scoring and automated
workflows.
Recruiters can instantly view AI-generated summaries, candidate priority indicators, and
hiring recommendations directly on candidate records. Hiring managers can review
salary approvals, risk insights, and interview performance summaries through structured
dashboards and automated alerts.
This solution enhances recruitment efficiency, ensures standardized decision-making,
improves candidate quality, and enforces governance using role-based security and
approval processes.
The system is scalable, secure, and designed to support high-volume recruitment
operations while maintaining data integrity and transparency.
Objectives
Centralized Recruitment Management
Provide a single Salesforce platform to manage:
● Candidate profiles
● Job openings
● Applications
● Interview stages
● Offer approvals
● AI hiring recommendations
Automation of Recruitment Workflows
Streamline:
● Candidate screening
● Interview scheduling
● Offer approval workflows
● Recruiter follow-up reminders
● Status updates
AI-Driven Hiring Intelligence
Enable:
● AI candidate scoring
● Hiring risk analysis
● Candidate summaries
● Recommendation support
Security & Governance
Ensure:
● Controlled access to hiring data
● Approval enforcement
● Role-based record visibility
Phase1: Requirement Analysis and Planning
Understanding Business Requirements
Modern organizations receive hundreds of candidate applications daily. Most hiring
teams rely on spreadsheets, emails, and disconnected tools, which leads to:
● Duplicate candidate records
● Lost applications
● Delayed interviews
● Inconsistent hiring decisions
● Lack of transparency
● Poor tracking of recruitment metrics
The business requires a centralized CRM-based hiring system that can:
● Track all candidates in one place
● Standardize screening
● Automate hiring workflows
● Provide AI-driven evaluation
● Improve recruiter productivity
● Support managerial approvals
Salesforce is selected because it offers:
● Secure cloud infrastructure
● Built-in automation tools
● AI capabilities through Agentforce
● Scalable architecture
● Real-time reporting
Defining Project Scope and Objectives
Project Scope
The project includes building a Salesforce recruitment system using Admin tools and
Agentforce AI without custom Apex development.
The application supports the full recruitment lifecycle:
Candidate → Screening → Interview → Offer → Hiring
Objectives
● Implement Salesforce CRM fundamentals in hiring
● Create a scalable recruitment data model
● Apply security at all levels
● Automate workflows using Flows
● Use AI for candidate evaluation
● Enable approval-driven hiring decisions
Phase 2: Salesforce Development – Backend &
Configuration
Milestone 1: Salesforce Account
Introduction:
Are you new to Salesforce? Not sure exactly what it is, or how to use it? Don’t know
where you should start on your learning journey? If you’ve answered yes to any of
these questions, then you’re in the right place. This module is for you.
Welcome to Salesforce! Salesforce is game-changing technology, with a host of
productivity-boosting features, that will help you sell smarter and faster. As you work
toward your badge for this module, we’ll take you through these features and answer
the question, “What is Salesforce, anyway?”.
What Is Salesforce?
Salesforce is your customer success platform, designed to help you sell, service, market,
analyze, and connect with your customers.
Activity 1: Creating Developer Account:
Creating a developer org in salesforce.
1. Go to https://developer.salesforce.com/signup
2. On the sign-up form, enter the following details:
1) First name & Last name
2) Email
3) Job Title: Developer
4) Company: College Name
5) Country: India
Click on sign me up after filling these.
Activity 2: Account Activation
1. Go to the inbox of the email that you used while signing up. Click on the verify
account to activate your account. The email may take 10-30mins and sometimes 2
hours.
2. Click on Verify Account
3. Give a password and answer a security question and click on change password.
4. Then you will redirect to your salesforce setup page.
Milestone 2: Objects Creation
The recruitment system requires custom objects to represent hiring data.
Activity 1: Creating Job Opening Object
To create an object:
1. From the Setup page
2. Click on Object Manager
3. Click on Create >> Custom Object
4. Enter the Label name as Job Opening
5. Enter Plural Label name as Job Openings
6. Enter Record Name as Job Title
7. Select Data Type Text
8. Select Allow Reports
9. Select Allow Search
10. Enable Track Field History
11. Click on Save and New
Activity 2: Creating Candidate Application Object
To create an object:
1. From the Setup page
2. Click on Object Manager
3. Click on Create >> Custom Object
4. Enter the Label name as Candidate Application
5. Enter Plural Label name as Candidate Applications
6. Enter Record Name as Application ID
7. Select Data Type as Auto Number: CA - {0000}, Starting with 1
8. Select Allow Reports
9. Select Allow Search
10. Enable Track Field History
· Click on Save
Milestone 3- Tabs
Activity 1: Creating a tab for Job Opening Object
1. Go to the setup page → type Tabs in Quick Find bar
2. Click on tabs
3. Click on New (under custom object tab).
4. Select Object (Job Opening) >> Select the tab style
5. Click on Next >> (Add to profiles page) keep it as default >> Click on
Next (Add to Custom App) uncheck the include tab.
6. Make sure that the Append tab to the user's existing personal
customizations is checked.
7. Click save
Activity 2: Creating a tab for Candidate Application Object
1. Go to the setup page → type Tabs in Quick Find bar
2. Click on tabs
3. Click on New (under custom object tab).
4. Select Object (Candidate Application) >> Select the tab style
5. Click on Next >> (Add to profiles page) keep it as default >> Click on
Next (Add to Custom App) uncheck the include tab.
6. Make sure that the Append tab to the user's existing personal
customizations is checked.
7. Click save
Milestone 4: Fields & Relationships
Object Field Name Data Type Required
Contact
Candidate ID Auto Number
C-{0000}
Starting
Number-1
Yes
Experience Level Picklist(Fresher,
Mid-Level,
Senior)
Yes
Job Opening Department Picklist( IT, HR,
Finance, Sales)
Yes
Salary Range Currency Yes
Vacancies Number Yes
Job Status Picklist (Open,
Closed, On Hold)
Candidate Application Candidate Master- Detail
(Contact)
Yes
Job Opening Master- Detail
(Job Opening)
Yes
Application Date Date Yes
AI Candidate Score Number Yes
Offer Amount Currency Yes
Application Status Screening
Interview
Offer Submitted
Approved
Yes
Rejected
Hired
Approval Status Picklist (Pending,
Approved,
Rejected)
Yes
Activity 1: Creation of Picklist field for Contact object:
1. Go to Setup → Click on Object Manager
2. Type object name Contact in the Quick Find box → Click on
Contact
3. Click on Fields & Relationships
4. Click on New
5. Select Data Type as Picklist and click Next
6. Enter the Field Label as Experience Level
7. Click on Enter values and enter:
a. Fresher
b. Mid- Level
c. Senior
Click Next, Next, and Save
Activity 2: Creation of Master- Detail field for Candidate Application Object:
1. Go to the Setup page >> click on Object manager >> type object name (Candidate
Application) in the quick find bar >> click on the Candidate Application object.
2. Click on Fields & Relationship
3. Click on New.
4. Select “Master- Detail” as data type and click Next.
5. Select the related object “Contact”.
6. Click on Next.
7. Give Field Label as “Candidate”.
8. Click on Next, Next, Next, Save.
Note: Create other fields from the above Fields table related to this object and
choose the data types of the fields carefully.
Milestone 5 - Validation Rules
Activity 1: To create a Validation rule to Candidate Application Object
1. Go to setup >> click on Object Manager >> type object name (Candidate
Application) in search bar >> click on the Candidate Application object
2. Click on the validation rule >> click on New.
3. Enter the Rule name as “Offer Amount Validation”.
4. Select Active
5. Insert the Error Condition Formula as:
Offer_Amount__c <= 0
6. Enter the Error Message as “Offer amount must be greater than zero.”.
7. Select the Error location as Top of the page
8. Click Save.
Activity 2: To create a Validation rule to Job OpeningObject
1. Validation Rule on Vacancies:
1. Go to setup >> click on Object Manager >> type object name (Job Opening) in search
bar >> click on the Job Opening object
2. Click on the validation rule >> click on New.
3. Enter the Rule name as “Job Vacancies Validation”.
4. Select Active
5. Insert the Error Condition Formula as:
Vacancies__c < 0
6. Enter the Error Message as “Vacancies cannot be negative.”.
7. Select the Error location as Top of the page
8. Click Save.
Activity 3: To create a Validation rule on Candidate Application Object
1. Validation Rule on AI Candidate Score:
1. Go to setup >> click on Object Manager >> type object name (Candidate
Application) in search bar >> click on the Candidate Application object
2. Click on the validation rule >> click on New.
3. Enter the Rule name as “AI Candidate Score Validation”.
4. Select Active
5. Insert the Error Condition Formula as:
OR(
AI__Candidate_Score__c < 0,
AI__Candidate_Score__c > 100
)
6. Enter the Error Message as “AI Candidate score cannot exceed 100.”.
7. Select the Error location as Top of the page
8. Click Save.
Milestone 6 – Duplicate and Matching Rules
This milestone ensures data integrity in the Recruitment System by preventing duplicate
Candidate (Contact) records and duplicate Candidate Application records.
Accurate and clean hiring data is critical for:
Reliable AI candidate scoring
Correct risk analysis
Meaningful Agentforce recommendations
Accurate offer approvals and reporting
Activity 1: Create a Custom Matching Rule for Candidate (Contact)
Objective:
Objective: Ensure each candidate is uniquely identified using Email and Phone.
Steps:
1. Go to Setup.
2. In the Quick Find box, search for Matching Rules.
3. Click New Rule.
4. Select Object: Contact and click Next.
5. Enter Rule Name: Unique Candidate – Email & Phone.
6. In Matching Criteria:
○ Field: Email → Matching Method: Exact
○ Field: Phone → Matching Method: Exact
7. Check Match Blank Fields.
8. Click Next.
9. Click Save & Activate.
Activity 2: Create a Duplicate Rule for Candidate (Contact)
Steps:
1. Go to Setup.
2. Search for Duplicate Rules.
3. Click New Rule.
4. Select Object: Contact.
5. Enter Rule Name: Unique Candidate Email and Phone.
6. Set Action on Create and Action on Edit: Allow and Report.
In Alert Text:
Candidate Email and Phone Number must be unique.
7. In the Matching Rules section:
8. Click Add Rule.
9. Select the previously created Matching Rule
(Unique Candidate – Email & Phone).
10.Click Save & Activate.
Milestone 7: Profiles
A profile is a group/collection of settings and permissions that define what a user can do
in salesforce. Profile controls “Object permissions, Field permissions, User permissions,
Tab settings, App settings, Apex class access, Visualforce page access, Page layouts,
Record Types, Login hours & Login IP ranges. You can define profiles by the user's job
function. For example, System Administrator, Developer, Sales Representative.
Types of profiles in salesforce
1. Standard profiles:
By default, salesforce provides below standard profiles.
● Contract Manager
● Read Only
● Marketing User
● Solutions Manager
● Standard User
● System Administrator.
We cannot delete standard ones
Each of these standard ones includes a default set of permissions for all of the
standard objects available on the platform.
2. Custom Profiles:
Custom ones defined by us.
They can be deleted if there are no users assigned with that particular one.
Activity 1: Recruiter Profile Creation
Objective
Provide recruiters with controlled access to candidate applications, job openings, AI
hiring insights, and daily recruitment activities.
To create a new profile:
· Go to Setup >> type Profiles in Quick Find box >> click Profiles >> clone the desired
profile (Standard User) >> enter profile name: Recruiter Profile >> Save.
· While still on the profile page, click Edit.
· Select the Custom App settings as default for the AI-Powered Recruitment &
Candidate Management System
· Scroll down to Custom Object Permissions and give Read/Create/Edit access for
the following objects:
· Contact (Candidate)
· Candidate_Application__c
· Job_Opening__c
Grant Read-Only access for:
● Reports
● Dashboards
· Set Session Timeout to 2 hours of inactivity.
AI & Agentforce Access:
● Read access to AI-related fields:
○ AI Candidate Score
● No approval or override permissions
· Configure Password Policies as:
· Passwords expire in 90 days
· Minimum password length = 8
· Click Save
Activity 2: Hiring Manager Profile Creation
1. Go to setup >> type profiles in quick find box >> click on profiles >> clone the
desired profile (Standard User Profile) >> enter profile name (Hiring Manager
Profile) >> Save.
2. While still on the profile page, click Edit.
3. Select the Custom App as default:
AI-Powered Recruitment & Candidate Management System
4. Grant Read/Create/Edit/Delete access for:
· Contact (Candidate)
· Candidate_Application__c
· Job_Opening__c
· Reports
· Dashboards
5. Approval Permissions:
· Can approve/reject high salary offers
· Can override AI recommendations
6. AI & Agentforce Access:
Full visibility of AI candidate score
Risk analysis
Hiring recommendations
7. Set Session Timeout: 2 hours
8. Click Save
Milestone 8: Roles & Role Hierarchy
A role in Salesforce defines a user’s record-level data visibility.
Roles control who can see whose records in the organization hierarchy.
In the AI-Powered Job Recruitment & Candidate Management System, roles are
used to ensure:
Recruiters see only their assigned candidates and applications
Hiring managers can see all team recruitment records
Secure and structured access to candidate and hiring data
Activity 1: Creation of Hiring Manager Role
Creating Hiring Manager Role:
1. Go to Quick Find
→ Search for Roles
→ Click on Set Up Roles.
2. Click Expand All and click Add Role under CEO.
3. Enter:
○ Label: Hiring Manager
○ Role Name: Auto populated
4. Click Save.
Activity 2: Creation of Recruiter Role
Creating Recruiter role under Hiring Manager role:
1. Go to Quick Find
→ Search for Roles
→ Click on Set Up Roles.
2. Click the + (Add Role) under Hiring Manager.
3. Enter:
○ Label: Recruiter
○ Role Name: Auto populated
4. Click Save.
Milestone 9:Users
A user is anyone who logs in to Salesforce. Users represent people involved in the
AI-Powered Job Recruitment & Candidate Management System, such as recruiters,
hiring managers, and administrators, who need access to candidate applications, job
openings, and approval processes.
Each user in Salesforce has a user account.
The user account identifies the user, and the user account settings determine what
features, objects, and records the user can access based on their role and profile.
Activity 1: Create Recruiter User
Note: Before Implementing Users first complete Profiles and Roles Milestones.
1. Go to Setup → type Users in the Quick Find box → select Users → click New User.
2. Fill in the following fields:
1. First Name : Recruiter
2. Last Name : User
3. Alias : Give an Alias Name (ex: recru)
4. Email Id : Give your personal Email Id
5. Username : Username should be in the format text@text.text and
must be unique
6. Nick Name : Give a Nickname
7. Role : Recruiter
8. User License : Salesforce
9. Profile : Recruiter Profile
3. Click Save.
Activity 2: creating Hiring Manager user
1. Repeat the steps and create other users using
a. Role : Hiring Manager
b. User license : Salesforce
c. Profile : Hiring Manager Profile
Activity 3: Assign Manager to Recruiter User
1. Go to Setup.
2. Search Users.
3. Open Recruiter User.
4. Click Edit.
5. In the Manager field select Hiring Manager User.
6. Click Save.
Milestone 10: APPROVAL PROCESS
Activity 1: Create an Approval Process for High Salary Candidate Offer
Note:
Before implementing the Approval Process, ensure that the following milestones are
completed:
● Profiles creation (Recruiter, Hiring Manager, Admin)
● Roles hierarchy setup
● Users creation and role assignment
This approval process ensures that candidate job offers with high salary amounts are
reviewed and approved by a Hiring Manager, preventing unauthorized compensation
decisions and enforcing company hiring policies.
1. Create Classic Email Template
This email template will notify the Hiring Manager when a high salary candidate offer is
submitted for approval.
Steps to Create Email Template
● Go to Setup (gear icon on top-right)
● In the Quick Find box, type Email Templates
● Click on Classic Email Templates
● Click New Template
○ You’ll now choose the type of email template you want to create.
Choose the type:
● Text – Plain text (no formatting)
● Click Next
Email Template Information:
Folder Public or private folder (use "Unfiled Public
Email Templates" for now)
Email Template Name High Salary Candidate Offer Approval
Notification
Template Unique Name Auto-filled, or change it (no spaces)
Encoding Leave default (UTF-8)
Subject Candidate Offer Awaiting Salary Approval
Email Body Dear
{!Candidate_Application__c.OwnerFullName
},
A candidate job offer with a high salary has
been submitted for your approval.
Please review the candidate application
details below:
Candidate Offer Details:
● Candidate Name:
{!Candidate_Application__c.Candidat
e__r.Name}
● Job Opening:
{!Candidate_Application__c.Job_Ope
ning__r.Name}
● Experience Level:
{!Candidate_Application__c.Candidat
e__r.Experience_Level__c}
● Proposed Offer Amount:
{!Candidate_Application__c.Offer_A
mount__c}
● AI Candidate Score:
{!Candidate_Application__c.AI_Candi
date_Score__c}
● Application Status:
{!Candidate_Application__c.Applicati
on_Status__c}
Please take the necessary action at your
earliest convenience.
Thank you,
AI Recruitment Management System
2. Create the Approval Process
● In the Quick Find box, type: Approval Processes
● Click on "Approval Processes" under Process Automation
● Click on the object name: Candidate Application
● Click Create New Approval Process → Use Standard Setup Wizard
Step 1: Basic Settings
● Name: High Salary Candidate Offer Approval
● Unique Name: Auto-fills (you can keep it as is)
● Click Next
Step2: Specify Entry Criteria:
1.This defines when the process will be triggered.
● Choose "Criteria are met"
Set:
o Field: Candidate Application→ Offer Amount
o Operator: Greater than
o Value: 1000000
o Field: Candidate Application→Application Status
o Operator: Equals
o Value: Offer Submitted
Click Next
Step 3: Select Approver
Approver Selection
● Choose Automatically assign to approver(s)
● Select Manager of Record Owner
Record Editability
● Select Administrators ONLY can edit records during the approval process
● Click Next
Step 4: Email Template Selection
Approval Assignment Email Template
● Select High Salary Candidate Offer Approval Notification
● Click Next
Step 5: Select Fields to Display on Approval Page Layout
You will see:
● Available Fields (left)
● Selected Fields (right)
Suggested Fields to Display
● Candidate Name
● Job Opening
● Offer Amount
● AI Candidate Score
● Application Status
Use:
● Add (→) button to move fields
● Up / Down arrows to arrange display order
● Click Next
Step 6: Specify Initial Submitters
This defines who can submit records for approval.
Steps
● Search for Owner
● Add Record Owner to Selected Submitters
This allows recruiters (record owners) to submit candidate offers.
● Click Save
Step 7: Final Approval Actions
Open the Approval Process which we have created just now
This defines what happens after approval.
Create Field Update
● Click Add New → Field Update
Field Update Details
Field Value
Name Set Approval Status to Approved
Field to Update Approval_Status__c
New Value
Click Save
Approved
Step 8: Final Rejection Actions
This defines what happens if the approval is rejected.
Create Field Update
● Click Add New → Field Update
Field Update Details
Field Value
Name Set Approval Status to Rejected
Field to Update Approval_Status__c
New Value Rejected
Click Save
Step 9: Create an Approval Step
● Under Approval Steps, Click on New Approval Step
● Give the Name as Step1
● Give the Unique Name as Step1
● Step Number = 1
● Click on Next
● Select All Records Should enter this Step
Step 10: Activate the Approval Process
● Click View Approval Process Detail Page
● Click Activate (top-right)
Milestone 11: Email Templates
Activity1: Create a High Priority Candidate Application Notification Email
Template
Purpose:
Notify the Recruiter when a candidate application is identified as high priority by
AI and requires immediate attention.
1. Go to Setup (gear icon on top-right).
2. In the Quick Find box, type Email Templates.
3. Click on Classic Email Templates.
4. Click New Template.
Choose the type:
● Text – Plain text (no formatting)
● Click Next
Template Name: High Priority Candidate Application Notification
Subject: High-Priority Candidate Application Assigned to You
Body:
Hello {!Candidate_Application__c.OwnerFullName},
A candidate application has been identified as high priority by AI and
requires immediate attention.
Candidate Application Details:
● Candidate Name: {!Candidate_Application__c.Candidate__r.Name}
● Job Opening: {!Candidate_Application__c.Job_Opening__r.Name}
● Experience Level:
{!Candidate_Application__c.Candidate__r.Experience_Level__c}
● AI Candidate Score:
{!Candidate_Application__c.AI_Candidate_Score__c}
● Application Date: {!Candidate_Application__c.Application_Date__c}
Please contact the candidate and proceed with the recruitment process within
24 hours.
Thank you,
AI Recruitment Management System
Click on save
Activity2: Create a High Salary Candidate Offer Approval Email Template
Purpose: Notify the Hiring Manager when a candidate offer with a high salary is
submitted for approval.
1. Go to Setup (gear icon on top-right).
2. In the Quick Find box, type Email Templates.
3. Click on Classic Email Templates.
4. Click New Template.
Choose the type:
● Text – Plain text (no formatting)
● Click Next
Template Name: High Salary Candidate Offer Approval Notification
Subject: Candidate Offer Awaiting Salary Approval
Body:
Hello {!Candidate_Application__c.OwnerFullName},
A candidate offer with a high salary has been submitted for your approval.
Candidate Offer Details:
● Candidate Name: {!Candidate_Application__c.Candidate__r.Name}
● Job Opening: {!Candidate_Application__c.Job_Opening__r.Name}
● Proposed Offer Amount:
{!Candidate_Application__c.Offer_Amount__c}
● AI Candidate Score:
{!Candidate_Application__c.AI_Candidate_Score__c}
● Application Status:
{!Candidate_Application__c.Application_Status__c}
Please review the offer details and approve or reject the request accordingly.
Thank you,
AI Recruitment Approval System
Click on save
Activity3: Create a Candidate Application Approval Outcome Notification Email
Template
Purpose:
Notify the Recruiter (Application Owner) when a candidate offer is approved or
rejected by the Hiring Manager.
1. Go to Setup (gear icon on top-right).
2. In the Quick Find box, type Email Templates.
3. Click on Classic Email Templates.
4. Click New Template.
Choose the type:
● Text – Plain text (no formatting)
● Click Next
Template Name: Candidate Application Approval Status Notification
Subject: Candidate Offer Approval Decision
Body:
Hello {!Candidate_Application__c.OwnerFullName},
The approval process for a candidate offer has been completed.
Application Summary:
● Candidate Name: {!Candidate_Application__c.Candidate__r.Name}
● Job Opening: {!Candidate_Application__c.Job_Opening__r.Name}
● Approval Status: {!Candidate_Application__c.Approval_Status__c}
● Final Offer Amount: {!Candidate_Application__c.Offer_Amount__c}
Please proceed with the next steps in the recruitment process based on the
approval outcome.
Thank you,
AI Recruitment Management System
Click on save
Milestone 12: Email Alerts
Activity1: Create High Priority Candidate Application Email Alert
Purpose:
Automatically notify the Recruiter when a candidate application is identified as high
priority by AI.
Steps:
· In the Quick Find box, search for Email Alerts
· Click on Email Alerts
· Click on Continue
· Click on New Email Alert
· Give the Description as
High Priority Candidate Application Email Alert
· Unique Name will be auto populated
· Select the Object as
Candidate Application
· Select the Email Template:
High Priority Candidate Application Notification
· For Recipient Type select User
Select Recipient: Record Owner
· Click on Save
Activity2: Create High Salary Candidate Offer Approval Email Alert
Purpose:
Notify the Hiring Manager when a high salary candidate offer is submitted for approval.
Steps:
· In the Quick Find box, search for Email Alerts
· Click on Email Alerts
· Click on Continue
· Click on New Email Alert
· Give the Description as
High Salary Candidate Offer Approval Email Alert
· Unique Name will be auto populated
· Select the Object as
Candidate Application
· Select the Email Template:
High Salary Candidate Offer Approval Notification
· For Recipient Type select User
·Select Recipient: Record Owner's Manager
· Click on Save
Note:
Before creating this Email Alert, complete the following:
1. Create Recruiter User.
2. Create Hiring Manager User.
3. Open Recruiter User.
4. Click Edit.
5. In the Manager field select Hiring Manager User.
6. Save.
Otherwise "Record Owner's Manager" will not appear.
Activity3: Create Candidate Application Approval Status Email Alert
Purpose:
Notify the Recruiter when a candidate offer is approved or rejected by the Hiring
Manager.
Steps:
· In the Quick Find box, search for Email Alerts
· Click on Email Alerts
· Click on Continue
· Click on New Email Alert
· Give the Description as
Candidate Application Approval Status Email Alert
· Unique Name will be auto populated
· Select the Object as
Candidate Application
· Select the Email Template:
Candidate Application Approval Status Notification
· For Recipient Type select User
Select Recipient: Record Owner or all the internal user
· Click on Save
Milestone 13: Declarative Automation (Flows)
Activity 1: Record-Triggered Flow – High Priority Candidate Application
Notification
Objective:
Automatically notify the Recruiter (Application Owner) when a candidate application is
identified as high priority by AI.
Trigger Condition:
● AI_Candidate_Score__c ≥ 85
Steps:
1. From Setup, in the Quick Find box, search for Flows.
2. Click New Flow.
3. Select Category: Triggered.
4. Select Type: Record-Triggered Flow.
5. Select Object: Candidate_Application__c.
6. Configure Trigger:
When a record is created or updated.
7. Set Entry Conditions:
8. Field: AI_Candidate_Score__c
Operator: Greater than or Equal
Value: 85
9. Select:
10.Run Every time a record is created and meets the condition requirements.
11. Optimize the flow for Actions and Related Records.
12.Click on the + icon and add Send Email Alert action.
13.Select Email Alert:
High Priority Candidate Application Email Alert
14.Enter the Label as:
High Priority Candidate Application Notification
15.Map RecordId to the Record Id field.
16.Save the Flow and Activate.
Activity 2: Record-Triggered Flow – High Salary Offer Submission for
Approval
Objective:
Automatically submit a candidate offer for approval when a high salary amount is
applied.
Trigger Condition:
● Offer_Amount__c > 1000000
Steps:
1. From Setup, in the Quick Find box, search for Flows.
2. Click New Flow.
3. Select Category: Triggered.
4. Select Type: Record-Triggered Flow.
5. Select Object: Candidate_Application__c.
6. Configure Trigger:
When a record is created or updated.
7. Set Entry Conditions:
8. Field: Offer_Amount__c
Operator: Greater than
Value: 1000000
9. Select:
10.Run Every time a record is created and meets the condition requirements.
11. Optimize the flow for Actions and Related Records.
12.Click on the + icon and add Submit for Approval action.
13.Select Approval Process:
High Salary Candidate Offer Approval
14.Enter the Label as:
Submit Candidate Offer for Approval
15.Map RecordId to the Record Id field.
16.Save the Flow and Activate.
17.
Activity 3: Scheduled-Triggered Flow – Pending Candidate Application
Follow-Up
Objective:
Automatically identify candidate applications that are pending approval for more than 3
days and notify the Recruiter.
Schedule Condition:
● Runs daily
Steps:
1. From Setup, in the Quick Find box, search for Flows.
2. Click New Flow.
3. Select Category: Triggered.
4. Select Type: Scheduled-Triggered Flow.
5. Set the Start Date and Time
(for example: Today, 9:00 AM).
6. Set Frequency: Daily
7. Select Object: Candidate_Application__c
8. Set Condition Requirements:
9. Approval_Status__c Equals Pending
10.Set Additional Condition:
11. LastModifiedDate Less than TODAY() – 3
12.Optimize the flow for Actions and Related Records.
13.Click on the + icon and add Send Email Alert action.
14.Select Email Alert:
Candidate Application Approval Status Email Alert
15.Enter the Label as:
Pending Application Reminder
16.Map RecordId to the Record Id field.
17.Save the Flow and Activate.
Activity 4: Screen Flow – Candidate Application Creation Wizard
Objective:
Provide a guided, user-friendly screen-based process for recruiters to create candidate
applications.
Steps:
1. From Setup, in the Quick Find box, search for Flows.
2. Click New Flow.
3. Select Category: Screen Flow.
4. Click Create.
5. Add a Screen element:
6. Screen Name: Candidate Details
7. Fields:
8. Candidate
Job Opening
Application Date
9. Add another Screen element:
10.Screen Name: Offer Details
11. Fields:
12.Offer Details
13.Offer Amount
14. AI Candidate Score
15.Add a Formula / Assignment:
16.Calculate Final Offer Amount
17.Add a Create Records element:
18.Create Candidate_Application__c record
19.Add a Confirmation Screen:
20.Display:
21.Candidate Application Created Successfully
22.Save the Flow with name:
23.Candidate Application Screen Flow
24.Activate the Flow.
Milestone 14: Agentforce AI
Activity 1: Create Recruitment Assistant Agent
Objective
Create an AI-powered Recruitment Assistant using Agentforce Studio.
Steps
1. Go to Setup.
2. Search for Agentforce Studio.
3. Click Agentforce Studio.
4. Open the Agents tab.
5. Click New Agent.
6. Under Start with a template, select Agentforce Employee Agent.
7. Enter the following details:
8. Agent Name :Recruitment Assistant Agent
9.Click Create.
 Save and Activate
Activity 2: Create Prompt Template – Candidate Application Summary
Objective:
Generate an AI-based summary of a candidate application for recruiters and hiring
managers.
Steps:
● From Setup, search for Prompt Builder.
● Click Prompt Builder.
● Click New Prompt Template.
● Select Prompt Type: Summary
● Select Object: Candidate_Application__c
● Enter Prompt Name:
Candidate Application Summary Prompt
Prompt Content:
You are an AI Recruitment Assistant.
Summarize the candidate application using the available Salesforce record.
Include:
• Candidate Name
• Job Opening
• Experience Level
• AI Candidate Score
• Offer Amount
• Application Status
Provide:
• Candidate Summary
• Candidate Strengths
• Possible Risks
• Hiring Recommendation
Only use the information available in Salesforce.
Do not generate information that is not present.
Click Save and Activate.
Activity 3: Create Prompt Template – Hiring Risk Analysis
Objective:
Help hiring managers understand whether a candidate application is risky or high value.
Steps:
● Go to Prompt Builder.
● Click New Prompt Template.
● Select Prompt Type: Flex
● Select Object: Candidate_Application__c
● Prompt Name:
Candidate Hiring Risk Analysis Prompt
Prompt Content:
● Analyze the candidate application.
●
● Provide:
●
● Candidate strengths
● Candidate weaknesses
● Hiring recommendation
● Risk Level (Low, Medium, High)
●
● Base your recommendation only on the Salesforce record.
●
● Click Save and Activate.
place with
Activity 4: Customize Recruitment Assistant Agent
Objective
Customize the default Employee Agent for recruitment.
Steps
1. Open Recruitment Assistant Agent.
2. Click General FAQ.
3. Replace the default reasoning instructions with:
You are a Recruitment Assistant for the AI-Powered Job Recruitment & Candidate
Management System.
Answer recruitment-related questions.
Help recruiters understand:
• Candidate Applications
• Job Openings
• AI Candidate Score
• Application Status
• Offer Amount
Provide hiring recommendations only from available Salesforce information.
If information is missing, ask the user for clarification.
Never create or assume information that does not exist in Salesforce.
4. Click Save.
Activity 5: Test Recruitment Assistant Agent
Objective
Verify that the Recruitment Assistant Agent responds to recruitment-related
questions.
Steps
1. Open the Recruitment Assistant Agent.
2. Click Preview.
3. Ask:
What can you do?
How can you help recruiters?
How do I evaluate a candidate application?
4. Verify that the agent responds correctly.
Expected Result
The Recruitment Assistant Agent provides recruitment guidance and asks
follow-up questions when additional information is required.
Note:
The default Agentforce Employee Agent provides general AI assistance based on its configured
instructions and available knowledge.
In a standard Salesforce Developer Edition, the agent may not automatically retrieve data from
custom objects such as Candidate Application or Job Opening without additional Agentforce
configuration or Data Cloud capabilities.
If the agent asks for more information instead of summarizing a record, this is expected behavior
unless additional grounding or custom actions have been configured.
Milestone : The Lightning App
Activity 1: Create a Lightning App for “AI-Powered Recruitment &
Candidate Management System”
“From Setup, enter App Manager in the Quick Find and select App Manager.
1. Click New Lightning App.
2. Enter AI-Powered Recruitment & Candidate Management System as the App
Name >> Click on upload image and add an image related to AI-Powered
Recruitment & Candidate Management System then click next
3. Under App Options, leave the default selections and click next.
4. Under Utility Items, leave as is and click Next.
5. From Available Items, select
Candidate Applications
Candidates (Contact)
Job_Opening__c
Accounts
Reports
Dashboards
and move them to the Selected Item and Click Next.
6. From Available Profiles, select System Administrator, Recruiter, Hiring
Manager and move it to Selected Profiles.
7. Click Save & Finish.
Milestone 15 -Editing of Page Layouts
Activity 1: To edit a Page Layout in Candidate_Application__c Object
1. Go to setup >> click on Object Manager >> type object name
(Candidate_Application__c) in quick find box >> click on the Candidate
Application object >> Page Layouts.
2. Click on the Candidate Application Layout.
3. Drag and arrange the field as shown below.
● Candidate
● Job Opening
● Application Date
● AI Candidate Score
● Offer Amount
● Application Status
● Approval Status
4. Click on Save.
Activity 2: To edit a Page Layout in Job_Opening__c Object
1. Go to setup >> click on Object Manager >> type object name (Job Opening)
in quick find box >> click on the Job Opening object >> Page Layouts.
2. Click on the Job Opening Layout
3. Drag and arrange the field as shown below
● Job Title
● Department
● Salary Range
● Vacancies
● Job Status
4. Click Save.
Activity : To edit a Page Layout in Contact Object
1. Go to setup >> click on Object Manager >> type object name (Contact) in
quick find box >> click on the Contact object >> Page Layouts.
2. Click on the Contact Layout
3. Drag and arrange the field as shown below
● Name
● Candidate ID
● Email
● Phone
● Experience Level
Click Save
Milestone 15 - Dynamic Forms
Activity 1: To create a Dynamic Form in Candidate Application Object
1. Go to setup >> click on App Launcher >> Open “AI-Powered Recruitment &
Candidate Management System” App >> click on the Candidate Application
object tab>> Open an existing Candidate Application record.
If no records exist, create one and save it.
2. Click on the record created and click on the Gear icon on the top right corner
and Select Edit Page.
3. Click on the Details section and on the right pane click on Upgrade Now to
enable Dynamic Forms for the object.
4. Select Candidate Application PageLayout and Click on Finish.
5. Click on Save and Click on Activate.
6. Click on Org as Default, select Desktop and Phone, click Next and Click Save.
7. Repeat the same steps for:
• Job Opening
• Contact
