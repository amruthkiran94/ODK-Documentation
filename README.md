
# INTRODUCTION

ODK or the Open Data Kit is an Open source suite of tools to build, collect and manage data, especially in resource constrained environments. Built by a team of developers across the world, major organisations from the likes of Google, WHO and Red Cross use the ODK for collecting data using a variety of tools built and optimised for mobile and web-based applications. Tools such as, ODK Collect for the mobile based data collection both in online and offline environments. ODK Aggregate, the remote server for the central database and management of forms and ODK Briefcase, the desktop application for handling everything in between.

# USECASES

ODK, being open sourced and completely free allows a wide range of applications to be built for specific use-cases around the world. A few of them are listed below:

## Field Data collection

- Hungry Cities Project - Indian Institute for Human Settlements, Bangalore.
- Ebola Aid in Africa - Measure effectiveness of relief efforts.
- Forest Monitoring in Indonesia.

## Data Management

- ODK Aggregate to push, pull and export forms.
- ODK-QGIS integration for spatial data support.
- ODK for researchers by London School of Hygiene and Tropical Medicine.

# Creating Survey Forms for ODK

There are two methods to creating the survey forms:

## Using ODK build ([**https://build.opendatakit.org/**](https://build.opendatakit.org/))

This is the official web-based tool developed to quickly create simple forms using drag-drop features on a web browser. Although it is quite easy to create and upload forms onto servers, it is only viable for simple or short surveys. More complicated surveys with many questions and interconnected logic might be quite hard to replicate on a web-based tool. This is recommended for simple surveys or for testing.

## Using XLSForm (Excel based)

Excel (Offline) based form building offers more flexibility and customisation as compared to its web-based counterpart. The Excel (.XLSX) worksheet created will have the following information on different sheets:

1. Survey
2. Choices
3. Settings

