# sharepointonlineinterviewqanda

1. What is SharePoint?
SharePoint is a platform developed by Microsoft which is being widely used to share, communicate, store and collaborate the content, documents, and records.
2. Why do we use SharePoint?
It provides various features like
we can easily share the content with the users
storing and managing data
easy to manage user access
we can build workflows to easy the business processes
3. What is SharePoint List?
SharePoint list is a collection of records related to an entity. These records in the list are termed as items. SharePoint list provides a feature to add a different type of fields which are termed as list columns.
4. What is the SharePoint Document Library?
A document library allows users to easily store, upload, share, collaborate, and track documents or files. Similar to lists, we can create columns in a document library which represents the metadata for the uploaded documents.
5. What is a Content type?
According to Microsoft, A content type is a reusable collection of metadata (columns), workflow, behavior, and other settings for a category of items or documents in a SharePoint list or document library. Content types enable you to manage the settings for a category of information in a centralized, reusable way.
Also check detailed article: Content types in SharePoint.
6. What is Site column?
According to Microsoft, “A site column is a reusable column definition, or template, that you can assign to multiple lists across multiple SharePoint sites. Site columns are useful if your organization wants to establish some consistent settings across lists and libraries.”

Also check detailed article: Site columns in SharePoint
7. What is Check-out?
When any user check-out the document, no one else can edit that document unless it is checked-in back by that previous user. At a time only one user can check-out the file. During the check-out period, other users can open the document in read-only mode.

In case any user forgot to check-in the document, the site collection administrator has privileges to take the ownership of those checked-out documents.
8. What is Check-in?
When a user check-in the document, the changes made in the document will be visible by other users. Once the file is check-in, it can be check-out by other users.
9. What is the difference between SharePoint 2010 and SharePoint 2013?
SharePoint 2010	SharePoint 2013
1. Normal user interface. Less UI friendly than SharePoint 2013

1. Enhanced with user-friendly look and feel

2. Less social features, sandbox solutions.

2. The version adds few new exciting features such as Social Feed, SharePoint Apps and cross-site publishing.

3. No minimal download strategy available

3. Introduced minimal download strategy feature

4. Search – SharePoint 2010 had Introduced Integrated FAST search as an Enterprise search. In addition to this build-in SharePoint search is still widely used in companies.

4. Search - SharePoint 2013 includes several enhancements, custom content processing with the Content Enrichment web service, and a new framework for presenting search result types. Some of the features added are

- Consolidated Search Results
- Rich Results Framework
- keyword query language (KQL) enhancements


10. What is the difference between SharePoint 2013 and Sharepoint 2016
Features	SharePoint 2013	SharePoint 2016
Content DB size	200 GB	1+ TB
Site collection per database	5,000	1,00,000
App launcher	No	Yes
Upload file size	2GB	10GB
Zero downtime patching	No	Yes
Automatic management of indices (indexed columns). This help in 5000 item limit issue. No need to worry about the threshold.	No	Yes

11. What is the Minimal Download Strategy (MDS)
Minimal Download Strategy (MDS) is a new technology in SharePoint that reduces the amount of data that the browser has to download when users navigate from one page to another in a SharePoint site. When users browse an MDS-enabled site, the client processes only the differences (or delta) between the current page and the requested page.

See more here: Minimal Download Strategy overview
12. What is App-model in SharePoint?
As SharePoint is moving towards the cloud, Microsoft wants developers to stop developing sandbox solutions. Now to develop custom applications, the app model is introduced where developers can create either SharePoint hosted apps or autohosted apps. These apps can easily adapt to the change of SharePoint versions and do not harm the SharePoint environment.

Sharepoint apps are also called as SharePoint add-in. A SharePoint Add-in is a self-contained piece of functionality that extends the capabilities of SharePoint websites to solve a well-defined business problem.

tags: SharePoint Interview Questions
13. Why App model is introduced in SharePoint 2013?
a) We know that in 2010, sandbox solutions were introduced to remove issues related to full trust farm solutions which we were using in 2007.

All code in full trust app runs in SharePoint's own server process. Any corruption has the potential to crash the entire farm.

b) To avoid these issues, Microsoft introduced sandbox solutions in 2010. Sandbox apps do not run with full trust and cannot elevate their privileges.

They run in the separate isolated process to prevent them from corrupting servers farms own process

c) Sandbox apps are deployed and managed at the site collection level and can access resources within a local site collection, They cant access resources within farm not even by using Client object model.

