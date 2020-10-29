# Workday- Maximo Integration Configuration

## Steps

1. [Create Report Maximo Skills](https://github.ibm.com/Watson-IoT/maximo-workday/blob/master/workday_setup.md#create-report-maximo-skills)
2. [Create Report Maximo Crafts](https://github.ibm.com/Watson-IoT/maximo-workday/blob/master/workday_setup.md#create-report-maximo-crafts)
3. [INT Maximo Worker Skills](https://github.ibm.com/Watson-IoT/maximo-workday/blob/master/workday_setup.md#create-report-INT-Maximo-Worker-Skills)
3. [Configure Scheduled Integration - Maximo Person Sync](https://github.ibm.com/Watson-IoT/maximo-workday/blob/master/workday_setup.md#configure-scheduled-integration---maximo-person-sync)
4. [Launch & Schedule Integration](https://github.ibm.com/Watson-IoT/maximo-workday/blob/master/workday_setup.md#launch--schedule-integration)


## For One Time Load

### Create report Maximo Skills

- Login into Workday Tenant.

- Security Required: Report Administrator, Report Writer

- Access task “Create Custom Report”

 ![Create Custom Report Maximo Skills.png](images/workday/Create_Custom_Report_Maximo_Skills.png)

 ![Report Maximo Skills - columns.png](images/workday/Report_Maximo_Skills_columns.png)

Filter on Category value will depend as per Configuration Workbook.

 ![Report Maximo Skills - Filter.png](images/workday/Report_Maximo_Skills_Filter.png)

Report must be shared with Integration system Security  Group / Integration User.

 ![Report Maximo Skills - Share.png](images/workday/Report_Maximo_Skills_Share.png)
 
 ![Report Maximo Skills - Advanced.png](images/workday/Report_Maximo_Skills_Advanced.png)

 ![Report Maximo Skills - View URLs.png](images/workday/Report_Maximo_Skills_View_URLs.png)

 ![Report Maximo Skills - JSON.png](images/workday/Report_Maximo_Skills_JSON.png)

 **REST API Endpoint:**

https://wd2-impl-services1.workday.com/ccx/service/customreport2/ibmsrv_dpt5/lmcneil/RPT_INT_Maximo_Skills?format=json


## Create report Maximo Crafts

- Login into Workday Tenant.

- Security Required: Report Administrator, Report Writer

- Access task “Create Custom Report”

 ![Create Custom Report Maximo Crafts.png](images/workday/Create_Report_Maximo_Crafts.png)

 ![Report Maximo Crafts - columns.png](images/workday/Report_Maximo_Crafts_Columns.png)

Filter on Category value will depend as per Configuration Workbook.

 ![Report Maximo Crafts - Filter.png](images/workday/Report_Maximo_Crafts_Filter.png)

Report must be shared with Integration system Security  Group / Integration User.

 ![Report Maximo Crafts - Share.png](images/workday/Report_Maximo_Crafts_Share.png)
 
 ![Report Maximo Crafts - Advanced.png](images/workday/Report_Maximo_Crafts_Advanced.png)

 ![Report Maximo Crafts - View URLs.png](images/workday/Report_Maximo_Crafts_View_URLs.png)

**REST Endpoint**

https://wd2-impl-services1.workday.com/ccx/service/customreport2/ibmsrv_dpt5/lmcneil/RPT_INT_Maximo_Crafts?format=json


## Create report INT Maximo Worker Skills

- Login into Workday Tenant.

- Security Required: Report Administrator, Report Writer

- Access task “Create Custom Report”

 ![Create Custom Report INT Maximo Skills.png](images/workday/Create_Custom_Report_Maximo_Skills_INT.png)

 ![Report INT Maximo Skills - columns.png](images/workday/Create_Custom_Report_INT_Maximo_Skills_Columns.png)

Filter on Category value will depend as per Configuration Workbook.

 ![Report INT Maximo Skills - Filter.png](images/workday/Create_Custom_Report_INT_Maximo_Skills_Filters.png)

 ![Report INT Maximo Skills - Prompts.png](images/workday/Create_Custom_Report_INT_Maximo_Skills_Prompts.png)

Report must be shared with Integration system Security  Group / Integration User.

 ![Report INT Maximo Skills - Share.png](images/workday/Create_Custom_Report_INT_Maximo_Skills_Share.png)
 
 ![Report INT Maximo Skills - Advanced.png](images/workday/Create_Custom_Report_INT_Maximo_Skills_Advanced.png)

 ![Report INT Maximo Skills - View URLs.png](images/workday/Create_Custom_Report_INT_Maximo_Skills_View_URLs.png)
 

 ## Configure Scheduled Integration - Maximo Person Sync

 ### Configure Core Connector Worker Integration template 

- Login into Workday Tenant.
- Security Required: Report Administrator, Report Writer, Integration Build
- Access task “Create Integration System”

![Create Integration System](images/workday/Maximo_Person_Outbbound_Create_Integration_System.png)

![Configure Services](images/workday/Maximo_Person_Outbbound_Configure_Services.png)

![Configure Services](images/workday/Maximo_Person_Outbbound_Configure_services_2.png)

![Create Field Override Services](images/workday/Maximo_Person_Outbbound_Create_Field_Override_Service.png)

![Configure Field Override Service](images/workday/Maximo_Person_Outbbound_Configure_FoS.png)

![Integration_Field_Attributes](images/workday/Maximo_Person_Outbbound_Configure_Integration_Attribute.png)

![Integration_Field_Attributes_1](images/workday/Maximo_Person_Outbbound_Configure_Integration_Field_Attributes_1.png)

![Integration_Field_Attributes_3](images/workday/Maximo_Person_Outbbound_Configure_Integration_Field_Attributes_2.png)

![Integration_Field_Attributes_3](images/workday/Maximo_Person_Outbbound_Configure_Integration_Field_Attributes_3.png)

![Integration_Field_Attributes_4](images/workday/Maximo_Person_Outbbound_Configure_Integration_Field_Attributes_4.png)

![Configure_FoS_Navigation](images/workday/Maximo_Person_Outbbound_Configure_FoS_Navigation.png)

![Configure_Field_Override_Service](images/workday/Maximo_Person_Outbbound_Configure_Field_Override_Service.png)

**Importing Studio Integration**

[How to Download Studio](https://community.workday.com/studio-download)

- Download the clar file from : [WorkdayStudioCLAR](WorkdayStudioCLAR/INT_STD_MaximoPersonSyncCollection.clar)
- Open Workday Studio
- Navigate to File > Import.
- From Wizard select Workday > CLAR file

![Import CLAR - Wizard](images/workday/Maximo_Person_Outbbound_Studio_Import_Clar.png)

Browse for the CLAR file from your local system

![Import CLAR - File Location](images/workday/Maximo_Person_Outbbound_Studio_Clar_location.png)

![Studio Assembly](images/workday/Studio_Assembly.png)

- Save the integration and Deploy to Workday Tenant.

**NOTE** If their is change in the fields of Core Connector Worker template, changes should be updated into Transformation stage in Studio integration.
<details>

    ![XSLTPlus Component](images/workday/XSLTPlus.png)

    ![XMLToJSON Component](images/workday/XMLtoJSON.png)
    


</details>

![Create Business Process](images/workday/Maximo_Person_Outbbound_Create_BP.png)

Add another step Integration step after initiation.

![Create BP Integration Step](images/workday/Maximo_Person_Outbbound_Configure_BP_Integration_Step.png)


#### Launch & Schedule Integration


![Launch Integration](images/workday/Maximo_Person_Outbbound_Launch_Integration.png)


![Launch Schedule](images/workday/Maximo_Person_Outbbound_Launch_Schedule.png)

![Configure Schedule](images/workday/Maximo_Person_Outbbound_Configure_Schedule.png)

![Configure Schedule Parameters](images/workday/Maximo_Person_Outbbound_Configure_Schedule_Parameters.png)

