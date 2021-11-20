# Twilio Fronline Salesforce Integration
This Salesforce code base provides the functionalities to display data dynamically in the Frontline application.

Prerequsits:
    1. Twilio Phone Number

    2. Front line user name:
    
    3. Salesforce Developer Sandbox: Provision a Salesforce developer sandbox (https://developer.salesforce.com/signup) 

## Deployment

Step 1: Get the code on your local pc.
Step 2: Open the project in VS Code.
Step 3: In Visual Studio code, open the Command Palette by pressing Ctrl+Shift+P on Windows or Cmd+Shift+P on macOS.
Step 4: Autorize a Salesforce Org. Make sure that you have already installed the Salesforce Extension Package  
        1. Type SFDX
        2. Select SFDX: Authorize an Org.
        3. Select the login option accordingly. Select login.salesforce.com to login into your developer Org
        4. Log in using your Org.
        5. If prompted to allow access, click Allow
        6. After you authenticate in the browser, the CLI remembers your credentials. The success message should look like this:
Step 5: Run following command in VS Code terminal window
    sfdx force:source:deploy --manifest manifest/package.xml
Step 6: Login to Salesforce, Go to setup, search for "user" in quick find box
Step 7: Click a user who is a frontline agent, click edit and enter frontline username in Twilio Frontline username field and add Twilio Frontline phone number to mobile field.  
Step 7: Configure Custom Labels to display dynamic Frontline tamplates.
    1. setting_days : Set no of days to pull the task or activities scheduled for an user. 
    2. setting_template_blockKeywords: Comma separated block keywords
    3. setting_template_case: Display case information. You can configure following case properties.
        1. CaseNumber
        2. Subject
    4. setting_template_stocks: Display custom object Recommendation data. You can configure following Recommendation object properties.
        1. File_Link__c
        2. Ticker_Symbol__c
    5. setting_template_task : Disaply customer scheduled tasks as template in Frontline.You can configure following Task object properties.
        1. ActivityDate
        2. Owner.Name
        3. Owner.Email
    6. setting_template_video: Add a video conversation link. 




## Configure Your Salesforce DX Project

The `sfdx-project.json` file contains useful configuration information for your project. See [Salesforce DX Project Configuration](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_ws_config.htm) in the _Salesforce DX Developer Guide_ for details about this file.

## Read All About It

- [Salesforce Extensions Documentation](https://developer.salesforce.com/tools/vscode/)
- [Salesforce CLI Setup Guide](https://developer.salesforce.com/docs/atlas.en-us.sfdx_setup.meta/sfdx_setup/sfdx_setup_intro.htm)
- [Salesforce DX Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_intro.htm)
- [Salesforce CLI Command Reference](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference.htm)
