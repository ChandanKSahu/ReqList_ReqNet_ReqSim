

Software Requirements Specification

for the

Management Processes

of an

Integrated Library System


Prepared by the PINES Reports Working Group:

LaToya Davidson, Twin Lakes Library System
Jennifer Durham, Statesboro Regional Library System
Dana Peeler, Ohoopee Regional Library
Susan Sexton-Cooley, Sara Hightower Regional Library
George Tuttle, Piedmont Regional Library

Katherine Gregory & Chris Sharp, PINES Staff Facilitators

August 7, 2009

[Based on Version 3.0 final of “Software Requirements Specification for the Management Processes of an Integrated Library System” prepared by Lori Ayre and Lucien Kress, Galecia Group, January 27, 2009]
 
Table of Contents
1. Introduction........................................................................................................................................	3
1.1 Purpose and Perspective ............................................................................................................................	3
1.1a Formation and Mission of PINES Reports Working Group……………………………………………………………………	4
1.2 Product Scope and Features ......................................................................................................................	4
1.3 Intended Audience .....................................................................................................................................	4
1.4 Document Conventions...............................................................................................................................	5
1.5 User Classes and Characteristics.................................................................................................................	5
1.6 Operating Environment ..............................................................................................................................	5
1.7 Design and Implementation Constraints ....................................................................................................	6
1.8 User Documentation...................................................................................................................................	6
1.9 Assumptions and Dependencies..................................................................................................................	6
2. System Requirements..........................................................................................................................	7
2.1 Management Tools: General ......................................................................................................................	7
2.2 Management Tools: Demographics.............................................................................................................8
2.3 Management Tools: Inventory Control .......................................................................................................9
2.4 Management Tools: Patron Records .........................................................................................................	10
2.5 Management Tools: Transaction Records..................................................................................................	11
2.6 Management Tools: Financial Records.......................................................................................................	11
 
1. Introduction

1.1 Purpose and Perspective
A program of the Georgia Public Library Service, Georgia Library PINES (Public Information Network for Electronic Services) is the public library automation and lending network for more than 275 libraries and affiliated service outlets in almost 140 counties.  PINES creates a statewide "borderless library" that provides equal access to information for all Georgians. Georgians with a PINES library card have access to materials beyond what is available on their local shelves and enjoy the benefits of a shared collection of 9.6 million books and other materials that can be delivered to their home library free of charge.  PINES has been running its shared bibliographic and patron databases on the Evergreen ILS, which was originally developed by the Georgia Public Library Service for use in PINES.
This Software Requirements Specification (SRS) describes the functional and nonfunctional requirements for Management Processes of an Integrated Library System (ILS). The requirements, while originally developed specifically for King County Library System, have been adapted for the Public Information Network for Electronic Services (PINES) as they are believed to be suitable for many large, urban, multiple-branch, centralized library systems. 
The requirements in this SRS presuppose the general data structures and functionality of a full-fledged ILS. The Management Processes will replace and enhance the current capabilities of Evergreen, as well as add new functionality. 

1.1a Formation and Mission of PINES Reports Working Group
The PINES Reports Working Group was formed in response to a need to make recommendations for improvements of the Evergreen ILS reports interface.  King County (Washington) Library System, in collaboration with the Galecia Group, had already developed a software requirements specification for a reports interface and PINES staff took the opportunity to build a PINES-specific requirements document on that foundation.  Katherine Gregory, PINES Services Specialist, requested group members from the existing PINES Reports Subcommittee, and included PINES library directors in a call for volunteers.  The resulting PINES Reports Working Group consists of one library director, three assistant library directors, and a systems librarian, all of whom have significant experience developing reports for PINES libraries.  The mission statement of the PINES Reports Working Group is as follows:
 