The &quot;Survey&quot; sheet will house the questions from the questionnaire provided to us. As well as some technical requisites such as the &quot;Data Type&quot;, &quot;Name&quot;, &quot;Label&quot; and more. Please refer to our example worksheet and the documentation on &quot;[ODK Questions Types](https://docs.opendatakit.org/form-question-types/)&quot; and &quot;[XLS Forms](http://xlsform.org/en/)&quot; for further details on the same.

XLSForm is a form standard created to help simplify the authoring of forms in Excel. Authoring is done in a human readable format using a familiar tool that almost everyone knows - Excel. XLSForms provide a practical standard for sharing and collaborating on authoring forms. They are simple to get started with but allow for the authoring of complex forms by someone familiar with the syntax described [here](http://xlsform.org/en/).

The &quot;Choices&quot; sheet will contain a variable and its corresponding question from the Survey sheet to the many options that question might have (as prepared in the questionnaire). These options will be reflected on the ODK Collect App along with the Questions.

&quot;Settings&quot; would contain the &quot;form title&quot;, &quot;ID&quot;, &quot;Version&quot; and a &quot;Submission URL&quot;. These have to be setup prior to conversion (to XLS) and each variable would be unique to the survey question version being edited and have to be updated with new versions that come later. The &quot;Submission URL&quot; would point to the Google Drive account where these forms would be submitted as results in Excel sheets. Here we use account # 2 ([gsl@iihs.ac.in](mailto:gsl@iihs.ac.in)) which is only accessible by IIHS.





# Convert Survey Form to XLS format

Once the questions, options and settings are filled in, the Excel worksheet needs to be converted into ODK ready format. The format is XLS. The Excel can be converted to XLS on this [link](https://build.opendatakit.org/). This converted form now can be uploaded onto the Google Drive account setup with the following credentials:

**Username** : iihs.ncdhr@gmail.com

**Password** : test123iihs

The same credentials will be updated into the ODK collect app so that the forms can be access by the surveyors.

# Platform to Manage Survey Forms

The account [iihs.ncdhr@gmail.com](mailto:iihs.ncdhr@gmail.com) is used to store the converted XLS forms, which can be accessed by the ODK Collect App. This account will also store the media files (Images and Videos) from each surveyor&#39;s submission in a folder called &quot;Open Data Kit&quot; with folders ordered by survey version edits. Create a folder for each new project and upload the XLS form into this folder.

# Setting Up ODK Collect App

The ODK collect is an Android based application to collect field based survey data from forms created via Excel(XLS). This renders the form into a sequence of human readable format with logic, constraints and repetitive sub-structures. Each user would be provided with the same questions as entered in the XLS form in a clean user-interface which can also work in offline mode (once the form has been downloaded).

The app has the following tabs/buttons:

- Fill Blank Form

To start survey with newly downloaded blank form

- Edit Saved Form

Edit previously completed form

- Send Finalized Form

Send Competed form to Server

- View Sent Form

View all sent forms from this device

- Get Blank Form

Download new/blank form from server

- Delete Saved Form

Delete existing instances of the form from device (blank and completed)

<a href="https://imgbb.com/"><img src="https://i.ibb.co/fq5p2Sb/1.png" alt="1" border="0"></a>

ODK Collect Main Menu 

- Settings
- About
  -
    - Basic information about the App/Developers
- General Settings
  -
    - Server
    - Platform
      - ODK Aggregate
        -
          - URL
          - Username
          - Password
      - Google Drive, Google Sheets
        -
          - Google Account
          - Fallback Submission URL
      - Other
        -
          - URL
          - Username
          - Password
          - Other Platform Settings
          - User Interface
          - Form Management
          - User and Device Identity
- Admin Settings

The sections under ODK Aggregate and Google Drive/Sheets in Settings would need to be updated based on the type of server installed. More information can be accessed [here](https://docs.opendatakit.org/collect-intro/).

If the server is based on Google Drive:

<a href="https://ibb.co/s5kqpGj"><img src="https://i.ibb.co/cbMQKHJ/3.png" alt="3" border="0"></a>

If the Server is based on AWS-Aggregate:

<a href="https://ibb.co/SxtNmWV"><img src="https://i.ibb.co/3sp1FGS/4.png" alt="4" border="0"></a>

## How to Submit a form?

Once the server has been linked on the ODK application, the following methodology can be used to download a blank form and start the survey.


<a href="https://ibb.co/4VZXVZj"><img src="https://i.ibb.co/hmR4mRK/5.png" alt="5" border="0"></a>

Internet connectivity is required to download the blank form and to submit the completed form from and to the server. While it is not necessary to have internet connectivity while running the survey, some questions such as obtaining location information might not work without it.

# Platform to Manage Submitted Forms

Currently two platforms have been tested to host submitted data for its storage and management. Google Drive/Sheets and ODK Aggregate.

**Google Drive**

<a href="https://imgbb.com/"><img src="https://i.ibb.co/NtGbjhy/6.png" alt="6" border="0"></a>

Google Drive form Management

If the setup to pull and push via Google Drive is used then the Submitted forms or results are stored in the [gsl@iihs.ac.in](mailto:gsl@iihs.ac.in) (Google Drive). Prior to this, Create a folder with an empty Google Sheet preferable named with the version of the form created. &quot;Share&quot; the sheet by creating a link that _anyone can view and_ edit from the &quot;Share&quot; button on the top-right of the page.

The &quot;Submission URL&quot; in the **created survey form** (3rd tab/sheet) needs to be updated with the link to **this empty sheet.**

**ODK Aggregate on AWS**

<a href="https://imgbb.com/"><img src="https://i.ibb.co/tsgfx56/7.png" alt="7" border="0"></a>
 
AWS-Aggregate Management

ODK Aggregate is a server-side implementation/tool to manage forms and submissions. The server can be setup on multiple platforms like Amazon Web Services (AWS), Google Cloud, Apache-Tomcat and others.

AWS based ODK Aggregate was tested and the steps to install the server on an AWS instance can be followed [here](https://docs.opendatakit.org/aggregate-aws/).

# Analysis

Once the surveys are completed and consistent backups are created, the Excel sheet based analysis can be carried out with the &quot;result&quot; sheet in the account [gsl@iihs.ac.in](mailto:gsl@iihs.ac.in).

## Pivot Tables

The first tab in the &quot;result&quot; excel sheet is the user-wise submission. This would be our main datasheet. Using this sheet and the corresponding answers to the questions, simple pivot tables and charts would be created to visualise the outcome of the surveys.

Create a new excel sheet and copy the complete datasheet from the &quot;result&quot; excel file. Create as many new tabs required in this new worksheet, this depends on the number of questions. See sample file for more information.

Pivot table are easy to create and enables to quickly compare multiple elements in an excel datasheet. Visit [here](https://support.office.com/en-us/article/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576) to learn more.

## Charts

Once Pivot tables are created, corresponding charts or pivot charts can be simultaneously created for each question. Visit [here](https://support.office.com/en-us/article/create-a-pivotchart-c1b1e057-6990-4c38-b52b-8255538e7b1c) to learn more.

## Macros

Analysing over 50 questions can be quite a manual task. Using VisualBasic Macros built for Microsoft Excel, we can automate large workflows with simple set of code modules.

First, Enable Developer mode in Excel by following the steps below:

-
  - On the File tab, go to Options \&gt; Customize Ribbon.
  - Under Customize the Ribbon and under Main Tabs, select the Developer check box.
  - After you show the tab, the Developer tab stays visible, unless you clear the check box or have to reinstall a Microsoft Office program.

Secondly, open the VB editor (Alt+F11) and select worksheet and insert module. Write or paste the VB code into the module, save and run as per module requirement.



Here are some links to macros and its supporting resources:

**Example Macro to create Pivot Chart**
```
Sub createPivotChart1a()

Dim PvtTbl As PivotTable
Dim rngChart As Range
Dim objChart As Chart
Set PvtTbl = Worksheets("Sheet14").PivotTables("PivotTable1")

'use the Charts.Add Method to add a new chart sheet in the workbook, which is represented as a Chart object

'adds new chart sheet before or after specified sheet:
ActiveWorkbook.Charts.Add Before:=Worksheets("Sheet14"), Count:=1

'Alternate 1: to add new chart sheet before the active sheet, use below code line:
'Set objChart = Charts.Add
'Alternate 2: to add new chart sheet after the last worksheet, use below code line:
'ActiveWorkbook.Charts.Add After:=Worksheets(Worksheets.Count)

'set as active worksheet:
Set objChart = ActiveSheet

'set range for the PivotChart, based on the existing PivotTable:
Set rngChart = PvtTbl.TableRange2

'specify the source data for the PivotChart, name of chart sheet and the chart type:
With objChart
.SetSourceData rngChart
.Name = "PivotChart1"
.ChartType = xlColumnClustered
End With

End Sub
```
# Appendix-A

## Do&#39;s and Don&#39;ts before/while you start creating forms

- Options such as
    - Others
    - Did not answer
    - Don&#39;t know/Can&#39;t say
    - Not Applicable, should be included for all relevant questions
- Add &quot;[DO NOT READ ALOUD]&quot; for questions/options that need not be asked.
- Make sure to include all possible options. For example: if the options are _1 day_, _2 days_ and more than _3 days_, then where would _3 days_ be recorded?
- &quot;Specify Other&quot; column is asked only if the responded has chosen &quot;other&quot; in the previous question. Do not ask questions for which they have answered &quot;No&quot; already.
- Save the Excel file as a new file using &quot;\_V[number]&quot; for every major edit (\_V1, V2 ...)
- **Make sure to change the**  **form\_title, form\_id**  **and**  **version**  **in the settings tab of the Excel sheet for every new version/edit.**

## Do&#39;s and Don&#39;ts for settings up ODK collect

1.Check the following:
      1. Downloading Blank form successfully from server (Google or Aggregate)
      2. Flow of the questions (If questions are being missed or repeated)
      3. The logic of nested questions
      4. Test the submission URL by conducting a sample survey with the created form and try sending the form. This confirms that the submission URL is working.

**Caution:** In questions requiring multiple options, if the respondent&#39;s response involves more than 3 responses, the Google Sheet registers the answer as a _Date_. (i.e. if 1,2 and 3 options are registered as 01-02-2003). To Avoid this, conduct a sample survey and submit the results with these multiple options. The column names are auto populated, identify the columns with these specific multiple options questions and change the data type as follows:

&quot;Format&quot; -\&gt; &quot;Number&quot; -\&gt; &quot;Plain Text&quot;

                     This ensures the responses are saved as numbers (i.e. 1,2,3)

## Do&#39;s and Don&#39;ts while survey is being conducted
  - Take regular backups of the submitted forms
  - In cases of forms being updated (additional questions, options etc…)
    1. Make a new version of the survey form with corresponding naming conventions and ensure the surveyors do not delete the older versions from their ODK Collect application. This is so that, older submissions can still be carried out (deletion of blank forms prohibits the submission of the said form).
    2. New surveys should also be submitted to a new Google Sheets file. Repeat the instructions to setup the &quot;Result&quot; Sheet as described in the sections above (with changes to the settings tab also).

Resources:

- [Office](https://support.office.com/en-us/article/quick-start-create-a-macro-741130ca-080d-49f5-9471-1e5fb3d581a8)
- [ExcelChamps](https://excelchamps.com/blog/category/vba/)
- [ExcelEasy](https://www.excel-easy.com/vba/create-a-macro.html)
