Getting Started
===============
You will be provided the following pieces of information in your starter kit:

URL:_______<application URL>________________________________
Company: _________________________________________________
User: _____________________________________________________
Password: _________________________________________________

Keep this information handy as you go through this guide and configure your system. 

**Planning your deployment**

RLCatalyst Command Center is capable of multi-tenancy. Using the same instance of the software, you can create several tenants. Each tenant can configure his own machines for monitoring. Each tenant can also configure his own cloud accounts and get an independent view of his cloud assets.
The landlord can create new tenants in the system.

**Creating your first tenant**

To plan the creation of a new tenant, use the planning sheet in Appendix A to collect all the information required upfront. Keep the sheet handy as you go through the following steps.

Open a browser (we recommend Chrome or Firefox). Enter the Application URL provided. The login page should open.

 .. image:: images/login.png

To register a tenant, click on the Register link which is available on the login page & application will display Register screen to the user.  

 .. image:: images/registeraccount.png

Use details from *Appendix A* for Company Name, User Name, Email & set the Password as per Password policy. Click on Create Account button. You will see a Thank You screen confirming that a verification email has been sent to the email address registered.  

 .. image:: images/VerificationEmailSent.png

 Check the verification email delivered to the registered email address & click on the verification link to activate the account. On successful validation, tenant will be allowed to login into the Command Center.  

.. image:: images/VerificationEmailConfirmed.png

**Logging in as a tenant**

Open a browser (we recommend Chrome or Firefox). Enter the application URL provided. The login page should open. On the login page, fill the Company, User and Password fields as captured in Appendix A. Then click the Login button. You will see the landing page.  
  Business Service Status View – by default this will not show any data. You will need to configure business services following the instructions in this guide.  
 
  Service Health – providing a quick way of viewing at a glance, if any of the linked services 
(across BSM’s) are in alarm state (Yellow & Red). By clicking on critical/warning service card, the system shall navigate to the Services page and should show the Service and Nodes tabs related to selected service. 
  
  ServiceNow Ticket Snapshot – by default this will not show any data. You will need to configure a Service Now account following the instructions in this guide.  
  
  BOT’s Summary (Total)- We need to configure a Catalyst Account to view the count of Bot’s summary.  

.. image:: images/dashboardBSMView.png

**Historical BSM Health Indicator**

Historical BSM Health Indicator gives you the ability to see the trend of the BSM over last 30 days as a consolidated view. Using this view, the user can then navigate to specific outage view of interest.  
  
The view can be available with a “Trend Icon” on Top-Left of BSM View and clicking that can show the Consolidated status of all BSM over last 30 days with appropriate status.  
  
.. image:: images/HistoricalStatusTrendIcon.png

.. image:: images/HistoricalStatusView.png

Clicking the link of Outage (Red) or Partial Outage available in the Historical Status Dashboard will take the user to the appropriate Outage Drill-down page  

.. image:: images/HistoricalStatusDrillDownView.png

**Configuring Cloud Credentials**

RLCatalyst Command Centre gives you the ability to view all your cloud assets (spanning across providers and accounts) in one place. These assets include:  
  Virtual Machines  
  ELBs  
  Security Groups  
  Networks  
  
Configure your Cloud Account Details in the Command Centre Settings to view all your cloud assets in one place. Command Centre collects the information from the configured cloud account periodically. You can configure the interval in which this information refreshes.   

.. image:: images/ProviderSettings.png

In Provider Settings, we have categorized the providers based on their services. Depends on Category selection Provider List will load the available vendors.

.. image:: images/AddProvider.png

Command Center will support for following Cloud Account providers.
  Microsoft Azure
  AWS
  Google Cloud

To configure a cloud account:  
  1.	Click on the Settings icon in the top bar.   
  2.	Click on the Provider Settings tab  
  3.	Click + button and add your cloud account credentials in Settings with the details captured in Appendix A. Example provided below is for a Microsoft Azure account. 

| Field                       | Instructions                                           |
|-----------------------------|--------------------------------------------------------|
| Account Name                | Enter a Friendly name                                  |
| Vendor                      | Choose Azure                                           |
| Time Zone                   | Choose IST                                             |
| Authentication Type         | Choose OAuth                                           |
| Client ID                   | Enter the Client ID of your Azure application E.g.: 9812d575-dja-4b48-8434-hdgh |
| Client Secret               | Enter the Secret key of your Azure Application         |
| Grant Type                  | Enter the text ‘client credentials’                    |
| Resource                    | https://management.azure.com/                          |
|                             |                                                        |
| Subscription ID             | Enter the Azure subscription ID                        |
| Tenant ID                   | Enter the Azure Tenant ID                              |
| Schedule                    | Enter the Time Interval for collecting data from Cloud |
| Repeat                      | Choose the Interval Type – Minutes/Hourly              |

*Note: To get the Client ID and Client Secret key, create an application in Azure and set the Role as Reader. To set the Role, Go to Subscription->Resource Group->Access Control(IAM)->Add>Permissions->Add Reader Permission*

.. image:: images/AddProviderAzure.png