Reports Working Group Mission:
Document optimal Reports functionality within a future Evergreen release and develop a list of requirements.
Become the Reports testing group, through which all new Reports development would be filtered.
Compile a list of reports needed for an Executive Reports Interface.
Determine and create templates needed for all PINES libraries.
1.2 Product Scope and Features
The Management Processes facilitates the management of Library services, programs, and policies. Specifically, the Management Processes support the following activities, among others: 
o	Analyzing the Library collection and its use by patrons. 
o	Analyzing branch capacity and optimal distribution of the collection. 
o	Analyzing the demographics and interests of the Library’s patrons. 
o	Analyzing staff productivity and workflow. 
o	Tracking and verifying financial transactions. 
The current specification presupposes the general functionality of an ILS and specifies only those requirements that directly or indirectly relate to management activities. PINES is currently working on specifications for Acquisitions and Cataloging modules.
Moreover, the current specification is focused on functional characteristics of Management Processes. Data structures and user interfaces will require further specification and development using an iterative, prototype-oriented software development methodology. 
1.3 Intended Audience
This SRS is intended both for library managers and staff who may contribute additional requirements or commentary, and for software project managers and developers who will implement the requirements. As such, it aims for a high level of readability for a non-technical audience, while providing enough specificity to be useful to a software developer.  
It is assumed that when software development occurs, it will be in a highly collaborative and iterative environment in which end-users have multiple opportunities to review prototypes and refine the user interface and software functionality. 
It is also assumed that the reader has a general understanding of Library services and processes and does not require definition of common Library terminology. 
1.4 Document Conventions
The SRS includes requirements. Requirements include a reference to a process flowchart where appropriate. Flowcharts generally indicate the current approach to Management Processes in PINES, and should be considered to give contextual information rather than to prescribe or constrain new software development. 

1.5 User Classes and Characteristics

Patron		A Patron is a resident of the State of Georgia, either possessing a library card or not, utilizing the resources of a PINES member library.
Staff		Staff includes paid employees of PINES member libraries who are involved in designing and providing services for the Library.
Local System Administrators		Local System Administrators include management staff who oversee Library processes.
Library Managers		Library Managers supervise a single organizational unit and provide input to the design and implementation of Library services.
Library Directors		Library Directors include members of the Library Executive Team who plan and direct Library services and priorities
Global System Administrator		Global System Administrators manage PINES at the consortium level, implementing software changes and configurations, and generating statistical reports for PINES as a whole.
1.6 Operating Environment
OE-1:	Management Processes support the needs of a large, multiple-system library consortium and its individual component systems and branches. Specifically, the system must support a library consortium with 286 locations, 17 million annual circulations, purchasing and processing over 900,000 items per year. It is highly desirable that searches and reports can be processed during open hours without disrupting other system functions. 
OE-2:	Management Processes shall operate on a Linux or Solaris server.
OE-3: 	Management Processes shall be accessible through a web-browser or a Windows-compatible client.
OE-4: 	If web-browser based, Management Processes shall be accessible through Microsoft Internet Explorer (v.6.0 and later) and Mozilla Firefox (v.2.0 and later). 
OE-5:	 Management Processes shall be accessible with screen-reading software, screen-magnification software, and other software programs designed to increase accessibility. 
 
1.7 Design and Implementation Constraints

CO-1:	Management Processes shall use a fully relational database back-end. 

CO-2:	Management Processes shall produce standards-compliant HTML. 

CO-3:	Management Processes shall provide a development and training environment with the ability to migrate configurations to a production environment.

CO-4: 	User rights and privileges will be controlled through security groups and/or “roles” that allow access control for individuals, workgroups, and arbitrary staff groups. 

CO-5:	These requirements shall not constrain functionality or features of the Online Public Access Catalog (OPAC) module. 

1.8 User Documentation
UD-1	The software developer shall provide complete data specifications for authority records, bibliographic records, order records, item records, hold/request records, and other records maintained or accessed by Management Processes. 

UD-2:	The software developer shall provide a thorough high-level description of major processes, including bibliographic record import and export, validation of bibliographic records against internal and external authority sources, and standard reports. 