d) The code in sandbox solution still runs in SharePoint farms thus poorly written ones can still affect performance.

e) Sandbox solution that corrupt their own memory or use too many resources may be restarted automatically further reducing server resources.

To avoid all these issues, Microsoft introduced App model in SharePoint 2013.

tags: SharePoint Interview Questions
14. What are SharePoint hosted apps?
SharePoint hosted apps are those apps, where all the components are hosted on  SharePoint only.

SharePoint-hosted apps are installed on a SharePoint website, called the host web. They have their resources hosted on an isolated subsite of a host web, called the app web.
15. What are Provider-hosted apps?
Provider-hosted apps for SharePoint include components that are deployed and hosted outside the SharePoint farm.

They are installed to the host web, but their remote components are hosted on another server. i.e. App web for provider hosted apps is completely a different server (provider).
16. What is the difference between Sharepoint-hosted apps and Provider-hosted apps?
SharePoint hosted apps

Provider-hosted apps

No server-side code, 100% client-side code

Server-side coding is used. Managed code and high trust

Can be developed using HTML5, CSS, JavaScript, jQuery, ASP.NET Ajax, CSOM, REST API, Silverlight, KnockOut JS, Angular JS

Any programming language can be used

Data Storage Locations: SharePoint Online, Content Database

Data Storage Locations: ISV Storage, Azure Storage, Content Database.

(ISV - Independent Software Vendors)

Can be hosted on either SharePoint on-premises or office 365

Deployed outside the SharePoint farm


17. What is the difference between SharePoint Online and SharePoint On-premise?
Online	On-premise
1) No need of hardware to buy. All updates and patches are taken care by Microsoft	1) Resource requirement: you need more resources to maintain the server, to add updates and patches. This means a requirement of more people and hardware.
2) Information stored in the cloud	2) Information lies in your local environment
3) Cost is less and is billed monthly per user.	3) Cost is more as it requires more resources, hardware, and maintenance
4) Powershell control is reduced as compared to on-premise.	4) More PowerShell control

18. What is the difference between SharePoint 2010 workflow and 2013 workflow?
2010 Workflows	2013 Workflows
1) .net version 3.5	1) .net version 4.0
2) Workflows are hosted by SharePoint itself.	2) Workflows are hosted outside SharePoint on Azure.
It runs as a separate service, and communication of workflow with SharePoint will happen via REST/ CSOM or OAuth.
3) Workflow data is stored in the content database	3) Workflow definitions reside within SharePoint and the actual workflow is stored on windows azure.
4) Issues with scale and large deployments	4) As workflow are decoupled from SharePoint runtime, it provides better scalability, stability, and transparency
5) Only 2010 workflows	5) Both 2010 and 2013 workflows are available
6) Fewer actions as compared to 2013	6) Added new actions like loops, stages, etc. State-machine workflows feature.



19. What are Event Receivers?
The event receiver is simply a method that is called when a triggering action occurs on a specified SharePoint object.

Two types of event receivers:

a) Synchronous: Events are executed before the action is executed on the content database.

b) Asynchronous: Events are executed after the action is executed on the content database.
20. Difference between event receiver and workflow?
Event receiver	Workflows
1) Can be executed before or after an operation	1) Can be executed only after the operation
2) Cannot be run manually	2) Can run manually
3) You can cancel the operation like adding an item	3) You cannot cancel the action as the item is already added.
4) You can create an event receiver only in Visual Studio	4) You can use any tool like SharePoint designer, Visual Studio, Visio, 3rd party apps, etc.
5) No UI interaction	5) Can use forms like initiation form, association form, etc.
6) Can be run for a very short period of time.	6) Can run for days, weeks or even years.
7) Will not survive after server reboots	7) Will survive after server reboots


21. What is the Timer job?
A timer job is a periodically executed task inside a SharePoint server. It provides us with a task execution environment.
22. What is REST API in SharePoint?
REST is an architectural style (general and reusable solution) providing standards between computer systems on the web, making them easier to communicate with each other.

SharePoint REST API is an interface which allows communication between the SharePoint server and client machine.

Using SharePoint REST APIs, users can interact remotely with SharePoint data by using any technology that supports REST web requests.

Also check details article: SharePoint REST API
23. What is JSON?
JSON stands for JavaScript Object Notation. It is a lightweight data-interchange format. Also, it is "self-describing" and easy to understand. JSON is language independent. As a result, you can use JSON in any language code like Javascript, C#, etc.
24. Why JSON is lightweight?
We can say JSON is lightweight than XML because it uses less amount of characters to represent the data. i.e. JSON is less verbose. As a result, the data can be sent/retrieved at a faster rate.

