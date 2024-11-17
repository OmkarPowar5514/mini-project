# mini-project
Problem 1 (kloudrac Assement 1) - 
        Database Overview:
            Database Name: Banking
            
            Tables: userlogin: Stores user details like ID, username, password.
                    accounts: Stores bank account information like account number, balance, transaction types, and links to the user.
                    transaction: Stores transaction details like type (deposit/withdrawal), amount, date, and links to the account.
          
            How the tables relate:The userlogin table stores user info and allows them to log in.
                                The accounts table stores information about a user's bank account, including balance and withdrawal limits.
                                The transaction table stores the details of transactions like deposits or withdrawals.
          
        API Creation with Node.js and Express:
            Files and Their Roles:server.js: The main file to run and handle API requests.
                                    db.js: Contains the database connection setup.
                                    .env: A file to store sensitive information like database credentials and port safely.
                                    Controller files (e.g., userloginController.js, accountController.js, transactionController.js): These files handle the business logic, which runs when an API request is made.
                                    Route files (e.g., userloginRoutes.js, accountRoutes.js, transactionRoutes.js): These files define how API requests are routed and which controller should handle them.
          
        How it Works: Using these files and structure, I created an API that connects to the database, allowing us to store and fetch data (like user info, account details, and transactions).

Problem 2 (Kloudrac Assesment - Senior Salesforce Developer - Assesment - 2) - 
      Salesforce Object & Details:
          Object Name: GST_Detail__c
          Fields: GST_Number__c, Legal_Name__c, Address__c, GST_Status__c, Business_Type__c.
      
      Backend (Apex Classes and Methods:
          Apex Classes:  GSTDetailRestApiHandler: Handles the API logic for fetching GST details.
                         InsertGstDetailHandler: Handles the logic for inserting GST details into the Salesforce database.
          Apex Methods:  fetchGSTDetails: A REST API method (marked with @AuraEnabled) that allows you to get GST details by passing a GST number.
                         addGstDetail: Another @AuraEnabled method that inserts new GST details into the GST_Detail__c object in Salesforce.

      LWC (Lightning Web Component:
          Component Files:  gstDetailCmp.html: The HTML template for the Lightning web component.
                            gstDetailCmp.js: The JavaScript file containing custom logic, validations, and imported Apex methods.
                            gstDetailCmp.js-meta.xml: A metadata file that controls the component's visibility and where it can be used within Salesforce.

      How It Works :  User Input: When a user enters a GST number, the system first checks if it's a valid GST number.
                      Fetching GST Details: Once the user clicks the "Get GST Detail" button, the fetchGSTDetails method is called to retrieve the GST details and display them in a grid.
                      Saving Data: After the details are shown in the grid, the user can click the "Save" button to save the GST details to the GST_Detail__c object in Salesforce.
                      The system also checks if the record already exists in Salesforce. If it does, it won’t add it again.