UD-3:	The system shall provide an online, hierarchical, and cross-linked help system in HTML that describes and illustrates all system functions. 

UD-4:	The system shall provide thorough high-level error reporting and feedback and shall allow low-level query-specific feedback for Local and Global System Administrators from the front-end interface.

1.9 Assumptions and Dependencies
AS-1:	Management Processes are part of an enterprise-level Library Automation System. 
AS-2:	Management Processes are consolidated at a central location, and accept input and provide services to multiple locations. 
DE-1:	Management Processes rely on the data structures and functionality of an enterprise-level Library Automation System, including Acquisitions and Cataloging modules. 
DE-2:	Management Processes interface with a variety of vendor websites, via published APIs and/or automated transfer of standard-format data files (e.g. USMARC21, EDIFACT). 
DE-3:	Management Processes interact with a patron interface, also known as an Online Public Access Catalog (OPAC).
 
System Requirements
Category: Management Tools: General
Req ID: PINES-001 Priority: 1
Name: streamlined staff login
Description: The system supports (but does not require) streamlined staff login methods, for example staff member swipes a card to log into a terminal or the staff member logs into a terminal by using his/her individual login and password.
Source: Reports Working Group (RWG)

Req ID: PINES-002 Priority: 1
Name: report templates
Description: System administrators can create reliable report templates that are available to staff, and can be run as is or modified to the staff person's particular needs. Changes in the templates could be done without comprising the results. The administrator can limit the filters and display fields that can be altered to certify a dependable output. For example, front-line staff could set the call number range for a weeding report or add or remove designated display fields from a pick list, but couldn’t alter the template to display deleted items.
Source: RWG

Req ID: PINES-003 Priority: 1
Name: reports permissions
Description: System provides distinct, fine-grained permission levels limiting who can create and clone reports. All permissions should be easy to administer. System administrators can create shared folders to allow or disallow staff to run specific reports, and/or to run ad hoc reports on specific sets of data.
Source: RWG

Req ID: PINES-004 Priority: 1
Name: query tool
Description: System provides a user-friendly interface for designing queries against all record types. Staff can select fields to query; select values from picklist of possible values; select regular expressions from drop-down menu, and use a full range of Boolean operators. Administrators control staff access to tables and fields.
Source: RWG

Req ID: PINES-005 Priority: 1
Name: board reports
Description: The system provides pre-defined reports for consumption by library boards or other consumers. There will be reports providing basic statistics like those required by the Georgia Annual Report and Application for State Aid and activity reports that indicate traffic and volume of use that display statistics on check-outs, check-ins, holds placed, and holds filled. It should be possible cross-tabulated per terminal, per branch, per library system, per hour, per patron age range, per patron type, and per patron location.
Source: RWG

 
Req ID: PINES-006 Priority: 1
Name: transaction data archive
Description: Transactions are archived in a form that protects patron privacy as defined by State Law, while providing useful demographic statistics.
Source: RWG

Req ID: PINES-007 Priority: 1
Name: periodic reports, examples
Description: Examples of periodic reports: bibliographic records with holds; items that have not been checked out in X days; item-level holds; items with invalid item type; in-transit items with outstanding hold; items that have been in-transit for more than X days; items that are the last copy in the
system; items with a long call number; missing items; bibliographic records with no item records; patrons with invalid home library.
Source: RWG

Req ID: PINES-008 Priority: 1
Name: Query selections
Description: System provides the query selections along with the results.
Source: RWG

Req ID: PINES-009 Priority: 1
Name: Reports queuing 
Description: Ability to see where your report is in the queue of reports waiting to run.
Source: RWG

NOTE:  Req IDs PINES-010 and PINES-011 refer to Appendix A & B, which were developed based on working knowledge of Evergreen ILS version 1.4.0.4 and terms in those appendices refer to specific aspects of that product.