For example, consider below example:
?
1
2
3
4
5
6
7
8
9
10
11
12
XML:
<person>
      <first-name>Mayuresh</first-name>
      <last-name>Joshi</last-name>
</person>
 
********************************************
JSON:
{
      "firstname":"Mayuresh",
      "lastname":"Joshi"
}
Here you can see, XML takes more characters than JSON to represent the same amount of data. As a result, XML is more verbose than JSON. Read more here.
25. Name some actions used in Nintex workflows?
Assign flexi task: Can have a custom outcomes
Assign to do task: has only two outcomes, approve and reject.
Build string
Calculate date
Call web service
Collection operation
Commit pending changes
Create item
Create item in another site
Create list
Create site
Create site collection

26. Name some actions used in SharePoint Designer workflow?
Assign a task: is used to create a SharePoint task and assign it to a single participant.
Start a task process: is used to assign a task to multiple participants.
Wait for Event in List Item: Used to wait for a new item to be created or an item to be changed.
Wait for Project Event: Used to wait for a project to be checked in, committed, or submitted.
Wait for Field Change in Current Item: Used to wait for a field to be changed in the current item.

27. How can we copy documents from one document library to other using designer workflow?
We have an action in the designer workflow which can be used to achieve this requirement. That action is Call HTTP Web Service
28. What is SharePoint Framework (SPFx)?
The SharePoint Framework (SPFx) is a page and web part model that provides full support for client-side SharePoint development, easy integration with SharePoint data, and support for open source tooling.

With the SharePoint Framework, you can use modern web technologies and tools in your preferred development environment to build productive experiences and apps that are responsive and mobile-ready from day one. The SharePoint Framework works for SharePoint Online and also for on-premises (SharePoint 2016 Feature Pack 2 and SharePoint 2019).

See more: Overview of the SharePoint Framework
29. What is JSOM?
JSOM or JavaScript Object Model is a set of .js files built for ECMAScript-enabled platforms. The main .js files that are available are:
SP.js
SP.Core.js
SP.Ribbon.js
SP.Runtime.js
These files are deployed in the SharePoint15_Root\TEMPLATE\LAYOUTS directory. The default master pages of SharePoint define a ScriptManager control, which automatically includes references to these .js files. You could also reference them by yourself.
30. What is CSOM?
CSOM stands for Client Side Object Model. CSOM runs as an application on a client (think a .exe) or as code inside IIS (provider hosted add-in). It is written in C#.
31. What is SSOM?
SSOM stands for Server Side Object Model. It is written in C#. We use the SharePoint Server Object Model when we are writing code that will run inside the context of SharePoint. Some common examples would be the code-behind in a page or a web part, event handlers behind a feature or a list, timer jobs etc.
32. Difference between JSOM and CSOM?
CSOM is written in C#, JSOM in JavaScript. CSOM runs as an application on a client (think a .exe) or as code inside IIS (provider hosted add-in) whilst JSOM runs in the browser (think a .JS file embedded in a HTML/aspx page).

One other major difference: CSOM calls need to be authenticated (with Oauth) while JSOM calls are automatically authenticated with the user's identity since it is JS code running in the browser.

CSOM is client-side object model which is comprised of C# client side coding(Microsoft.sharepoint.client.dll), JavaScript client-side coding(sp.js) and Silverlight. JSOM OR ECMAScript are same and CSOM coding which is done in JavaScript is called JSOM.
33. What is Content Type Hub (CTH) in SharePoint?
Content Type Hub is a central location where you can manage and publish your content types – so now web applications can subscribe to this hub and pull down the published content types from the hub.
34. What is visual web parts?
Microsoft SharePoint 2010 introduced Visual Web Parts. Visual Web Parts are similar to user controls in that you can simply drag and drop items from the Toolbox onto your custom controls to create a Web Part UI. You also get the code-behind file where you implement the UI logic. Technically, the SharePoint 2010 Visual Web Part is an ASCX web user control that is hosted inside a standard Web Part.

A Visual Web Part is simply a classic Web Part that automatically loads the web user control with it. The advantage of this approach is that you can use Visual Web Developer to design the web user control. Traditional Web Parts differ from Visual Web Parts in several ways.
35. Name some out of the box webparts in SharePoint.
List view webpart
Search webaparts
Script editor webpart
Content editor webpart