Req ID: PINES-010 Priority: 1
Name: PINES-Specific Reports Examples
Description: System must be able to support the reporting definitions as described in Appendix A.
Source: RWG

Req ID: PINES-011 Priority: 1
Name: PINES-Specific Fine-Grained Requirements
Description: System must be able to support the fine-grained reports requirements as described in Appendix B.
Source: RWG 

Category: Management Tools: Demographics
Req ID: PINES-012 Priority: 1
Name: behavior and use analysis
Description: The system produces statistics that can be used to understand and predict patron behavior and use of materials. For example, how quickly is a particular book returned, on average? How likely is a particular book to be renewed? What percent of check-outs at a particular branch are renewals?
Source: RWG
Req ID: PINES-013 Priority: 1
Name: demographic statistics
Description: The system produces useful demographic statistics, including transactions by geographical regions, age ranges, etc. The data used to produce these statistics must be anonymized, i.e. information that could be used to identify a patron is deleted.
Source: RWG

Category: Management Tools: Inventory Control
Req ID: PINES-014 Priority: 1
Name: material volume report
Description: Ability to report on the volume of material in a given library at any point in time, based on new acquisitions, items on the shelf, and items out in circulation, with the ability to break down volume in categories (e.g. total items in library, number of holds, number of adult fiction, number of board books, etc).
Source: RWG

Req ID: PINES-015 Priority: 1
Name: system capacity interface
Description: The system provides an interface showing capacity of all branches (as defined in PINES-014).
Source: RWG

Req ID: PINES-016 Priority: 1
Name: shelf space report
Description: For each genre and format of material, ability to compare the percentage of total circulations, the percentage of the collection, and the percentage of total shelf space that genre/format comprises. Ability to report per library and per system.
Source: RWG

Req ID: PINES-017 Priority: 1
Name: uncataloged material
Description: Ability to control inventory of uncataloged material, such as paperback books and children's board books. Support for quick distribution; minimal branch labor; and ability to identify how the material is being used. Ability to count transactions and include in circulation statistics
and reports.
Source: RWG

Req ID: PINES-018 Priority: 1
Name: item transfer utility
Description: System provides a utility for transferring batches of items between branches, used for example to move books into a mobile library, an outreach program collection, or a "just-in-time" warehouse. Utility includes ability to query for candidate materials; ability to save queries for repeated use; ability to manually select titles from query results; and ability to change records of all or selected items to move to new location. Mechanisms for moving items include changing location field, generating pull lists, etc. In addition, utility provides means to revert items to original location after a set period of time, and/or based on other criteria.
Source: RWG
Req ID: PINES-019 Priority: 1
Name: missing and damaged items report
Description: The system provides reports of missing and damaged items per branch.
Source: RWG

Req ID: PINES-020 Priority: 1
Name: in-transit items report
Description: The system generates a list of items that have been in-transit for more than X days (X configurable), per branch and per system.  The report would merge the transit to and transit from into one report for ease of front-line staff use.
Source: RWG

Req ID: PINES-021 Priority: 1
Name: item record purging
Description: The system provides a utility and reports for identifying item records to purge, based on customizable criteria such as: an item has been in status "missing" for more than X months; an item has status "discard/weed". The system has a report to assist in the conversion of items from one status to another. The system provides a last copy report that would single out a library system's last copies, to assist catalogers who need to edit WorldCat entries. The system provides a quick effective method
of deleting volume entries along with copy entries, as well as records with no items attached.

Req ID: PINES-022 Priority: 1
Name: deletions
Description: Ability to count and track record deletions (e.g. item records, patron records) per location and per system.
Source: RWG

Category: Management Tools: Patron Records
Req ID: PINES-023 Priority: 1
Name: patron characteristics
Description: Queries and reports can be limited or grouped by various patron characteristics, including: age range, zip code, county of residence, home branch, patron type, and preferred language.
Source: RWG

Req ID: PINES-024 Priority: 1
Name: inactive patrons report
Description: The system generates a list of patrons with no circulation or electronic activity in the last X days (X configurable).  List should be configurable to System, Home Library, County, etc.
Source: RWG

Category: Management Tools: Transaction Records
Req ID: PINES-025 Priority: 1
Name: transaction history
Description: Transaction history is maintained for X days (X is configurable);
monthly and annual aggregate information is maintained indefinitely.
Related Reqs: Related Process
Source: RWG
Req ID: PINES-026 Priority: 1
Name: examples of useful backroom statistics
Description: Transactions can be grouped by hour, terminal, branch, and system. Transactions include check-ins, check-outs, fines collected, patron registrations, etc., and can be queried by all transactions or by type of transaction.
Source: RWG

Req ID: PINES-027 Priority: 1
Name: types of check-in
Description: The system counts all types of check-in individually and cumulatively: book-drop, by terminal, by user or self-service.
Source: RWG

Req ID: PINES-028 Priority: 1
Name: types of check-out
Description: The system counts all types of check-out individually and cumulatively: staff check-out, self check-out, staff renewal, self checkout renewal, online renewal, OPAC renewal.
Source: RWG

Req ID: PINES-029 Priority: 1
Name: holds and locations
Description: The system counts all hold requests, including how the hold was placed: at a staff desk, at a public computer inside the library, or remotely.
Source: RWG

Req ID: PINES-030 Priority: 1
Name: transactions report
Description: The system can generate a report of transactions (holds placed, holds filled, and check-outs) per patron, per library, per selected group o libraries, per system, per county. The system displays the number of check-outs and placed holds per patron. Holds are subtotaled by type, e.g. active, frozen, and frozen-until holds.
Source: RWG

Category: Management Tools: Financial Records

Req ID: PINES-031 Priority: 1
Name: value of items report
Description: The system can generate a report of the value of items (based on data in item record) in the entire collection or a portion. Example: staff can obtain value of all items with status of longoverdue, or value of all dvds in children's collection, or value of entire collection.
Source: RWG

Req ID: PINES-032 Priority: 1
Name: standard accounting practice and auditing requirements
Description: All reports and data archiving must comply with standard accounting practice and state, county, and municipal auditing requirements.
Source: RWG
Req ID: PINES-033 Priority: 1
Name: financial data (patrons)
Description: Fines, charges, waivers, and ecommerce transactions are attached to patron and item records. System tracks fines waived and payments made per library. Financial information can be updated easily. As an example, a staff user can easily query patron accounts with balances
greater than X dollars.
Source: RWG

Req ID: PINES-034 Priority: 1
Name: financial reports
Description: The system provides financial reports including: patron account balances by patron, home library, and system; fines and charges accrued per time period (e.g. last twelve months, YTD, last
month) and per type of charge (overdue fines, damaged item charges, lost item charges, etc.); fines waived per time period and per branch; payments made per time period and per payment method (e.g. staff desk, self-check station, OPAC).
Source: RWG

Req ID: PINES-035 Priority: 1
Name: financial audit trail
Description: The system maintains a ledger of patron payments, including which charges payments are applied to, to facilitate reconciliation.
Source: RWG
 
Appendix A – PINES Reports Examples
Canned reports would be pre-set reports
On Demand Reports would be preset but have the ability to edit selection criteria and display options

CIRCULATION Canned or On Demand Reports
•	Check in Count 
•	Checkout Count - includes checkouts only 
•	Items overdue by X days -daily, shelf reading, patron contact info 
•	Circulation Count by Circ Modifier, Cat1, and Cat2 (Adult, YA, Juv...) 
•	Renewals Count 
•	Non-Cat Count 
•	Circulation Count -total circ including checkouts, renewals, and noncats
•	Total Circulation Count (Merging both Cat and Non-Cat circulation data by Circ Mod & Non-Cat Item Type and facility) 
•	Circulation Count by Dewey
•	Circulation Count by Circ Modifier  
•	Circulation Count by Shelving Location 
•	Circulation Count by MARC 
•	Circulation Count by Circ Location broken down by Patron County 
•	Circulation Count by Circ Location broken down Patron Home Library 
•	Circulation Count by Age Demographic 