36. 'select', 'orderby', 'filter', 'top' operation in REST API?
Selecting columns:
/_api/web/lists/getbytitle('employee')/items?$select=ID,Title,Employee,company

Order by:
Ascending:
/_api/web/lists/getbytitle('employee')/items?$select=ID,Title,Employee,company&$orderby= Employee asc 

Descending: 
/_api/web/lists/getbytitle('employee')/items?$select=ID,Title,Employee,company&$orderby= Employee desc

Filtering items:
Filter by Title: 
/_api/web/lists/getbytitle('employee')/items?$filter=Employee eq ‘Mayuresh' 

Filter by ID:
/_api/web/lists/getbytitle('employee')/items?$filter=ID eq 12 

Filter by Date: 
/_api/web/lists/getbytitle('employee')/items?$filter=Start_x0020_Date le datetime'2019-01-19T10:19:32Z' 

Multiple Filters: 
/_api/web/lists/getbytitle('employee')/items?$filter=( Modified le datetime'2019-01-19T10:19:32Z') and (ID eq 12) 

Title name starts with the letter M: 
/_api/web/lists/getbytitle('employee')/items?$filter=startswith(Title,‘M’) 

Return all items from the 'employee' list modified in August:
/_api/web/lists/getbytitle('employee')/items? $filter=month(Modified) eq 8

Paging items:
/_api/web/lists/getbytitle('employee')/items?$top=100
37.Dealing with Lookup field using REST API

When creating a lookup field, you can select which field from source list you want to show. The number of such fields is limited by field type. For example, you can create a lookup with lookup field pointed only to the following field types:

Single line of text
Date and Time
Number 
Thus in your REST query, you can select additional fields only with above-mentioned field types. For example, you have a list Category with fields Title, Id, Active (custom Yes\No field). You created a lookup to Category in your other list (employee).

/_api/web/lists/getbytitle('employee')/items?$select=category/Id,category/Title&$expand=category - works 

and  

/_api/web/lists/getbytitle('employee')/items?$select=category/Id,category/Title,category/Active&$expand=category - doesn't work because Yes\No is unsupported field type for lookup.
38. Data Loss Prevention Policy in SharePoint?
With a data loss prevention (DLP) policy in the Office 365 Security & Compliance Center, you can identify, monitor, and automatically protect sensitive information across Office 365.

It helps in:

Identify sensitive information across many locations, such as Exchange Online, SharePoint Online, and OneDrive for Business. Prevent the accidental sharing of sensitive information.
39. How to create Birthday wishes workflow in sharepoint designer?
You basically need 2 workflows that will end up triggering each other to create a loop.

The workflows would check to see if the date the workflow is being executed is the same as the birthday. If it is, email the user, if it isn't wait 24 hours, update a trigger field in your list and end. This updating of the trigger will cause the other workflow to start and do the same thing.

In SP 2013, there will be loop actions, so this should finally be easier to accomplish.
40. Difference between "Assign to do task" and "Assign flexi task" in Nintex?
"Assign to do task" has two fixed outcomes, either Approve or Reject. But, we can add custom outcomes in "Assign flexi task" action.
41. What is the difference between Content Editor & Script Editor Webpart in SharePoint?
Content editor webparts can be exported while Script Editors cannot be exported by default.

In Script Editor Web Part we can paste html and JavaScript only. In Content Editor webpart we can add html, JavaScript, formatted text, tables, hyperlinks, and images also.

In Content Editor webpart, we can give a link to the file uploaded in a document library. In Script editor webpart we do not have such option.

For detailed explanation, refer this article: Difference between Content Editor & Script Editor Webpart
Unanswered Questions:

40. What is Request Digest in REST API?

41. What is eTag in REST API?

42. Difference between JSOM and REST API?

43. Is REST API only developed for SharePoint?

44. How can we access SharePoint data from Other applications (e.g. Java Application). How the authentication will happen in that case?

44. What are the ways to provide RunWithElevated access?

45. What files are needed when we use JSOM

46. Can designer be replaced with Microsoft flow?

47. What are azure web jobs?

48. Difference between webjobs and event receivers?

49. What is cross-site publising?

50. Difference between load and load.query?

51. What do you know about Search in SharePoint?

52. What is OAuth?

53. What is promise function in jQuery?

54. Name some features available in SharePoint?

55. How to edit master pages in SharePoint?

56. What are remote event receivers?

57. How to fetch more than 5000 items using REST API?

58. How to configure Search Webparts?

59. What is term store management?

60. What is the managed metadata?

61. What is the difference between Classic and Modern pages in SharePoint?