ITEMS Canned or On Demand Reports
•	Items Added Count 
•	Items Deleted Count 
•	List of Items Added 
•	List of Items Added (Cataloger's version, displaying the various Copy Editor fields)
•	Items Edited Count 
•	Items Count 
•	List of Items by Fines Stopped Reason 
•	Items Currently Checked Out 
•	Items more than XX days overdue (aka Overdue Materials Report) 
•	Items marked longoverdue by system 
•	List of Items with a > Total Use Count  
•	List of Items with a < Total Use Count [Weeding Report] 
•	List of Items Deleted 
•	Last Copy Report (last copy owned by a library system that was deleted)
•	List of Items by Creation Date Range 
•	List of Items with a status of Missing 
•	List of Items in Transit by both sending library and destination library  
•	Claims returned 
•	List of Long Overdue
•	Weeding report - a report that lists the date of the last circulation and the number of circs - possibly create date - with the purpose of identifying candidates for de-selection.  
•	List of items with XXX in bib record
•	Age of collection by call number or shelving location 
•	Price value of collection by call number or shelving location 
•	Items to be Converted (used in batch converting items from one status to another -- examples, items missing for X months to be converted to discard/weed or item In process for X months to be converted to missing, etc.) 

BIB RECORDS Canned or On Demand Reports 

•	Bib Records Count 
•	Bib Records Edited Count 
•	Bib Records Added by user by library Count 
•	Bib Records with No Volumes attached
•	Bib Records missing specific MARC fields

PATRONS Canned or On Demand Reports 

•	Patron Count 
•	Patron Added Count by Month 
•	New Patron Count (patrons added the previous month by Demographic Category & facility)
•	Patron Count by Age Demographic 
•	Patron Count by County   
•	Patron Count by County, City, & Zip Code  
•	Patron Count by Home Library 
•	Patron Count by Profile Group
•	Patron Count by survey answer (for custom surveys) 
•	List of patrons by survey answer (ex: survey is do you want to be on mailing list?) 
•	Voter Survey Responses County by Week
•	List of Patrons by Expiration Date 
•	Voter Reg Survey Responses Count by Week 
•	List of patrons who are BARRED (JennD) 
•	List of Patrons with inactive status 
•	List of Staff Accounts with date of last password change and account expiration date-- GT 
•	List of Patrons with specific wording in notes (used to identify patrons "pushed to collections")

HOLDS Canned or On Demand Reports 

•	Holds Purchase Alert
•	Items Sent for Holds 
•	Items Received for Holds 
•	IntraPINES Loans for all Systems 
•	IntraPINES Loans for all Facilities 
•	IntraPINES Loans by System 
•	IntraPINES Loans by Facility
•	Unfilled Holds 
•	Annual # of holds placed
•	Stale Holds - holds sitting on hold shelf waiting for pickup for too long

IN HOUSE USE Canned or On Demand Reports 

•	 NonCat In House Use Count by Month 
•	 Cataloged In House Use Count 
  
  TRANSITS Canned or On Demand Reports 

•	Items In Transit to Destination Library 
•	Items In Transit by Sending Library
  
  BILLS Canned or On Demand Reports 

•	Bills currently Owed by Patrons 
•	Detailed Payments Received  
•	Detailed Forgive, Work, and Goods Payments Received 
•	Detailed Voids 
•	Aged Debt 
 
Appendix B – Fine-Grained Requirements
•	Three interfaces - canned reports, noncanned or on demand reports, and open template reporting
•	Canned reports are generic reports set to run by the individual either ASAP or recurring.  There should be a certain set of templates that are pre-written and delivered with the Evergreen product.  Will have the ability for it to run by yesterday’s data, last week's, last month's, or last year's.  Canned reports can be checked off from a list to run at the same time and will be viewed within one document.
•	Noncanned or On Demand Reports - would be for pre-selected criteria but for things like maintenance reports or collections development and  would be set to run on demand
•	Open Template Reporting - would have all attributes associated with say circulation, items, patrons, bills, and bibs to select from for filtering and the same attributes for displaying.  
•	"Quick Access Interface"
•	 Ability  to hover over each title of canned report/template with pop-up box with description. i.e., “check-in count report gives monthly numbers on X for the preceding month’s.” 
•	 Check off any part of data you want 
•	 Ability to  select Run ASAP. Hourly, Daily, Weekly, Monthly, Yearly 
•	Output would be in Excel, HTML, and CSV format
•	 Ability to enter email addresses for report to be sent to -would be great to have an address book of regularly used addresses 
•	 Ability to edit recurring reports by adding or removing certain reports selections as well as editing the email addresses  
•	Ability to determine the output results in a way such that a result could have one column for last month's circs, another for previous month's Circ, a percent difference column, previous year's month column, a percent difference from last month to last year's month column
•	The system provides a report to assist in the batch conversion of statuses. The report would be configurable by number of months an item had been in a given status.
•	Ability to edit canned report for display purposes such as adding shelving location as a display?  
•	Ability to add more canned reports via permission level
•	Ability to get a list of items deleted that was the last copy owned by the library system in order to update WorldCat
•	Ability to prioritize certain types of reports so they will pop to the top of the queue over resource-consuming reports 
•	Ability to have a total use count on items as well as a use count broken down by usage date range such as an FY use count or monthly use count
•	Ability to retrieve total circ including checkouts, renewals, and noncats with a breakdown displaying those circ types
•	Ability to upload a text file such as barcodes or TCN to use for filtering on a report
•	Ability to run reports for pre-overdue, overdue, and holds notices sent 
•	Pivot table output 
•	Tested and proven  output
•	Ability to cancel a report that has already been scheduled to run or is currently running 
•	All nulls and blank fields must be included in the results no matter what is being filtered or displayed 
•	Ability to have real time reporting 
•	Ability to have historical reporting - a reporting warehouse such that data can be acquired on a given date or date range.  What was the bill amount on June 30th?  What was the circ count by circ mod or shelving location on x past month even though the shelving location is currently different than it was at the time of check out. 
•	Selection criteria is clearly defined
•	Report results would include the date selection criteria at the top or bottom to quickly see date range selected along with the name of the report
•	Ability to select the survey name and not have to enter the survey id for filtering
•	Ability to run a report on deleted items that were the last copy in the facility
•	Ability to pull MARC record fields so that they appear on a single row of data. Currently to pull a report with title and subtitle info or a report with all of the subject headings, one must heavily massage an excessively large report with numerous duplicate rows for each title/TCN.
•	Ability to run a report on transactions that occurred on x date and time on x workstation or by x staff

Open Template Reporting
•	Create an "open" template that allows for each of the attributes associate from circulation, patrons, items, bibs, and bills to be checked of for inclusion or exclusion when filtering as well as all of those attributes can be selected for display purposes
•	An Open template would have all attributes associated with items, patrons, bills, circulation, and bib records to select from for filtering and the same attributes for displaying.   
•	For instance, Circulation would have an option to check a box to filter by circ mod.  This would have the attribute of circ modifier as a selection to include or exclude and then have a drop down to select any circ mods to filter by.  All filter options would be listed as display option as well.  So, a display option would be circ modifier. 
•	Ability to get a snapshot bills report going back in time. 
•	Ability to have the last edit date on reports be for only when the item is edited and not to include last circulation
•	Ability to indicate last circulation date
•	Checkin Date/time should not include renewals
